# Saga pattern
# Definitions
Alias: Long-running transaction | Long-lived transaction
- Wikipedia: The saga interaction pattern are computer database transactions that avoid locks on non-local resources, use compensation to handle failures, potentially aggregate smaller ACID / atomic transactions, and typically use a coordinator to complete or abort the transaction. In contrast to rollback in ACID transactions, compensation restores the original state and is business-specific.
- Wikipedia: a sequence of database transactions grouped to achieve a single atomic result.

Saga provides a reliable basis for the business layer by hiding the imponderabilities of distribution from the business layer.

## Frameworks
### OASIS Business Transaction Processing and WS-CAF
These protocols use a coordinator to mediate the successful completion or use of compensation in a long-running transaction.??


## Caveats
- [The Saga pattern can only be used to logically roll back transactions due to business errors, but not respond to technical errors.](https://www.ufried.com/blog/limits_of_saga_pattern/)
- concurrency control
- scalability??
- Additional coordinator like 2pc
