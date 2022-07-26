---
title: 'Summary of "Rethinking Agile: Why Agile Teams Have Nothing To Do With Business
  Agility"'
date: 2022-07-26T12:00:39+02:00
description: 'Notes on the book Rethinking Agile: Why Agile Teams Have Nothing To
  Do With Business Agility'
tags:
- books
- agile
draft: true

---
I recently read the book [Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility](\[https://www.amazon.com/Rethinking-Agile-Nothing-Business-Agility/dp/3903205397), and many of the ideas and concepts resonated with me. Usually, I take notes in a Miro-board, but this time I also want to share some notes here, as it might be useful to others.

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

1. **The pitfall of simplistic inference in the change process:** The company wanted to optimize Time-To-Market (TTM) and faster customer feedback, and believes that agile is a concrete step to reach that goal. So they introduced a big agile transformation project. They reorganize, introduce new roles, and describe what these roles are allowed to do. This drew focus to roles, responsibilities, and processes, rather than how to actually increase TTM and customer feedback. They confuse _"means for the purpose"_. He also notes that your organizational model does not make you agile either. not. _"Success depends on answering one question: How do we make our money and which problem are we trying to solve?"\[^1\]
2. **Dealing with dependencies between Teams and Products:** The teams had Kanban boards as required by the organization's chosen framework. In these boards, Leopold found columns that are called "External waiting", i.e. the team has dependencies on other teams. He visualized this with a dependency graph. Dependencies lead to increased cycle times. The reason for this external wait time is, according to Leopold, that one forgets that: (1) Even though a team usually only works on one product, several teams are working on the same product. (2) Even though one team only works on one product, there are dependencies between products (3) Knowledge work has a tendency to create dependencies, and one has to be extremely cautious. He quotes Russel L. Ackoff _"\[..\] the performance of the whole is never the sum of the parts taken separately, but it's the product of their interactions."_  Leopold ends with: _"Agility is created when the interactions between teams are agile. That was the problem in this company: The interactions between the individual teams were not being managed."_ \[^3\]
3. **An incomplete value stream:** Many big and difficult steps ahead of the development, slows down development, such as idea selection, business case writeup, and steering committee approval. Leopold also observes that the burden of becoming faster falls on the development teams nevertheless. "_And business agility will never be achieved if all of the slow-moving process and system logic is simply maintained without consideration for the end-to-end system."_ \[^4\]
4. **WIP Limits at the wrong place:** Leopold separates Work in Progress from Work in Process. In Progress means it's actively worked on, while In Process means that it's in the system but without real progress. To increase the organization's ability to deliver, the Flow Efficiency (how much time a work item spends in being actively worked on vs. in process), must reduce how much things are ongoing at the same time rather than the active work. To increase this, **one must reduce the number of initiatives going at the same time**, so that the most important initiatives are in _progress_, and tasks do not have to wait.

## Part 3: Flight Levels

To enact the WIP limits for initiatives, and increase the project visibility and coordination to mitigate the problem and causes, the organization and establish artifacts and meetings at three levels:

1. **Operational Level, i.e. implementation level:** This is where the transition had focused so far, having a Kanban board and meetings within the team. The focus is on breaking down initiatives into tasks and delivering them.
2. **Co-ordinational Level:** To optimize team interactions so that the prioritised initiatives are completed. The focus is to break the initiatives into pieces so that they can be worked on by teams, and to make sure that dependencies are handled.
3. **Strategic Portfolio Management Level:** Here you want an overview of everything that's happening, how it's going, and what to do next. Does the organization complete the initiatives, and are they aligned with the current company strategy? The focus is to set direction and prioritize. 

Leopold also suggests three improvements in addition to the flight level system:

1. Make dependencies visible and manage them
2. Integrate the upstream
3. Get the executive management on board so that strategy, operations, development, and delivery can work closely together towards a clearly defined goal.

## Part 4: The Result

It all ends well, they get:

1. **Reduced time to market**
2. **Strategic alignment**
3. **Greater efficiency**
4. **Focus on outcome over output**
5. **Increased financials:** Increased revenue. Also found that increased time to marked saved "ten Million Euros per year in delay costs.

**How can we do the same?**

1. Be an ambassador for agile ideas. Agility does not happen through a two year plan
2. Focus on goal over method
3. Focus on organizational process and generating value, rather than on the "agile team"
4. Identify flight levels, and get them on board. We won't get the "transformation" further than the management level we have involed
5. Manage and eleminitate depdencies (not the other way around)
6. Implement the drivers for lean business at every flight level, that is:
   1. Make work and processes explicit, i.e. [Making Work Visible](https://www.amazon.com/Making-Work-Visible-Exposing-Optimize/dp/1942788150)
   2. Manage WIP
   3. Increase feedback loops
   4. Improve

## Final notes

This was a great summary of both a typical agile transformation, the causes to why it fails, and it introduces a concrete tool for how to handle organizational visualization of strategy, dependencies and ongoing intiative.s 

These quotes from the final part stuck with me:

> Business agility doesn't work if an organization is comprised of agile islands while the logic of the surrounding processes remains the same and certain groups exempt themselves from practicing agility. _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._

> The decision to "work without a hierarchy" has to be decided by someone—presumably it isn't the building maintenance person making this decision.
>
> _- Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 126). LEANability PRESS. Kindle Edition._

\[^1\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 41). LEANability PRESS. Kindle Edition.

\[^2\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 64). LEANability PRESS. Kindle Edition.

\[^3\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 51). LEANability PRESS. Kindle Edition.

\[^4\]: Leopold, Klaus. Rethinking Agile: Why Agile Teams Have Nothing To Do With Business Agility (p. 56). LEANability PRESS. Kindle Edition.