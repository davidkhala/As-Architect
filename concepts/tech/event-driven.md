# Event Driven
It is time to stop technical only brain.
![image](https://github.com/davidkhala/mq/assets/7227589/cfd6a9e2-bc80-44ac-ab39-d93df16856fc)
"A key distinction of a digital business is that it's a **event-centric**, which means it's always **sensing**, always **ready** and always **learning**" ---- Gartner

Technology goals for event driven is to deliver better customer experience.
# Design
## Being distributed:
### Retry Pattern: solution for transient unavailability of failure of a component
Scenario
- Request for configuration / init information
- Request for login

Implement
- Timeout logic
- Retry logic: finite vs infinite (max times)
- Back-off / anti-flood parameters (DDoS), e.g. exponential growing timeout interval
### Idempotent Processor Pattern: solution for receiving duplicate data
Scenario
- New order submission

Implement
- sequence # / unique id
- Other duplicate detection and suppression. e.g. hash(all fields + current timestamp)
- Retransmit flag inspection (重传标志检查), powered by Solace
### Pub-Sub Pattern: solution for sending to unknown n-consumers
Scenario
- Catalogue update
- Status, Heartbeat

Implement
- Decoupling via intermediate component (Middleware)
- by data, e.g. event/topic/channel
## Being Scalable
### Async Request-Reply Pattern: solution for blocked waiting on a slower service
- [A MEP](https://github.com/davidkhala/As-Architect/blob/main/concepts/tech/MEP.md#pattern-request-reply)

Scenario
- Acceptance confirmation

Implement
- Async & parallel vs sequential & sync
- Trace outstanding requests / defer execution
- Timeout -> Retry -> Cancel / rollback (combined with idempotent and transactional pattern)
### Queue-Based Load Leveling Pattern: solution for handling bursty traffic

Implement
- communication is async
- But finally the queue will also be filled up, then -> Competing Consumers Pattern
### Competing Consumer Pattern
![image](https://github.com/davidkhala/As-Architect/assets/7227589/c5d855de-55f8-44da-8190-e5cd04b537a1)

Implement
- Event trigger to scale more consumer/workers
- Each task should be independently
## Data Handling
### Eventual Consistency Pattern: solution for keeping multiple data replicas sync

Implement
- Relaxation of Consistency in CAP theorem
- Guaranteed delivery of data update evantualy to all replicas, powerd by queue, make data update as a topic to publish, and write back to data replica from consumer
### Sharding Pattern: solution for db scale is limited
Scenario
- Server hosting customer details db is bandwidth limited

Implement
- DB access logic can compute correct Shard to access based on stable data fields
- 分库分表

### Command & Query Responsibility Segregation (CQRS, 读写分离) Pattern: solution for Imbalanced read vs write db operations
Scenario
- queries are requiring complex views, impacting on the command operations

Implement
- Maintain differnet Command DB and Query DB
- Guaranteed delivery of Command DB to the Query DB to keep it in sync to changes. Combine Eventual Consistency Pattern
