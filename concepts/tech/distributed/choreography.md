
- Loose coupling: Choreography allows microservices to be loosely coupled, which means they can operate independently and asynchronously without depending on a central coordinator. 

# caveats
- If you have any sort of ordering requirement of tasks, such as ordered steps in your saga, choreography can get unwieldy fairly quickly.
  - it’s difficult to understand the order that the system should have since that ordering is distributed throughout the code. 
