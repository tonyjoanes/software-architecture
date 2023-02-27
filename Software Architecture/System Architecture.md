## Loose Coupling
Making sure services and components are not strongly coupled to each other.
Prevent platform coupling
Services could be multiple technologies such as .NET and Java. Messaging and REST can acheive this as different services can use REST and use different underlying tech.

### Spiderweb
Services calling each other directly and meaning tightly coupled and changes can cause changes to multiple services.

### Directory
Use a directory of services to get URLs for services. Consul.
Or use a gateway or service Mesh for calls to other services. You don't call other services directly this way and changes can be made.

## Stateless
Stateful services store states in memory and can therefore lose state on restarts etc. This is also not scaleable
Scaling out is easy with stateless services.
Load balancers would be used to distribute requests between the instances of the stateless service.
Supports scaleability and redundancy.

## Caching
Bring data closer to its retriever so that it is faster.
Example browser caching a page so that when you goto the page it will load quicker.
Cache engines such as Redis.
Cache should hold data this is frequently access and rarely modified.
Syncing cache and DB can be challenging

In memory cache (C# in memory cache)
- Best performance
- Store complex objects
- Easy to use
Distributed cache (redis, installed as services, easier to keep other services in sync)
- Distribution among servers
- Failover capability
- Large storage
- Requires more setup, training and management.

## Messaging
Communication between different services within a system.
Asynchronous communication
Good for long running operations
Feedback and Reliability is a consideration, how do you deal with failures. Poison queues etc.
Complex

### REST API is a messaging method. Request - Response
- Easy and wellknown
- Fast
- Direct connection
- Message size restricted by HTTP protocol limitations
- .NET has Web API, Python has Flask and Fast API etc
### HTTP Push Notifications
- Subscribe and notify
- SignalR or Web Sockets
- Performance is excellent
- Bi directional communication
- Useful for chats where lots of clients need to be aware of updates
- Message size is limited
- Operates on a fire and forget mode so failures hard to deal with
- Chat and Monitoring Applications
### Queue
- Producer places a message on a queue
- Consumer pulls message from a queue
- Performance is not great, queue adds latency
- Performance worse when also using database in combination
- Reliable in that we know message was set. It is a handoff
- Down to the otherside to consume
- Requires training and setup for developers and infrastructure
### File based and Database
- Message places in a folder or a record in the database
- Consumer polls file location or table with messages
- Hard to use multiple instaces as they could poll and pickup same record to process it
- If polling is required then a queue is the best method

## Logging & Monitoring
Unify the logging across all services, format and location
Use identification of logs to know the team, service that the log came from
Use tools for collecting and visualisation of logs.
Implement correlation ids so that you can trace an event through multiple services