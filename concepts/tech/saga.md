
# Definitions
Alias: Long-running transaction | Long-lived transaction
- Wikipedia: The saga interaction pattern are computer database transactions that avoid locks on non-local resources, use compensation to handle failures, potentially aggregate smaller ACID / atomic transactions, and typically use a coordinator to complete or abort the transaction. In contrast to rollback in ACID transactions, compensation restores the original state and is business-specific.
- Wikipediap: a sequence of database transactions grouped to achieve a single atomic result.

## Frameworks
### OASIS Business Transaction Processing and WS-CAF
These protocols use a coordinator to mediate the successful completion or use of compensation in a long-running transaction.??


## Drawback
It creates challenges of concurrency control and scalability.
