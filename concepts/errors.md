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


Technical errors in a distributed system landscape are non-deterministic
- You cannot predict when they will occur and how they will manifest.
- The only thing you know for sure is that they will happen for sure, i.e., their probability is bigger than 0.
