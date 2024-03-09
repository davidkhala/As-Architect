# Business Continuity Plan (BCP)

Business continuity plans (BCP) should be tested annually to ensure the plan is covering current operations

Focused on business objectives (business requirements, priorities, and context) than workload (technology)
> An earthquake might prevent you from transporting products purchased on your eCommerce application – even if effective DR keeps your workload functioning, your BCP needs to accommodate transportation needs.

It includes
- disaster recovery plan

## Business impact analysis (BIS) and risk assessment

A *business impact analysis* should

- quantify the business impact of a disruption to your workloads
- determine how quickly the workload needs to be made available
- determine how much data loss can be tolerated.
- inform the business value of providing DR for a workload by factoring in probability of disruption and cost of recovery

A *risk assessment* determine the probability of disruption occurring, based on
- the type of disaster and geographical impact
- an overview of the technical implementation of your workload

# Disaster Recovery strategy plan
Broadly 4 DR strategies
- backup and restore
- pilot light
- warm standby
- multi-site active/active
  > active/active in DR has different meanings of multi-writes in DB


## Recovery objectives (RTO and RPO)


### RTO
the maximum acceptable delay between the interruption of service and restoration of service.

