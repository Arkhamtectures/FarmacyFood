# 006 Analytics Event Processor

Date: 2021-11-01

## Status

Proposed

## Context

All events in the analytics event stream need to be batched and processed. The event processor need to be easily modifiable as analytics needs evolve. It should be elastic as we balance performance and cost

## Decision

We will go with AWS Lambda to process the events. This will keep development quick and easilyh modifiable. Using back-pressure of the kinesis stream, we can control how quickly to process the events. 

## Consequences

**Positive:**  Quick development using familiar languages, serverless

**Negative:**

**Risks:** 

**Bonus Features:** 
