# Business error
Cases when
- if you try to pay with an expired credit card
- if a pending payment would exceed your credit limit:

# Technical error
Cases when
- if your database does not respond or throws an unexpected technical error (the dreaded “IOException”)
- if a service is down or latent
- if a message is lost or corrupted
- if your replicated and eventually consistent database is out of sync

Technical error will happen for sure, i.e., their probability is bigger than 0.
- You cannot predict when they will occur and how they will manifest.

Solutions
- 2 phase commit (2pc)
- You must make sure that you do not lose the pending changes before you can complete them
  - pending change be cached outside the place where we finally want to persist it
  - assume: the system will eventually recover from the error. And the pending change can be applied
- Solution for inconsistent database: event sourcing combined with snapshots
  - You replace the broken parts of the system, reload the latest snapshot and then replay all events that occurred after the snapshot
  - assume: this requires idempotent event processing to work reliably.