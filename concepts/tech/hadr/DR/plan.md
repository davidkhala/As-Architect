# Disaster Recovery strategy planning
Broadly 4 DR strategies
- backup and restore
- pilot light
- warm standby
- multi-site active/active
  > active/active in DR has different meanings of multi-writes in DB

![4strategies](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/disaster-recovery-strategies.png)

## Recovery objectives (RTO and RPO)
![RTO-vs-RPO](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-objectives.png)

### RTO
the maximum acceptable delay between the interruption of service and restoration of service.
![RTO-strategy](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-time-objective.png)

### RPO
Recovery Point Objective (RPO) is the maximum acceptable amount of time since the last data recovery point.

![RPO](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-point-objective.png)
