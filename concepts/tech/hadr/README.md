# High Availability
Eliminating single points of failure
- AWS: High Availability focuses on components of the workload

A case with HA but not DR
> Consider a storage solution that continuously replicates to another site to achieve high availability (such as a multi-site active/active workload).
> If a file or files are deleted or corrupted on the primary storage device, those destructive changes can be replicated to the secondary storage device.
> In this scenario, despite high availability, the ability to failover in case of data deletion or corruption will be compromised.
> Instead, a point-in-time backup is also required as part of a DR strategy.

Assume: The interconnections between your HA systems function perfectly

[AWS: HA is not DR](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/high-availability-is-not-disaster-recovery.html)

HA is often a major component of DR

# Disaster Recovery 
The process of getting a system back to an operational state when a system is rendered inoperative.
- AWS: disaster recovery focuses on discrete copies of the entire workload.

In essence, disaster recovery picks up when high availability fails, so **HA first**. You should first ensure your workload meets your availability objectives

A case with DR but not HA
- single standalone DB with continous backup

