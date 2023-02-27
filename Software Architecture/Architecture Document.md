Arc42 https://arc42.org/overview

Described what should be developed and how.
Lay out the requirements and the non functional requirements

Audience:
- CTO
	- Ensure the project is in good hands
	- Requirements reflect the system
	- Architecture is geared towards business goals
- Project Manager
- Developers
- QA Testers
	- What test tools are required
	- Test strategy
	- Risk assessment

Management sections in document can go at the beginning to save them time and keep things together.

## Format of Document

UML - modelling language
- Not everyone will be familar with UML
- Requires time for explaining

Keep the document as simple as possible

## Structure

**Background**
Short section and target audience is all the team **and** management.
If replacing another system explain why the need.
Use some metrics and numbers, how will it improve.
Validate your point of view on the system.
This section is important as the rest of the document is built from it.
Keep technical terms out of this section

**Requirements**
Describe the requirements for the system. Include NFR.
Keep it brief, there are problem another requirements system to reference.
Try to keep 3 lines per requirement.
Include them so that it allows the readers the chance to comment and validate the requirements

First functional requirements
Second functional requirements and be accurate and specific with them
examples:
1. The system will have 150 users, with expected load of 20 concurrent users
2. On day one the system will have 150GB migrated from the old system and be expected to grow 400GB annually
3. SLA: The system is allowed a downtime of 5 days annually (planned and unplanned combined)


**Executive Summary**
Audience is management. Present the design at a high level and easy to understand.
It will reiterate the overview and requirements.
It needs to be more business oriented in this section.
Provide a high level overview of the architecture.

- Use charts and diagrams
- Write this at the end after the rest of the document
- Use well known technical terms

**Architecture Overview**
This is likely a long section.
Present the architecture to the team and the structure

*General Description*
Type: Web based, Microservices etc

*High Level Diagram*
Charts and diagrams with interactions between the varios parts of the system
Logic diagram only, no need to describe hardware such as servers

*Diagram Walkthrough*
describe variuos parts and their roles in the system
Inclde relevant details

*Technology Stack*
If there is one underlying stack then it can be described here otherwise you will document it for each component that makes up the system.

**Components Drill Down**
Audience is the development team. Sometimes management might want to read this section.
For each component breakdown as such
1. Role
	- What does the component do
	- What are its boundaries
2. Tech
	- Discuss decisions and why you chose technology
	- Explain pros and cons and then decision
	- Describe the layers
3. Component architecture
4. Developer instructions

Be as details as possible to reduce questions.
