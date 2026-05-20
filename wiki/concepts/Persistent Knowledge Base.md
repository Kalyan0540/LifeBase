---
type: concept
sources:
  - "[[LLM Wiki — Karpathy]]"
created: 2026-05-07
updated: 2026-05-07
---

# Persistent Knowledge Base

A knowledge system where an LLM incrementally builds and maintains structured content over time, rather than re-deriving answers from raw documents on every query. The core idea behind [[LLM Wiki — Karpathy]] and this wiki itself.

## Contrast with RAG

Standard RAG retrieves raw document chunks at query time — nothing accumulates between sessions. A persistent knowledge base compiles knowledge once and keeps it current as new sources arrive. Cross-references, contradictions, and synthesis are pre-done, not re-computed per query.

## Why it works

The bottleneck in human-maintained wikis is bookkeeping — updating cross-references, keeping summaries current, flagging contradictions. LLMs handle this at near-zero cost. The human focuses on sourcing, directing analysis, and asking good questions.

## Precedent

Related in spirit to Vannevar Bush's **Memex** (1945) — a personal, curated knowledge store with associative trails between documents. Bush envisioned private, actively curated knowledge where connections between documents are as valuable as the documents themselves. The unsolved problem was who does the maintenance. LLMs solve that.

## Related pages

- [[LLM Wiki — Karpathy]]
- [[LLM Wiki Architecture]]
- [[Obsidian]]
