---
title: 'Book notes on "Rethinking Agile: Why Agile Teams Have Nothing To Do With Business
  Agility"'
date: 2022-07-26T12:00:39+02:00
description: 'Notes on the book Rethinking Agile: Why Agile Teams Have Nothing To
  Do With Business Agility'
tags:
- books
- agile
draft: true

---
# Book notes on Rethinking Agile

I recently read the book [Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility](\[https://www.amazon.com/Rethinking-Agile-Nothing-Business-Agility/dp/3903205397), and many of the ideas and concepts resonated with me. Usually, I take notes in a Miro-board, but this time I also want to share some notes here, as it might be useful to others.

## Part 1: The Problem

The book takes a look at a company that goes through an Agile Transition. The IT organization had 600 people. The organization wants the transition for the usual reasons:

1. Optimized Time to Market
2. Increase customer feedback
3. Become "ready for the future", i.e. enable the IT organization to utilize new technology

They plan their agile transition around the following practices, over a time-frame of 18 months:

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

They did not have the measurements from before the transition, but they did had a measure of project cycle time. The project cycle time had gone down after the transition, so 

## Part 2: Causes

The book describes four causes of the problem, each in its own section. He uses the example from the first part  explain these four causes. Here's a brief summary of each:

1. **The pitfall of simplistic inference in the change process:** When companies want optimized Time-To-Market (TTM) and faster customer feedback, they tend to believe that agile is a concrete step to reach that goal. So they introduce a big agile transformation project. They reorganize, introduce new roles, and describe what these roles are allowed to do. Leopold argues that this will draw focus to roles, responsibilities, and processes, rather than how to actually increase TTM and customer feedback. They confuse _"means for the purpose"_. He also notes that your organizational model does not make you agile either. not. _"Success depends on answering one question: How do we make our money and which problem are we trying to solve?"\[^1\]
2. **Dealing with dependencies between Teams and Products:** After discovering that management has a simplistic understanding of agile, and the need for it, Leopold explains that he usually visits the teams. He often discovers that they have Kanban boards as required by the organization's chosen framework. In these boards, he found columns that are called "External waiting", i.e. the team has dependencies on other teams. He visualized this with a dependency graph. Dependencies lead to increased cycle times. The reason for this external wait time is, according to Leopold, that one forgets that: (1) Even though a team usually only works on one product, several teams are working on the same product. (2) Even though one team only works on one product, there are dependencies between products (3) Knowledge work has a tendency to create dependencies, and one has to be extremely cautious. He quotes Russel L. Ackoff _"\[..\] the performance of the whole is never the sum of the parts taken separately, but it's the product of their interactions."_  Leopold ends with: _"Agility is created when the interactions between teams are agile. That was the problem in this company: The interactions between the individual teams were not being managed."_ \[^3\]
3. **An incomplete value stream:** Many big and difficult steps ahead of the development, slows down development, such as idea selection, business case writeup, and steering committee approval. Leopold also observes that the burden of becoming faster falls on the development teams nevertheless. "_And business agility will never be achieved if all of the slow-moving process and system logic is simply maintained without consideration for the end-to-end system."_ \[^4\]
4. **WIP Limits at the wrong place:** Leopold separates Work in Progress from Work in Process. In Progress means it's actively worked on, while In Process means that it's in the system but without real progress. To increase the organization's ability to deliver, the Flow Efficiency (how much time a work item spends in being actively worked on vs. in process), must reduce how much things are ongoing at the same time rather than the active work. _"If an organization wants to become faster, the primary focus should not be on optimizing the active work. That is exactly the problem with many efficiency programs: They focus solely on the active work and want to make it faster. Let's assume a flow efficiency of ten percent, and you drive the people to work twice as fast. You can still only gain a maximum of five percent in system performance because 90 percent of the time, the work is inactive. Attempting to improve individual performance doesn't move us forward. It makes more sense to focus on the system and work on improving the performance there."\[^2\]

## Part 3: Flight Levels

Klaus argues that to achieve visibility and coordination as to mitigate the problem and causes, one must establish visibility and coordination arenas at three levels:

1. Operational Level
2. Co-ordinational Level
3. Strategic Portfolio Management

Every organization is different, but I'd translate this to:

1. Implementational level, e.g. development teams
2. Middle management, i.e. leaders of various business areas
3. Executive level, i.e. the leaders responsible for setting the course and deciding on the future of the company as a whole

My experience is that most organizations would implement agility in the teams, while not on the other business areas. tjhi

> Business agility doesn't work if an organization is comprised of agile islands while the logic of the surrounding processes remains the same and certain groups exempt themselves from practicing agility.
> _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._

> The decision to "work without a hierarchy" has to be decided by someone—presumably it isn't the building maintenance person making this decision.
>
> _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._

\[^1\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 41). LEANability PRESS. Kindle Edition.

\[^2\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 64). LEANability PRESS. Kindle Edition.

\[^3\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 51). LEANability PRESS. Kindle Edition.

\[^4\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 56). LEANability PRESS. Kindle Edition.