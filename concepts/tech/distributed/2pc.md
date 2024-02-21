# two-phase commit
the two-phase commit (2PC) protocol require all participants in a transaction to commit or roll back before the transaction can proceed.

# Drawback
- some participant implementations, such as NoSQL databases and message brokering, don't support this model.