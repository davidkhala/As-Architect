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
### Queue-Based Load Leveling Pattern
### Competing Consumer Pattern
## Data Handling
