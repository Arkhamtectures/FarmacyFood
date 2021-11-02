# 001 Analytics System Approach

Date: 2021-11-01

## Status

Proposed

## Context

The analytics sub-system requires a reliable and scalable event bus that also enables full de-coupling of event producers and consumers. 

## Decision

We will go with AWS EventBridge 

## Consequences

**Positive:** Other sub-systems need not concern with analytic needs. Adding new sub-systems or interaction types will be easier

**Negative:**

**Risks:** Development team needs to be experienced with designing and developing event driven system

**Bonus Features:** If any
