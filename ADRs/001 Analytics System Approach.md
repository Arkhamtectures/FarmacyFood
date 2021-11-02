# 001 Analytics System Approach

Date: 2021-11-01

## Status

Proposed

## Context

The analytics sub-system is one of the core systems of Farmacy Family. It provides a complete view of each user i.e. his dietary needs, his goals, his interaction. It drives the predictive and prescriptive capabilities of Farmacy Family. The sub-system needs to expandable (for new interaction types and new services). 

## Decision

We will go with a event-driven architecture for the analytics module. The other services of Farmacy Foods and Farmacy family will need to publish events to the analytics event bridge. They would not need to concern with OLAP needs of Farmacy Family. The events will be processed by the analytics sub-system and stored for analytic needs of Farmacy family

## Consequences

**Positive:** Other sub-systems need not concern with analytic needs. Adding new sub-systems or interaction types will be easier

**Negative:** 

**Risks:** Development team needs to be experienced with designing and developing event driven system

**Bonus Features:** If any
