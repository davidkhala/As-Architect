# Being distributed
## Retry Pattern: solution for transient unavailability of failure of a component
Scenario
- Request for configuration / init information
- Request for login

Implement
- Timeout logic
- Retry logic: finite vs infinite (max times)
- Back-off / anti-flood parameters (DDoS), e.g. exponential growing timeout interval
## Idempotent Processor Pattern: solution for receiving duplicate data
Scenario
- New order submission

Implement
- sequence # / unique id
- Other duplicate detection and suppression. e.g. hash(all fields + current timestamp)
- Retransmit flag inspection (重传标志检查), powered by Solace
## Pub-Sub Pattern: solution for sending to unknown n-consumers
Scenario
- Catalogue update
- Status, Heartbeat

Implement
- Decoupling via intermediate component (Middleware)
- by data, e.g. event/topic/channel

# Being Scalable
## Async Request-Reply Pattern: solution for blocked waiting on a slower service
- [A MEP](./MEP.md#pattern-request-reply)

Scenario
- Acceptance confirmation

Implement
- Async & parallel vs sequential & sync
- Trace outstanding requests / defer execution
- Timeout -> Retry -> Cancel / rollback (combined with idempotent and transactional pattern)
## Queue-Based Load Leveling Pattern: solution for handling bursty traffic

Implement
- communication is async
- But finally the queue will also be filled up, then -> Competing Consumers Pattern
## Competing Consumer Pattern
![image](https://github.com/davidkhala/As-Architect/assets/7227589/c5d855de-55f8-44da-8190-e5cd04b537a1)

Implement
- Event trigger to scale more consumer/workers
- Each task should be independently


