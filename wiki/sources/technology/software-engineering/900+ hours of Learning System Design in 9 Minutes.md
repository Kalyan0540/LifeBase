---
type: source
source_title: "900+ hours of Learning System Design in 9 Minutes"
source_url: "https://www.youtube.com/watch?v=3Pusamd6BO4"
raw_path: "raw/knowledge/technology/software-engineering/900+ hours of Learning System Design in 9 Minutes.md"
created: 2026-07-17
updated: 2026-07-17
---

# 900+ hours of Learning System Design in 9 Minutes

A Maddy Zhang video that condenses system design into six interview- and architecture-oriented mental models: statelessness, caching, CAP theorem, message queues, database guarantees, and API design.

## Core Ideas

### Statelessness

Horizontal scaling depends on servers being interchangeable. If session state is stored on a specific app server, the load balancer needs sticky sessions and that server becomes a failure point. Move state to a client token, shared store, distributed cache, or another shared system so any server can handle the next request.

Main design question: what state is this server holding, and where should it live?

### Caching

Caching is a freshness-for-speed tradeoff. Browser caches, CDNs, application caches such as Redis, and database query caches all store a faster copy of data while accepting some staleness.

Main design questions:

- where is the bottleneck?
- how stale can this data be?
- what TTL, cache-aside, write-through, or write-back behavior is appropriate?

### CAP Theorem

In real distributed systems, network partitions are not optional. The practical choice is which operations require consistency and which can remain available with possibly stale data.

Examples from the source:

- financial transactions, access control, and permissions need stronger consistency
- feeds and similar experiences may tolerate eventual consistency

### Message Queues

Queues break synchronous dependency chains. Instead of making order placement wait on inventory, payment, and notification services, the system can publish an `order placed` event to Kafka, SQS, or a similar queue and let downstream services process independently.

This improves resilience because downstream outages do not have to fail the user's core action.

### Databases

SQL vs NoSQL is framed as a guarantees question, not an old/new or simple/scalable choice.

SQL is favored when ACID guarantees matter:

- atomicity: all-or-nothing transaction
- consistency: writes preserve valid database state
- isolation: concurrent transactions do not interfere
- durability: committed data survives crashes

NoSQL can fit high-scale, flexible, or eventually consistent workloads such as feeds, catalogs, or analytics where slightly stale data is acceptable.

### API Design

An API is a contract. Once clients depend on it, changes become migrations, not simple code edits.

The source contrasts:

- REST: simple, cacheable, resource-oriented, stable for public APIs and mobile clients
- GraphQL: flexible for multiple clients with different data needs

Regardless of style, the source recommends explicit versioning, resource-oriented design, and documented contracts.

## Links

- [[System Design Fundamentals]] - concept derived from this source
