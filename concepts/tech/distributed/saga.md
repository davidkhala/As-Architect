# Saga pattern

Saga provides a reliable basis for the business layer by hiding the imponderabilities of distribution from the business layer.
- Wikipedia: The saga interaction pattern are computer database transactions that avoid locks on non-local resources, use compensation to handle failures, potentially aggregate smaller ACID / atomic transactions, and typically use a coordinator to complete or abort the transaction. In contrast to rollback in ACID transactions, compensation restores the original state and is business-specific.
- [Microsoft](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga): A saga is a sequence of transactions that updates each service and publishes a message or event to trigger the next transaction step. 
- [Microsoft] Each local transaction updates the database and publishes a message or event to trigger the next local transaction in the saga. If a local transaction fails, the saga executes a series of compensating transactions that undo the changes that were made by the preceding local transactions.
- With alias as `Long-running transaction` or `Long-lived transaction`, SAGE itself is not a transaction

## Pivot transaction 
A pivot transaction is the go/no-go point in a saga. If the pivot transaction commits, the saga runs until completion. 
- A pivot transaction can be a transaction that is neither compensable nor retryable
- A pivot transaction can be the last compensable transaction or the first retryable transaction in the saga.

## Retryable transaction
Retryable transactions are transactions that follow the pivot transaction and are guaranteed to succeed.

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