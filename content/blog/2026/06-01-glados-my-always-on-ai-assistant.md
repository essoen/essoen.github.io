---
title: "GLaDOS: My Always-On AI Assistant"
description: How I set up an always-on Claude assistant on a VPS, and what it
  actually does for me
draft: false
tags:
  - ai
  - productivity
date: 2026-06-01T06:00:00.000Z
---

First off: I find the AI hype pretty exhausting, the second-order effects of AI jobs and energy and copyright are real, and most companies still report no measurable productivity gains from AI. I'm still a sceptic. But over the last few months something changed for me: The models have gotten better, but in particular I've found the the integrations around them has gotten good enough to be useful in my own daily life.

So I stopped trying to evaluate AI as a category and started steering based on my own quality of life instead. The goal isn't to make Claude do my thinking, but improve my own daily life by [*reducing administration and free up time*](https://www.svorstol.com/blog/2026/hva-betyr-det-for-oss-at-llmer-reduserer-administrasjonskostnaden/). In practice this means that I push the routine, low-judgment work onto an assistant, and keep the thinking for myself. [Cognitive offloading, rather than cognitive surrender.](https://leehanchung.github.io/blogs/2026/05/01/dont-outsource-your-understanding/)

To work towards that, I set up a small, cheap VPS with [Shrp in Norway](https://shrp.no). It runs an always-on Claude Code instance connected to my productivity tools, accessible from my phone via Telegram and from any browser via Claude Code's remote control feature. I call the assistant [GLaDOS](https://en.wikipedia.org/wiki/GLaDOS).

## Why a VPS over Claude.ai and CoWork?

Claude already has a chat interface at claude.ai, MCP integrations for tools like Google Calendar and Slack, and CoWork for scheduling tasks against local files. There's also Claude Code, a CLI for working with code and files directly. Nevertheless I wanted a server running Claude all the time for three reasons:

1. **Availability.** Local MCPs only work when my laptop is open. A VPS is always on, which means the assistant is reachable from my phone while I'm walking the dog, between meetings, or away from the desk. A quick Telegram message to check tomorrow's calendar or draft a reply saves real time.
2. **Context.** Chat conversations are stateless. Each session starts from scratch with no memory of yesterday, no persistent file system, no long-running processes. Projects help, but only inside the chat surface. On the VPS, Claude works directly in my Obsidian vault, so notes, meeting logs, and project files are always one read away.
3. **Workflow fit.** For this to be worth the effort, it had to augment the tools I already use rather than introduce a parallel one. The VPS lets me orchestrate MCPs, chain them into skills, schedule them with cron, and expose Claude through whatever interface I want (Telegram, web, soon probably more).

## The architecture

The VPS is the hub. Inputs come in from Telegram, the browser, or scheduled cron jobs. Claude operates on the vault and reaches out through MCP servers to the services I actually use day to day. Everything important is backed up to Backblaze B2 overnight. The following services are running:

- **Claude:** Claude Code with remote control is the core. The VPS has a service that runs `claude remote-control`, which makes the Claude session accessible from claude.ai and the Claude apps. Claude has access to my Obsidian vault, which gives it full context of my notes.

- **Telegram access:** The Telegram Claude plugin exposes the same session as a Telegram bot via a Python PTY wrapper. I message the bot, Claude processes it, replies in the chat. Quick questions, calendar checks, task management, drafting messages can then be done from my phone.

- **Obsidian Sync:** To have access to notes everywhere, I use Obsidian sync with the `ob` CLI in continuous mode, keeping the server-side vault in sync with Obsidian's sync servers. This bidirectional sync is what makes the whole thing work: Claude operates on the same vault I use every day.

- **Transcription of voice memos:** A script monitors a folder in the vault for audio files. When I record a voice memo on my phone (I use Quick Draft to quickly add them), Obsidian Sync pushes it to the VPS. The watcher picks it up, sends it to AssemblyAI with speaker diarization and language detection, and writes a structured markdown transcript back into the vault. Original audio is archived automatically. Set it up so the service is independent of the workflow, in case I want to switch to another transcription service later on. For client meetings etc. I do not use this though, but rather MacWhisper with local transcription on my Mac. For cleanup I use the LLM model and harness approved by the client.

- **Meeting transcription:** As mentioned I usually use MacWhisper locally for meeting transcription, but I have a similar setup for cleanup of meeting transcriptions that can be processed by Claude. I drop the transcript into a different folder. It runs the `/meeting-summary` skill automatically and turns raw transcripts into structured notes in the right place.

- **Backup:** Kopia runs nightly at 03:00, backing up the server to Backblaze B2 with zstd compression. Retention is 7 daily, 4 weekly, 24 monthly, 3 annual. After each backup it restarts the Claude Remote service so that new skills, agent definitions, or MCP config changes get picked up overnight without manual intervention.

- **System Monitoring:r** A script monitors CPU, RAM, and disk every 60 seconds and pings me on Telegram if anything looks off. 

Other than logging in, all these services was set up by Claude and not manually by me.

## MCP integrations

Claude connects to external services through MCP (Model Context Protocol). Currently it has access to Gmail, Google Calendar, Slack, Notion and Miro in the regular web version. There's also Todoist, but their OAuth implementation is iffy so I don't use their MCP. I've had much success with installing CLIs on the VPS for integrating with services, rather than using MCPs. So, I've done this for Todoist, Tripletex, LastFM, PocketCasts, NotebookLM, Hevy, Garmin Connect nad Readwise Reader. I've also set up self-hosted OpenNotebook instance (since Google NotebookLM integrations were very limited).

All these integrations makes it an assistant, an enables it to handle things such as "What's on my calendar tomorrow?" is a Telegram message. "Summarize unread threads on Slack" is a Telegram message. "Create a Todoist task for the quarterly review, priority 2, due next Friday" is a Telegram message. 
## Skills and agents

As previously indicated I use lots of skills, reusable prompts for specific tasks. I have skills for cleaning up transcriptions, editing blog posts, processing Readwise highlights, logging hours in Tripletex, and a dozen other things. The definitions live in a `CLAUDE/` folder in the vault with symlinks into the directory Claude Code expects.

Because they're in the vault, any change I make on my laptop syncs to the server automatically through Obsidian Sync. This means I also can use Claude Code on my computer directly, with the same agent and skills files.

Cron can run Claude as a **scheduled agent** through `claude -p "prompt" --allowedTools "tools"`. I have a daily morning brief that checks Slack, Gmail, and calendar, and a weekly review that summarizes open Todoist tasks and surfaces what slipped. Output gets piped to my Telegram session, so the briefing shows up like any other message. I've learned that from June 15, 2026, programmatic `claude -p` and Agent SDK usage [draws from a separate monthly credit billed at full API rates](https://support.claude.com/en/articles/15036540-use-the-claude-agent-sdk-with-your-claude-plan), which means I might adjust this approach.

I've been sceptical of AI tools for years. What changed my mind was not the language models themselves. It was the integrations. An LLM that can read and write to the tools I already use is fundamentally different from one that just generates text. As [one writer put it](https://mht.wtf), LLMs become useful when they can actually *do things*.

There's a related point I keep coming back to: [AI's real superpower is consuming, not creating](https://www.reddit.com/r/ChatGPT/comments/1jxqzjy/ais_real_superpower_consuming_not_creating/). The value isn't in having Claude generate text for me. It's in having it read my calendar, cross-reference my notes, and surface what I need to know right now. The consuming side, parsing, connecting, summarising across sources, is where the leverage sits. At least I can try to enjoy it while the pricing provides a reasonably cost-beneficial. 
