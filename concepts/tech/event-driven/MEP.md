# Messaging Exchange Patterns (MEPs)
Most applications can be reduced to a series of interactions that adhere to one of the below 3 patterns
## pattern: Publish-Subscribe
![image](https://github.com/davidkhala/As-Architect/assets/7227589/9de0713a-a299-484b-a385-d6737e5ea0f1)

Messages sent by the Producer are processed multiple times by different consumers. 

Each consumer receives its own copy of the message for processing.
## pattern: Point-to-Point
![image](https://github.com/davidkhala/As-Architect/assets/7227589/20d30759-952e-43d2-8006-7f0befc4dd9e)

Messages sent by the Producer are processed by a single Consumer.
### p2p extension: Non-Exclusive Consumption
![image](https://github.com/davidkhala/As-Architect/assets/7227589/022ee595-5e45-4901-9176-215dccb8a580)
by using consumer groups—multiple consumers sharing a single channel or queue. 

The scale of the overall receiving application is increased by having multiple consumers, but each message is still only delivered to a single endpoint. 

## pattern: Request-Reply
![image](https://github.com/davidkhala/As-Architect/assets/7227589/3f9b1c18-d254-45f6-bf94-c0da49ce7f60)

applications achieve two-way communication using separate point-to-point channels: one for requests, and another for replies.



