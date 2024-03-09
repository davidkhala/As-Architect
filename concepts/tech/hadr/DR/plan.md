# Disaster Recovery strategy planning
Broadly 4 DR strategies
- backup and restore
- pilot light
- warm standby
- multi-site active/active or hot standby active/passive
  

![4strategies](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/disaster-recovery-strategies.png)

## Backup and restore
In addition to data, you must redeploy the infrastructure, configuration, and application code in the recovery Region.
- To restore without IaC will lead to increased recovery times then exceed your RTO.

## Pilot light

- DBs and object storage is always on to support repliciate and backup
- app servers are loaded with code and configurations, with capability to deploy but off.
- provision a copy of your core workload infrastructure (VPC, LB, scaling group) and they are always available 

You need to make sure core infrastructure changes are synced across regions

## Warm standby
- there is a scaled down, but fully functional and always-on, copy of your production environment in another Region.

## Multi-site active/active
Multi-site active/active serves traffic from all regions to which it is deployed
- active/active DB is required
- no failover
- The Disaster recovery Drill in this case would focus on how the workload reacts to loss of a Region:
  - Is traffic routed away from the failed Region? 
  - Can the other Region(s) handle all the traffic?
- human disaster still need to rely on backups, which usually results in a non-zero recovery point evitably.

## Hot standby active/passive
hot standby serves traffic only from a single region, and the other Region(s) are only used for disaster recovery


## Recovery objectives (RTO and RPO)
![RTO-vs-RPO](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-objectives.png)

### RTO
the maximum acceptable delay between the interruption of service and restoration of service.
![RTO-strategy](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-time-objective.png)

### RPO
Recovery Point Objective (RPO) is the maximum acceptable amount of time since the last data recovery point.

![RPO](https://docs.aws.amazon.com/images/whitepapers/latest/disaster-recovery-workloads-on-aws/images/recovery-point-objective.png)
