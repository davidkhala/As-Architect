# [DR in cloud is different](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-is-different-in-the-cloud.html)

what can be saved
- physically transporting tapes
- replicating data to another site
- fixed capital expense of a physical backup data center by OpEx
- data center connectivity  (with the exception of your ability to access it)
- power, air conditioning, fire suppression
- hardware failure

what can be better
- Simple and repeatable testing allow you to test more easily and more frequently

## With single Region
- Continuous backup of data within this region to reduce risk of human threats
- Partition workloads across multiple zones
- deploying across multiple Availability Zones(AZ)

## With multiple Regions
- back up data and configuration (including infrastructure definition) to another Region
- It is recommended you use a different account per Region in the case compromised credentials are part of your disaster recovery plans as well.

# Ref

[AWS Well-Architected Framework - Reliability Pillar whitepaper](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)

Architect can reproduce product features provided by [AWS Resilience Hub](https://github.com/davidkhala/aws-collections/blob/main/architect/DR/resilience-hub.md) in a DR project
