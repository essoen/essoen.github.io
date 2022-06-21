+++
date = 2022-06-21T10:57:49Z
description = "A short note on how I've made the application Todoist useful for me"
tags = ["productivity"]
title = "My setup of filters in Todoist"

+++
I'm a big fan of [Todoist](www.todoist.com), and I've used it as my main to-do app for around 7 years. I picked it after some extensive research after Wunderlist was bought by Microsoft. Recently a colleague asked me about my setup, Here's a short overview:

* I have one project per context, where I have two main projects: Work and Personal
* Each project has two sections: Do Now and Backlog
* This enables me to have the following really useful filters:
  * Overdue first, then inbox, then all work items for today, and finally all personal items for today: `overdue, #Inbox, (##Work & today), (##Personal & today)`
  * Do Now or Backlog for a context: `(##Work ) & /Do Now` or `(##Work ) & /Backlog`, and similarly with `##Personal`

See [here](https://todoist.com/help/articles/introduction-to-filters) for more on how filters work in Todoist, and more [suggestions on use](https://blog.doist.com/todoist-filters).

In addition, I have a separate main project for agendas with people, i.e. things I want to talk about with person X.

It's also worth mentioning the tool [Tascaly](https://www.tascaly.com/), which creates a calendar event for tasks that has a scheduled time of day, as well as a label for how long it'll take. E.g. `today at 13 @1h` becomes a 1-hour slot at 13:00.

I have also made it easy for me to send tasks to Todoist. So I've added the Todoist extension for my email apps, and to Slack. This enables me to schedule/plan for everything in one place. Sadly, the Todoist extension for Slack only supports one Slack team at a time. To enable me to add tasks from multiple teams, I've set up this [zap from Zapier](https://zapier.com/apps/slack/integrations/todoist/1580/add-new-saved-slack-messages-to-todoist-as-tasks).

The next step for all this to be useful is having a process around that set up to put dates on your Do Now tasks, sort your inbox into projects, and move new items from your backlog into Do Now. That's a longer story for another time.