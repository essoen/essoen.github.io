+++
date = 2023-03-08T10:13:16Z
description = ""
draft = true
tags = ["organizational design"]
title = "Enabling teams vs. platform teams"

+++
Lately, I've felt the need to clarify the distinction between enabling and platform teams in the book ["Team Topologies: Organizing Business and Technology Teams for Fast Flow"](https://www.amazon.com/Team-Topologies-Organizing-Business-Technology/dp/1942788819). The reason for this, is that platform teams often must consult on more than what their platform is dedicated to do. That might not be the best for that team, but it might be what the organization needs. HOw can we address that need directly?

## Definitions of enabling and platform teams

First, look at the enabling team:

> The primary purpose of an enabling team is to **help stream-aligned teams deliver working software in a sustainable, responsible way.** Enabling teams do not exist to fix problems that arise from poor practices, poor prioritization choices, or poor code quality within stream-aligned teams. **Stream-aligned teams should expect to work with enabling teams only for short periods of time (weeks or months)** in order to increase their capabilities around a new technology, concept, or approach. **After the new skills and understanding have been embedded in the stream-aligned team, the enabling team will stop daily interaction with the stream-aligned team, switching their focus to a different team.**  
> _- Skelton, Matthew; Pais, Manuel. Team Topologies (p. 113). IT Revolution Press. Kindle Edition._

What's the role of the platform team?

> The platform team provides internal services to reduce the cognitive load that would be required from stream-aligned teams to develop these underlying services.  
> _\[..\]  
> _In practice, platform teams are expected to focus on providing a smaller number of services of acceptable quality rather than a large number of services with many resilience and quality problems.
>
> _- Skelton, Matthew; Pais, Manuel. Team Topologies (pp. 115-116). IT Revolution Press. Kindle Editio_

So, the enabling team offers competence and guidance. The platform teams offer services.

The authors refer to the Jutta Eckstein article from 2014, ["Architecture in Large Scale Agile Development"](https://link.springer.com/chapter/10.1007/978-3-319-14358-3_3). It offers us this figure showing various ways of handling architecture needs:

![Figure 2 from Eckstein 2014](/2023/eckstein2014.jpg)

The platform team works in organization where the teams want to make many changes, and the degree of uncertainty is high. They are technical service teams, offering a platform of internal services that enable many changes.

The enabling teams work in areas where there are fewer changes and less uncertainty. So, they can consult on ways forward. 

Nevertheless, many teams would need help with

1. Deciding if the platform is for them
2. If not, what else should they use
3. Help on how to use the platform

Does this mean there should be a dedicated enabling team consulting on this behavior?

## A consulting platform team

I do not believe that this means platform teams cannot consult. They need to talk to their users to define needs and improve their platform. They must collaborate with their users.

> What kind of behaviors and outcomes do we expect to see in an effective platform team? ​
>
> * A platform team uses **strong collaboration with stream-aligned teams** to understand their needs. 
> * A platform team relies on **fast prototyping techniques and involves stream-aligned team members for fast feedback** on what works and what does not. ​
> * A platform team has a strong focus on usability and reliability for their services (treating the platform as a product), and r**egularly assesses if the services are still fit for purpose and usable.** 
> * ​A platform team leads by example: using the services they provide internally (when applicable), partnering with stream-aligned teams and enabling teams, and consuming lower level platforms (owned by other platform teams) whenever possible. ​
> * A platform team understands that adoption of internal new services, like new technologies, is not immediate, but instead evolves along an adoption curve.
>
> Skelton, Matthew; Pais, Manuel. Team Topologies (pp. 117-118). IT Revolution Press. Kindle Edition.

So, they will interact with and help the team. What they won't do, is help a team over time.  
They might point the stream-aligned team in another direction, after realizing their platform isn't fit for this use case. Who might the stream-aligned team get help from then? 

Well, someone who knows what they need help with. In the case of "architecture", the people on the platform team consist of those with the most competence. As well as cloud services. So, they might point away from their team, but nevertheless, the "need" will come back to them.

To handle this, here are a few practices that might work, based on the number of people you have in your platform team, and the need for consulting around your organization:

1. Create a dedicated enabling team for consulting on the platform, where the people might be in multiple teams (i.e. platform team and one enabling)
2. Dedicate a few people on the platform team to consult, and rotate who does it
3. Establish routines for handling this in your community of practice, i.e. asking for consulting over time from specific people through your Community of Practice

This means that members of the platform team will do broader consulting, and that's okay. But the platform team must focus on internal services. So, if the consulting activities take up too much time, you'll see fewer results in the platform team. THat should start a conversation on where we put our resources. 