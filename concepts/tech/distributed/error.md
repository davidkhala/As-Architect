# Technical errors in distributed systems
Solutions
- [2 phase commit](./2pc.md)
- You must make sure that you do not lose the pending changes before you can complete them
  - pending change be cached outside the place where we finally want to persist it
  - assume: the system will eventually recover from the error. And the pending change can be applied
- Solution for inconsistent database: event sourcing combined with snapshots
  - You replace the broken parts of the system, reload the latest snapshot and then replay all events that occurred after the snapshot
  - assume: this requires idempotent event processing to work reliably.