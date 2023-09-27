---
title: 'Summary of "Rethinking Agile: Why Agile Teams Have Nothing To Do With
  Business Agility"'
description: 'Personal notes on, and summary of, the book "Rethinking Agile: Why
  Agile Teams Have Nothing To Do With Business Agility"'
draft: false
tags:
  - books
  - agile
date: 2022-07-26T12:00:39+02:00
---
_Updated September 27 2023_

I recently read the book [Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility](\[https://www.amazon.com/Rethinking-Agile-Nothing-Business-Agility/dp/3903205397). I found it useful, and many of the ideas and concepts resonated with me. Usually, I take notes in a Miro-board while I read, but this time I also want to share some notes here, as it might be useful to others. Please note that these are my own notes, so it might be things that I've missed, or left out. Please reach out if you want to discuss the book and concepts further, or have questions as to why something isn't mentioned. Thanks!

## Part 1: The Problem

The book takes a look at a company that goes through an Agile Transition. The IT organization had 600 people. The organization wants the transition for the usual reasons:

1. Optimized Time to Market
2. Increase customer feedback
3. Become "ready for the future", i.e. enable the IT organization to utilize new technology

They plan their agile transition around the following practices, over a time frame of 18 months:

1. All teams should be cross-functional
2. Every team should be organized around the premise "one team, one product"
3. There were the following minimum requirements for the agile process:
   1. Work should be visually managed
   2. Every team should have daily Standups and regular Retrospectives
   3. They took the following measurements as reference points:
      1. Throughout, i.e. the number of work items that are completed per time frame
      2. Cycle time to indicate how fast work is completed

The practices were implemented with training, reorganization through self-organization, and external support. Even though the mood was great and 80% of the teams had implemented the minimum requirements of practices, the measurements was not developing as expected:

> Nonetheless, the actual trend of the Scrum teams looked completely different. The teams managed to get off to a good start and velocity increased sharply. Then all of a sudden, the line flattened out and was now in a downward trend. The performance had strongly diminished over time.
>
> \[..\]
>
> As expected, the cycle time increased slightly at the beginning but only marginally decreased over time. The line followed a downward trend, but the improvement did not even reach the 1 percent mark—a cycle time reduced by half was nowhere to be found.  
> Regardless, whether Scrum or Kanban—it was clear that ability of the teams to deliver had not changed much.
>
> Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (pp. 24-27). LEANability PRESS. Kindle Edition.

They did not have the measurements from before the transition, but they did have a measure of project cycle time. The project cycle time had gone down after the transition, which meant that the company went from bad to worse and did not meet its goals. Why?

## Part 2: Causes

The book describes four causes of the problem, each in its own section. He uses the example from the first part to explain these four causes. Here's a brief summary of each:

1. **The pitfall of simplistic inference in the change process:** The company wanted to optimize Time-To-Market (TTM) and faster customer feedback, and believes that agile is a concrete step to reach that goal. So they introduced a big agile transformation project. They reorganize, introduce new roles, and describe what these roles are allowed to do. This drew focus to roles, responsibilities, and processes, rather than how to actually increase TTM and customer feedback. They confuse _"means for the purpose"_. He also notes that your organizational model does not make you agile either. not. _"Success depends on answering one question: How do we make our money and which problem are we trying to solve?"_ [^1]
2. **Dealing with dependencies between Teams and Products:** The teams had Kanban boards as required by the organization's chosen framework. In these boards, Leopold found columns that are called "External waiting", i.e. the team has dependencies on other teams. He visualized this with a dependency graph. Dependencies lead to increased cycle times. The reason for this external wait time is, according to Leopold, that one forgets that: (1) Even though a team usually only works on one product, several teams are working on the same product. (2) Even though one team only works on one product, there are dependencies between products (3) Knowledge work has a tendency to create dependencies, and one has to be extremely cautious. He quotes Russel L. Ackoff _"\[..\] the performance of the whole is never the sum of the parts taken separately, but it's the product of their interactions."_  Leopold ends with: _"Agility is created when the interactions between teams are agile. That was the problem in this company: The interactions between the individual teams were not being managed."_ [^2]
3. **An incomplete value stream:** Many big and difficult steps ahead of the development, slows down development, such as idea selection, business case writeup, and steering committee approval. Leopold also observes that the burden of becoming faster falls on the development teams nevertheless. "_And business agility will never be achieved if all of the slow-moving process and system logic is simply maintained without consideration for the end-to-end system."_ [^3]
4. **WIP Limits at the wrong place:** Leopold separates Work in Progress from Work in Process. In Progress means it's actively worked on, while In Process means that it's in the system but without real progress. To increase the organization's ability to deliver, the Flow Efficiency (how much time a work item spends in being actively worked on vs. in process), must reduce how much things are ongoing at the same time rather than the active work. To increase this, **one must reduce the number of initiatives going at the same time**, so that the most important initiatives are in _progress_, and tasks do not have to wait.


**Addition in September 2023:** The [Fligt Levels Academy Introduction](https://www.flightlevels.io/workshops/flight-levels-introduction/) summarizes the causes like this:

1. No agile interactions
2. No end to end flow (of work) 
3. No agile portfolio management
4. No agile change process

## Part 3: Flight Levels

To enact the WIP limits for initiatives, and increase the project visibility and coordination to mitigate the problem and causes, the organization and establish artifacts and meetings at three levels:

1. **Operational Level, i.e. implementation level:** This is where the transition had focused so far, having a Kanban board and meetings within the team. The focus is on breaking down initiatives into tasks and delivering them.
2. **Co-ordinational Level:** To optimize team interactions so that the prioritised initiatives are completed. The focus is to break the initiatives into pieces so that they can be worked on by teams, and to make sure that dependencies are handled.
3. **Strategic Portfolio Management Level:** Here you want an overview of everything that's happening, how it's going, and what to do next. Does the organization complete the initiatives, and are they aligned with the current company strategy? The focus is to set direction and prioritize.

Start your transition at the highest possible flight level In this organization, that was at level 2. Lead by example. 

### Make dependencies visible and manage them

At each level, you'll want a board that shows what's going on, and relevant people involved in relevant and well-organized meetings. Given that we already have the team-level boards:

1. Send team delegates to set up product boards (can be used by individual teams as well)
2. Define the optimal amount of work for the product/set of teams
3. Run product standup meetings with team delegates (could be in rotation)
4. Run replenishment meetings across teams when stuff is actually done
5. Establish feedback loops across teams, such as having cross-team retros
6. Get metrics for your feedback loops

**Too many meetings?** We might not need all the old meetings, and everyone does not need to participate in everything.

### Integrate the upstream

The upstream is the number of steps from the idea to when the developers can start working on that idea. If the steps take a lot of time, TTM is higher than necessary. We want to integrate the steps, processes, and people in the flight level system to increase TTM.

> The question isn't how many steps are part of the upstream value stream, but instead how quickly these steps—from the first step to an assessable unit of value (idea, concept, etc.)—are able to be executed. - _Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 119). LEANability PRESS. Kindle Edition._

Leopold describes three time traps in the upstream processes: 

1. The annual budget created batch sizes that were too large, i.e. what's committed in the budget is more than the teams can deliver. If what's to be built is decided a year ahead, agility is not pssobløe The longer one collects ideas, the lower the possibility of agility. To increase reaction time to market needs, you need a new budgeting process. Leopold suggests a monthly review and possible replenishment of money.
2. Colleagues as suppliers, i.e. if the IT department is considered a supplier that limits the possibility of a positive relationship. This means that we do not have one large process of estimates and approvals like you would see with an external contractor.  
3. Making an estimate for something that must be done anyway, i.e. doing estimates for things that the company is legally bound to do anyway.

In Leopold's example they changed the upstream process to have the following steps:

1. Approx. business case
2. Waiting on approval
3. Reviewing business cases every two weeks. 

Meeting more often for reviewing business cases made the development and business work tighter together. This was also supported by feedback loops:

1. Joint standup meetings and retros
2. Metrics that would give an idea of the total of TTM, not just for development

### Strategic Portfolio Management

Get the executive management on board so that strategy, operations, development, and delivery can work closely together towards a clearly defined goal. This means establishing flight level 3. Leopold recommends the same steps for including upper executive management as for the two other levels:

1. Visualize 
   1. .. by making a strategy board that visualizes everything that's going on, and what's planned. Make one that fits your context. In Leopold's example, they idenfited two types of work with upper management: initiatives (makes money), and investments ("necessary but not urgent projects"). To focus on outcomes and ensure continuous evaluation, there's no "finished" column but "Measuer & Improve success", "Adjust & Improve", "Result Achieved" and "Result not achieved".
   2. .. by making the processes and criteria from idea to implementation explicit
2. Limit the WIP. Find the right WIP limit for your organization. 
3. Establish feedback loops by making sure there's a meeting around the board often enough, and that decision are actually made. Leopold recommends doing a Strategic Portfolio Standup weekly.  Also, run retros and strategy reviews. He recommends running these more often in the beginning and getting a sense of the necessary cadence over time. 

> The specific design of these steps can, must and should look different for every company. And the design can change over time based on the needs of the company and its customers. - _Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 131). LEANability PRESS. Kindle Edition._

## Part 4: The Result

It all ends well, and the organization that's described has the following results:

1. **Reduced time to market**
2. **Strategic alignment**
3. **Greater efficiency**
4. **Focus on outcome over output**
5. **Increased financials:** Increased revenue. Also found that increased time to marked saved "ten Million Euros per year in delay costs.

**How can we do the same?**

1. "Agility begins with the change process", so be an ambassador for agile ideas. Agility does not happen through a two-year plan, but through getting people on board and implementing practices. Lead by example.
2. Focus on goal over method
3. Focus on organizational process and generating value, rather than on the "agile team"
4. Identify flight levels, and get them on board. We won't get the "transformation" further than the management level we have involved
5. Manage and eliminate dependencies (not the other way around)
6. Implement the drivers for lean business at every flight level, that is:
   1. Make work and processes explicit, i.e. [Making Work Visible](https://www.amazon.com/Making-Work-Visible-Exposing-Optimize/dp/1942788150)
   2. Manage WIP
   3. Increase feedback loops
   4. Improve, i.e. use your feedback loops and implement improvements

## Final notes

This was a great summary of both a typical agile transformation, and the causes of why it fails, and it introduces a concrete tool for how to handle organizational visualization of strategy, dependencies, and ongoing initiatives. It fits well with books such as Accelerate, Making Work Visible, Team Topologies,  The Fearless organization, Upstream, and A Seat at the Table.

These quotes stuck with me, but didn't fit directly into the summary:

> Business agility is achieved when delivering value to the customer is optimized. Sooner or later, it becomes clear what needs to change in the organizational structure to support this. _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 102). LEANability PRESS. Kindle Edition._
>
> Business agility doesn't work if an organization is comprised of agile islands while the logic of the surrounding processes remains the same and certain groups exempt themselves from practicing agility. _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._

> The decision to "work without a hierarchy" has to be decided by someone—presumably it isn't the building maintenance person making this decision. _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._
>
>   
> Important meetings should be held frequently People in organizations like to complain about meetings, which is partly due to how they are set up. But I also take a close look at how often important meetings are actually held. Most likely, you will find that the meeting intervals are too long (also making the meetings longer). The decisions made in these meetings lose value because people are forced to make permanent (isolated) decisions in the meantime. - _Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 136). LEANability PRESS. Kindle Edition._

Thanks for reading!

[^1]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 41). LEANability PRESS. Kindle Edition.

[^2]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 51). LEANability PRESS. Kindle Edition.

[^3]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 56). LEANability PRESS. Kindle Edition.