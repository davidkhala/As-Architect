Orchestration is like an air traffic control tower directing planes, or microservices. 

One service, a “super microservice” if you will, functions as the message broker sending messages directly to individual microservices telling them what to do

![image](https://github.com/davidkhala/As-Architect/assets/7227589/7fa7c417-30d8-401d-822c-5f49b8652425)

- Easier to build with greenfield applications


# Caveats
- the message broker is a single point of failure.
- Is “harder” to implement initially, but pays dividends later
