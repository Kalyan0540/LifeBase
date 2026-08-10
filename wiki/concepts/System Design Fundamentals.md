---
type: concept
sources:
  - "[[900+ hours of Learning System Design in 9 Minutes]]"
created: 2026-07-17
updated: 2026-07-17
---

# System Design Fundamentals

System design is less about memorizing component names and more about reasoning through tradeoffs. The source frames six fundamentals as reusable questions for architecture.

## Six Tradeoff Questions

1. **State:** what state does each server hold, and should it move to a client token, shared store, or distributed cache?
2. **Freshness:** where would a cache reduce latency, and how stale can the data be?
3. **Consistency:** which operations need the latest write, and which can tolerate eventual consistency during partitions?
4. **Dependency:** which synchronous calls can become queued events so one slow service does not fail the whole flow?
5. **Data guarantees:** does this workload need ACID transactions, or is flexibility/scale with relaxed consistency acceptable?
6. **API contract:** what contract are clients depending on, and how will versioning and documentation prevent breakage?

## Interview Use

The practical move is to apply each concept to a real system instead of reciting definitions. For example, a payment flow can be analyzed for strong consistency and ACID needs, while a feed can be analyzed for caching and eventual consistency.

## Links

- [[900+ hours of Learning System Design in 9 Minutes]]
