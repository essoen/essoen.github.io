---
title: Leverage waiting
description: A short post on how a development team can change their apporach
  and thinking when they fell all deliveries are blocked by other, especially if
  they're blocked by third parties.
draft: false
date: 2025-04-21T15:31:10.276Z
---

The last 6 months I have  experienced a lot of waiting in one of the teams I'm working with. We've been blocked on deliveries, by either third parties or other teams. Blocked means being unable to move forward as desired. This could things such as some API or software someone else has to develop, or testing on some physical hardware that is not available.

Being blocked has forced us to reflect and evaluate our approach. Of course we  must maintain pressure on those we wait for. This can be done by:

- reach out regularly, and use tickler files to make sure we remember to do so 
- asking for timelines as a means to be able to time things for yourself
- escalating to others internally, who talks with others with the third party

It's evident though that this work, even though necessary in many contexts, are not valuable it itself. It's waiting for someone else, and reminding/pushing them.  

Our approach is to do those things, but mostly focus on what we can do of valuable work while we wait. What could that be?

- identify parts that can be built independent of the dependency, i.e. build a happy path first
- handle the dependency by mocking or other techniques
- prepare for things we know we'll have to do later. 
- move on to other things, without dependencies, and rework your goals and roadmap

It's an awareness thing. We all know we're blocked, but we can leverage the waiting time for something useful and valuable.