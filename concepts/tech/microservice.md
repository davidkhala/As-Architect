[Introduction to Microservices Governance](https://medium.com/microservices-learning/introduction-to-microservices-governance-part-i-53f407d7ec62)
- Smart endpoints and dump pipes: avoid using Enterprise Service Bus (ESB). Business logic and app is not infra, it should not be designed in ESB
- 1 db for each service(?)
- Infra automation with CD is must
- Focus business capabilities instead of around tech
- Component-ization: independently replace parts of a system

Industry has found its faster to build app in microservice by full-stack dev vs by team with role assigned by tech stack


# [Compared to SOA](https://www.atlassian.com/microservices/microservices-architecture/soa-vs-microservices)
- Larger, centralized teams can manage SOA. Microservices demand a higher degree of expertise and collaboration within smaller teams.
- SOA involves more centralized planning and integration. Microservice architecture facilitates faster development with independent deployments.
- SOA highlights on reusability and interoperability. Require strong governance structure and mature development processes.
- Microservice highlights on speed, agility, flexibility, and fault isolation. Require companies with a DevOps culture focusing on continuous delivery.

# Drawback
Don't use microservice if you write application which is
- small
- Not business critical
- to be built by single app dev team and/or with single schedules and milestones
- to be built by organization and role is aligned by tech stacks (backend service dev, UI, middleware, DBA), not by business capability implemented by full stack dev
- designed in infra mindset

