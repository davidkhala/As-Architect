[Introduction to Microservices Governance](https://medium.com/microservices-learning/introduction-to-microservices-governance-part-i-53f407d7ec62)
- Smart endpoints and dump pipes: avoid using Enterprise Service Bus (ESB)
- 1 db for each service(?)
- Infra automation with CD is must
- Around business capabilities instead of around tech
- Component-ization: independently replace parts of a system


# [Compared to SOA](https://www.atlassian.com/microservices/microservices-architecture/soa-vs-microservices)
- Larger, centralized teams can manage SOA. Microservices demand a higher degree of expertise and collaboration within smaller teams.
- SOA involves more centralized planning and integration. Microservice architecture facilitates faster development with independent deployments.
- SOA highlights on reusability and interoperability. Require strong governance structure and mature development processes.
- Microservice highlights on speed, agility, flexibility, and fault isolation. Require companies with a DevOps culture focusing on continuous delivery.

# Drawback
Don't use microservice if you write application which is
- small
- Not business critical 
