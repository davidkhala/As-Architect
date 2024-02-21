# Saga pattern
# Definitions

- Wikipedia: The saga interaction pattern are computer database transactions that avoid locks on non-local resources, use compensation to handle failures, potentially aggregate smaller ACID / atomic transactions, and typically use a coordinator to complete or abort the transaction. In contrast to rollback in ACID transactions, compensation restores the original state and is business-specific.
- Wikipedia: a sequence of database transactions grouped to achieve a single atomic result.

Saga provides a reliable basis for the business layer by hiding the imponderabilities of distribution from the business layer.

- With alias as `Long-running transaction` or `Long-lived transaction`, SAGE itself is not a transaction

## Caveats
- [The Saga pattern can only be used to logically roll back transactions due to business errors, but not respond to technical errors.](https://www.ufried.com/blog/limits_of_saga_pattern/)
- If you need the Saga pattern too often, it is a hint for a design smell, please check whether your services are organized around **entities** instead of **use cases/user interactions**
### complexity
> [The saga pattern is difficult to debug and its complexity increases with the number of microservices. The pattern requires a complex programming model that develops and designs compensating transactions for rolling back and undoing changes.](https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-data-persistence/saga-pattern.html)
- [it requires careful coordination and handling of distributed transactions](https://www.linkedin.com/pulse/saga-pattern-distributed-designpattern-pratik-pandey/)
### Performance
The need for inter-service communication and coordination can introduce additional latency and overhead.

The system must handle the increased network traffic
### Consistency
- Concurrency: The SAGA pattern can be susceptible to concurrency issues. This is because multiple sagas may be executing at the same time. You need to take steps to prevent sagas from interfering with each other.