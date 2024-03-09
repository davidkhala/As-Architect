# Business Continuity Plan (BCP)

Business continuity plans (BCP) should be tested annually to ensure the plan is covering current operations

For maximum resiliency, you should use only data plane operations as part of your failover operation.
- data planes typically have higher availability design goals than the control planes. (LB vs API call)

Focused on business objectives (business requirements, priorities, and context) than workload (technology)
> An earthquake might prevent you from transporting products purchased on your eCommerce application – even if effective DR keeps your workload functioning, your BCP needs to accommodate transportation needs.

It includes
- [disaster recovery plan](./plan.md)

## Business impact analysis (BIS) and risk assessment

A *business impact analysis* should

- quantify the business impact of a disruption to your workloads
- determine how quickly the workload needs to be made available
- determine how much data loss can be tolerated.
- inform the business value of providing DR for a workload by factoring in probability of disruption and cost of recovery
  > If the cost of the recovery strategy is higher than the cost of the failure or loss, the recovery option should not be put in place unless there is a secondary driver such as regulatory requirements.

A *risk assessment* determine the probability of disruption occurring, based on
- the type of disaster and geographical impact
- an overview of the technical implementation of your workload
