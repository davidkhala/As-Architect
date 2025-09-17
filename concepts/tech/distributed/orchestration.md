Orchestration is like an air traffic control tower directing planes, or microservices. 

One service, a "super microservice" sends messages directly to individual microservices telling them what to do ("Command")



- Easier to build with greenfield applications
- The recipient does not necessarily know who issued the command.

# Caveats
- the message broker is a single point of failure.
- Is “harder” to implement initially, but pays dividends later
