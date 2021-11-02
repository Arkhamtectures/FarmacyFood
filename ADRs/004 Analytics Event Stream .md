# 004 Analytics Event Stream

Date: 2021-11-01

## Status

Proposed

## Context

All customer interactions with both Farmacy Foods and Farmacy Family will be delivered to the EventBridge. We need a separate event stream which will deliver events needed for all analytical needs which will define its own SLA or latency. 

## Decision

Have a separate Kinesis stream for analytics pipeline. Using pre-defined rules, all events matching the rules will be delivered to this stream

## Consequences

The analytics sub-system can now have a event processor that consumes events from one stream and populates the analytics DB. As this system evolves or expands, additional stream and processorts can be added 

**Positive:**  We can balance latency vs costs using a seperate stream. Maximizing batch processing of events will keep costs down

**Negative:**

**Risks:** 

**Bonus Features:** 
