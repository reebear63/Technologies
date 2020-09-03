# Agile Mindset #

## Introduction to Agile ##
- Clarity of Requirements and Familiarity with Technology drive the "Uncertainty Level" of projects (-> Cynefin)
  - Cone of Uncertainty
  - Cynefin

- Traditional Approach
  Requirements -> Architecture -> Programming -> Testing -> Fixing
  - assumes correct requirements are known from the start
  - change is risky and costly, so new needs cannot be met
  - hand-offs between groups require work and invite disconnects
  - testing is done towards the end, when fixing defects is more expensive
  - no working software until late in the project => lots of surprises

- Iterations = Repeated Cycles of creating increments
  
- Change Requests - why do they exist?
  - end user is not clear about end result
  - assumptions differ
  - lack of clarity within development team
  - market changes
  - customer expectations change

- Agile vs. Waterfall
  - Predictive Process (Waterfall) = Plan-driven
    - traditional software development are too heavyweight or cumbersome
    - too many things are done which are not directly related to software production (bringing value to the customer)
    - difficulty with incomplete or changing requirements
  - Adaptive Process (Agile) = Value-Driven
    - lightweight process
    - people-based rather than plan-based
    - several Agile methods, XP and Scrum being the most popular
    - no single definition, the Agile Manifesto containing a set of principles comes closest to a definition


## Agile Team ##

## Agile Manifesto ##
- February 11-13, 2001
- **Individuals and interactions** over processes and tools
- **Working software** over comprehensive documentation
- **Customer collaboration** over contract negotiation
- **Responding to change** over following a plan
  

## Scrum Theory ##
- Scrum is founded on **empirical process control** theory, or **empiricism**
- three main pilars: transparency, inspection, and adaption

- Scrum projects make progress in a series of iterations, called **sprints**

**Agile Scrum Process**
- input from customers, team managers, other stakeholders given to **Product Owner**
- list iof requirements, prioritizes by business value => **Product Backlog**
- Sprint Planning Meeting: how much can the team commit to deliver by the end of the sprint
- Sprint Backlog: contains the tasks committed by the team for a sprint
- Sprint: iteration - between 2-4 weeks (constant duration, based on complexity)
- Daily Scrum / Daily Standup
- Sprint Review
- Potentially Shippable Product Increment
- Sprint Retrospective


**Roles**
- Product Owner
  - defines the features of the product
  - decides on the release date and content
  - responsible for the productivity of the product (ROI)
  - prioritizes features according to market value
  - adjusts features and prorities for every iteration, if needed
  - accepts or rejects work results
- 
- Scrum Master
  - servant leader of the team
  - leader, mentor, and coach of Scrum
  - represents management to the project
  - responsible for making sure Scrum values and practices are followed
  - removes impediments
  - ensures the team is fully functional and able to work
  - shields the team from outside interferences

  - moderator of all meetings and ceremonies (?)
  - enabler and team mobilizer
  - stakeholder and communication management
  - continuous improvement (inspect and adapt)
  - process improvement at the systemic level, share best practices, knowledge management
  - improve team velocity/productivity by enabling the team to continuously improve
  - effective implementation of Scrum processes, ceremonies - authority over process
  - tracking and monitoring of sprint(s)
  - sharing best practices between teams
  - process improvements at sprint level and organizational level
  - pay special attention to distributed teams

- Scrum Team
  - Scrum Team consists of Development Team, Product Owner and Scrum Master
  - a self-organized team is key to the project success

- Development Team
  - responsible to implement the product
  - size is 6 (+/- 3 people)
  - bigger projects => multiple dev teams working on a single product backlog
  - cross-functional: dev team has all skills necessary to produce working software 
  - 
**Ceremonies or Events**
- Sprint Planning
  - analyze and evaluate product backlog
  - team selects items from product backlog which they commit to completing
  - select sprint goal
  - create sprint backlog from productk backlog items
  - tasks are identified, if necessary specified in more detail and estimated
  
- Daily Scrum Meeting (32/82)
  - make prorgress, plans, and blockers visible to each other (not the SM!)
  - 15 min timebox
  - PO may attend, but must not interfere
  - SM notes the blockers
  - after Daily Scrum, SM helps remove blockers, team members can meet in smaller groups to discuss issues
  - 
- Sprint Review
  - inspect and adapt the product
  - takes place at the end of the sprint
  - PO, DevTeam, SM, and stakeholders get "hands on" with what the DevTeam produced in the sprint
  
- Sprint Retrospective
  - inspect and adapt the process
  - last activity of each sprint (timebox: 1 hour * no. of weeks per sprint)
  - PO, DevTeam, and SM talk what they have experienced and observed during the sprint
  - create plan of action what to improve next sprint(s)
  - approaches
    - Start - Stop - Continue
  

**Artifacts** (37/82)
- Product Backlog
  - contains the requirements
  - list of all desired work on the project
  - ideally expressed in a way that each item has value to the users or customers
  - prioritized by the PO
  - may be reprioritized at the start of every sprint

- Product Backlog Items (PBI)
  - Scrum does not specify how to write PBIs
  - user stories are a widely used Agile approach to put requirements into PBIs
  - good PBIs are DEEP
    - Detailed appropriately
    - Estimated
    - Emergent (regularly defined)
    - Prioritized
  - User Stories start big, with only the highest-level detail (Epics)
    - over time, the PO and the DevTeam slice Epics into smaller and more detailed stories as they get closer to being implemented
    - slicing and detialing happens during Product Backlog Refinement
    - goal for a user story is to be small enough for 1-2 people could implement in 3-4 days ("1-2-3-4")
    - non-functional requirement have to be included as user stories
    - INVEST (Independent, Negotiable, Valuable, Estimatable, Small, Testable)
    - UINVEST = Understandable + INVEST
    - "As a <person>, I want to <do something>, so that <something happens>"
    - user stories are designed to force a conversation between the DevTeam and the PO
      - this conversation begins at the start of the project
      - conversation continues sprint-by-sprint
      - conversations are documented in the details of the user stories
      - during the conversations, the PO and DevTeam identify confirmations for each User Story
      - DevTeam uses these as a guide to development, and as a way of confirming that the requirements have been met
  
- Sprint Backlog
  - subset of Product Backlog Items which define the work for one sprint
  - selected by DevTeam members
  - team can add or subtract items from the list; PO is not allowed to do it
  
- Burndown Charts
  - Sprint Burndown Chart
    - depicts the total Sprint Backlog Story Points remaining per day
    - shows the estimated amount of time until release
    - ideally should burn down to zero till the end
    - not necessarily a straight line
    - might burn up as well

## Agile Projects ## (50/82)
- Agile development model is also a type of incremental model
- software is developed in incremental, rapid cycles
- small incremental releases with each release building on previous functionality
- each release is thoroughly tested to ensure software quality is maintained

**Definition of Done (DoD)**
- at the end of each sprint, the DevTeam aims to have an increment of the product done, according to the DoD
- Potentially Shippable Product Increment does not mean it HAS to be shipped every sprint
- Anything not "done" (= not finished, has defects, or needs improvement) gets put back to the Product Backlog by the PO and (re-)prioritized

**Product Backlog Refinement**
- DevTeam, PO, and SM take time in each sprint to look at the upcoming Product Backlog Items which will be worked on in the next 2-3 sprints
- take large upcoming PBIs and split them into smaller slices
- get a more detailed shared understanding of the requirements for the upcoming PBIs
- no fixed format, timing, or timebox
- start with a 2-hour session for PO, DevTeam, and SM halfway through the sprint and adapt as necessary

Scrum Events               | Duration per Event       | Frequency  
---------------------------+--------------------------+-------------------  
Sprint Planning Meeting    | about 2 hrs per week     |  once per sprint 
Daily Scrum                |       15 mins            |  daily
Product Backlog Refinement | max. 10% of available    |  once per sprint
                           |     capacity             |
Sprint Review              | about 1 hr per week      |  last day of sprint    
Sprint Retrospective       | about 1 hr per week      |  last day of sprint 

**Deliverables in Agile Projects**
- cost and scope estimates
- prioritized Product Backlog
- Sprint Backlog
- User Stories
- Definition of Done
- Potentially Shippable Product Increment
- Final Delivery

**Agile Team stages**
- Agile Projects are successful through the team performances
- Agile Teams undergo **forming, norming, storming** stages before the start **performing**


## Requirements, Estimation & Planning ## (58/82)
- Agile requirements are logged in Product Backlog, detailed into User Stories
- We use T-Shirt sizing / Planning Poker for estimating

**Requirements**
- Requirements are gathered in the form of a Product Backlog
- Requirements are further detailed in Epics and User Stories
- These User Stories are prioritized based on discussion between customer and team (PO)
- Team agrees on Story Point Definition & Velocity of delivery
  Velocity is the team's capacity to deliver user stories (Story Points) in a sprint
- During Sprint Planning, the team picks up the stories which have been prioritized
  Picking up Stories based on the velocity and focused on what and how to deliver
 
**Scaling Agile Teams** 
- multiple teams working on the same Product Backlog
- Scaling POs
- Scrum of Scrums (2-3 x per week meeting of team representatives to coordinate, manage dependencies, impediments discussion) 

**Tracking and Monitoring Agile Projects**
- Burn-down charts
  
## Tool Overview ## (75/82)
- Definition of Done Checklist
- Sprint Retrospective
- Acceptance Criteria
- Sprint Burndown Chart
- Task Board (Story: New, In Progress, Resolved, Closed)

## References ##
- https://www.mountaingoatsoftware.com/agile/scrum
- https://www.scrumalliance.org
- https://www.youtube.com/watch?v=JaqiXSp-D8E - Agile Estimation and Planning by Sally Elatta
- https://www.youtube.com/watch?v=502ILHjX9EE - Agile Product Ownership in a Nutshell by Henrik Kniberg

=======================================
## Interesting Questions ##
=======================================
Q: What is agile velocity?
* It predicts how much work Agile can complete in sprint planning.
* This is baseline speed of execution of user stories. (wrong)
* Velocity is a metric that is calculated by addition of all efforts estimates associated with user stories completed in an iteration.
* Velocity means count of stories completed.

Q: Agile methods are described as "adaptive" because...
* Agile teams have the empowerment to frequently respond to change and to learn on a project by changing the plan.
* The rate of development progress on an Agile project is constantly tracked to allow adaptation. (wrong)
* Project Managers are not needed in Agile methods because teams are self-organizing.
* Workshops held at the beginning and the end of every iteration (timebox) allow the team to adapt the product specification.

Q: Which of the following is a good example of a barely sufficient user story?
* As a banking customer or maintainer of the system, I should be able to log into the system at all hours of the day from PCs and tablets. (wrong)
* As a banking customer, I can bank.
* As a banking customer, I should have following capabilities: checking, savings, CDs, mortgage loans, loans, bonds, stocks.
* As a banking customer, I can deposit checks using my smart phone.

Q: In an agile pre-mortem retrospective the team tries to anticipate
* what has gone wrong.
* what will definitely go wrong.
* what could go wrong. (wrong)
* waht is wrong.

Q: Sanika is confused about the purpose of a product roadmap. She asks you, her project manager, to identify a benefit of a product roadmap to help her understand a product roadmap's purpose. Select the benefit of a product roadmap.
* Helps facilitate iteration development. (wrong)
* Helps facilitate prioritization of features.
* Helps facilitate reflection meetings.
* Helps facilitate daily stand-up meetings.

Q: When is it appropriate to estimate tasks for an iteration?
* Both during sprint planning and during the sprint itself.
* Only during release planning.
* During the sprint.
* During sprint planning. (wrong)

=======================================
