# Dead Letter Queue(DLQ)
a service implementation to store messages that meet one or more of the following criteria:
1. Message that is sent to a queue that does not exist.
2. Queue length limit exceeded.
3. Message length limit exceeded.
4. Message is rejected by another queue exchange.
5. Message reaches a threshold read counter number, because it is not consumed. Sometimes this is called a "back out queue". (read without callback)
6. The message expires due to per-message [TTL (time to live)](https://en.wikipedia.org/wiki/Time_to_live)
7. Message is not processed successfully.(read, then callback about the failure result)
## Use case
Use DQL when
- Along with standard queue. You should always use DLQ when your application don't depend on ordering.
- decrease the number of messages by reduce the possibility of exposing your system to **poison-pill messages** (messages that can be received but can't be processed)

Don't user DLQ when
- keep retrying the transmission of a message indefinitely.(失败消息重回队列)
- you don't want to break the exact order of messages in FIFO queue.

