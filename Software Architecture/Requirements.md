## There are two types of requirements

### System Requirements

- What the system should do

### Non Functional Requirements - what the system should deal with

The main types of requirements:

- Performance
   - Always talk in numbers (what is fast?)
      - Latency and throughput
		- Latency - How much time does it take to perform a single task
		- Throughput - How many tasks can be performed in a given time
		- **Talk to the client!**
  - Load
	- Quantity of work the system can stand without crashing
	  - eg how many concurrent requests can the web API take
	  - 500 requests without crashing
- Data Volume
  - How much data will the system accumulate over time
	- Decide on db type
	- How will it be queried
	  - What will the expected growth be
- Concurrent users
  - How many users will use the system concurrently (at the same time)
  - SLA

### Defining the NFR

Who should define them. Architect needs to frame the requirements and the boundaries for the project manager / product owner.

As an architect you need to help define the NFR's

> Never design a system without any NFR's!!!!!!

