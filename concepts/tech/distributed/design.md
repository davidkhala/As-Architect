# Data Handling
> Don’t match REST resources to database entities. That’s just wrong.
## Eventual Consistency Pattern: solution for keeping multiple data replicas sync

Implement
- Relaxation of Consistency in CAP theorem
- Guaranteed delivery of data update evantualy to all replicas, powerd by queue, make data update as a topic to publish, and write back to data replica from consumer
## Sharding Pattern: solution for db scale is limited
Scenario
- Server hosting customer details db is bandwidth limited

Implement
- DB access logic can compute correct Shard to access based on stable data fields
- 分库分表

## Command & Query Responsibility Segregation (CQRS, 读写分离) Pattern: solution for Imbalanced read vs write db operations
Scenario
- queries are requiring complex views, impacting on the command operations

Implement
- Maintain differnet Command DB and Query DB
- Guaranteed delivery of Command DB to the Query DB to keep it in sync to changes. Combine Eventual Consistency Pattern