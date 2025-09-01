# High Availability
> High Availability focuses on components of the workload -- AWS

- Assumption: The interconnections between your HA systems function perfectly

# Plan for maintenance and downtime

## unplanned maintenance event

event occurs when the platform(e.g.Azure) **predicts** that any platform component associated to a physical machine is about to fail.

- Azure: uses Live Migration technology to migrate your virtual machines from the failing hardware to a healthy physical machine.

## unexpected downtime
occurs when the hardware or the physical infrastructure for your platform componen fails unexpectedly.

## planned maintenance
periodic updates made by service provider to the underlying platform to improve overall reliability, performance, and security of the platform