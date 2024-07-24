---
title:  Syncing articles between Readwise Reader and Pocket
date: 2024-07-24T17:16:58Z
description: I wrote some code to help me get use of both Readwise Reader and Pocket, so I still can read articles on my Kobo.
draft: false
tags:
  - tech
  - productivity
  - coding
---

I'm a big reader and I've used Kindles to read for a long time. I now have a Oasis (best one there is) and Paperwhite (2021). What I don't like is the lock-in, but what I also like is the ecosystem. There's always tradeoffs.

Recently Amazons competitor Kobo released colour e-ink devices, with stylus support. Their styluses, unlike Kindle devices, can write directly in books (not in notes as the Kindle Scribe does). It's more like the Remarkable (without the perfect tactile feel), but in a smaller form factor. Other noteable (fantastic) features are a Pocket-integration and OverDrive support (so one can get books from the library[^1]) So I bought a Kobo Libra Colour.[^2]

The device itself is nice [^3], but that's not the point of this text. The Kobo community is more into hacking, and less into locked systems. This led my to reconsider my main RSS reader over the last few years, [Feedly](https://feedly.com/). It's quite costly for what it does. I pay for [Readwise](https://readwise.io) as well, which originally collects all your highlights across services and exports them to you preferred note taking app [^4]. Now, they also have an extensive Reader app which has RSS support (and read it later support).

This meant I could

1. reduce my cost on this type of software with around 3000 NOK
2. reduce the number of apps I use with 1 

.. which is nice.

(Of course I should've switched over to some of the fantastic open source offers out there, but as I haven't seen/found any realistic Readwise replacements I'd have to stick to it anyway.)

## The challenge

I still wanted to read articles on my Pocket integrated Kobo, and you don't need Pocket Premium if you're not using their "library features" but just read articles.

The issue was that the "sync" between Pocket and Reader was one-way, and the Reader people don't plan to do anything with it.

Of course, I could manually copy-paste links into Pocket. I could. But, you know.[^5]


## Building a little Readwise Reader-Pocket integration
So, I needed to build my own little integration. Thankfuly the services have public APIs, whoo!

1. [Readwise has an API](https://readwise.io/reader_api) to fetch their articles (and add articles)
2. [Pocket has an API](https://getpocket.com/developer/) that lets you create, read and change articles


There's noe queue/triggering capabilites in the Reader APIs, so a scheduled check would have to do. For simple IFTTT-tasks I've used Zapier for a couple of years. Their no code features work well for most things, while they also support code.

So, I wrote some code and ended up with the following 

1. When I add articles to "later" in Reader they are also saved to Pocket
2. When articles are archived in Reader, they are also archived in Pocket

This is triggered every hour. The code is [here](https://gist.github.com/essoen/5fddb415b531ad91759fbb2590b8927b). The code step in Zapier is restricted so it cannot be shared as a template, but here's a picture:

![graphic representation of Zap that handles data push from Readwise to Pocket and vice versa](/2024/readwise-pocket-zap.png)


Worth noting that the loop step will complain when given an empty list. [^5]

It's good to still be able to do some coding, although the code craftsmanship certainly isn't what it is. You improve the most on the things you do, I guess.


## What's missing

Obviously I want archived Pocket-articles to be archived in Reader. That's not currently possible, as Reader doesn't offer an API to change articles. So, that's manual.

Also, the orignal use case for Readwise (not Reader) was to collect highlights, so they have a Pocket integration. This is now causing  I am talking with the devs about all this, hopefully they can do small improvemenets on their API so my litte integration can improve.


## So what?
It's nice to have a few weeks off in the summer, and have time to do some tinkering. Maybe my Reader-Pocket solution is useful to you? Or someone.

[^1]: This only works for english language books in Norway. For norwegian books we have to use BookBites, which replaced Allbok last year. Allbok supported Adobe Digital Editions export so one could transfer burrowed books to an ereader over cable. Bookbites doesn't have that, so there you'll have to read on a regular tablet or get an Android eink tablet. I've also considered that, but I was put off by the fact that the most recent Android version offered on Boox devices (main actor in the business) was Android 12. 
[^2]: I really enjoy ereaders.
[^3]: But the Kindle Oasis is still the best ereader I've used (despite the micro-USB port)
[^4]: Obisdian is my preferred app for this right now, and I try to get all my notes to end up here. I still have a few things in Notion, overviews and such. Their tables are nice, their GDPR compliance not so much. Tradeoffs. 
[^5]: [Whaddya gonna do?](https://www.youtube.com/watch?v=GLrdrC1H6ZY)