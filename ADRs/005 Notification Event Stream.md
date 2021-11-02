# 005 Notification Event Stream

Date: 2021-11-01

## Status

Proposed

## Context

All customer interactions with both Farmacy Foods and Farmacy Family will be delivered to the EventBridge. We need a separate event stream which will deliver events needed for all notifications needs which will have its own latency (typically very low)

## Decision

Have a separate Kinesis stream for the notifications pipeline. Using pre-defined rules, all events matching the rules will be delivered to this stream

## Consequences

The notification sub-system can now have a event processor that consumes events from a single stream. For e.g. when a customer purchases a product, we need capability to send an email highlighting the benefits of Farmacy Family. 

**Positive:**  

**Negative:**

**Risks:** 

**Bonus Features:** 
