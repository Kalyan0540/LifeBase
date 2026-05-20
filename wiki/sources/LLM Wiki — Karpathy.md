---
type: source
source_title: "LLM Wiki"
source_url: "https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f"
raw_path: "raw/llm-wiki.md"
created: 2026-05-07
updated: 2026-05-14
---

# LLM Wiki — Karpathy

A pattern for building personal knowledge bases using LLMs. Written by Andrej Karpathy as an idea file intended to be shared with an LLM agent to instantiate a specific implementation. This wiki is itself an implementation of that pattern.

## Core idea

Standard RAG re-derives knowledge on every query — nothing accumulates. This pattern is different: the LLM **incrementally builds and maintains a persistent wiki** between you and raw sources. When a new source is added, the LLM reads it, integrates it into existing pages, notes contradictions, and updates cross-references. Knowledge compounds over time rather than being re-discovered.

The wiki is a **persistent, compounding artifact** — cross-references are pre-built, contradictions pre-flagged, synthesis pre-done.

## Three-layer architecture

See [[LLM Wiki Architecture]] for full details.

1. **Raw sources** — immutable. LLM reads but never modifies.
2. **The wiki** — LLM-owned markdown pages. Summaries, entity pages, concept pages, synthesis.
3. **The schema** — config file (AGENTS.md / CLAUDE.md) that defines structure, conventions, and workflows.

## Three operations

- **Ingest** — drop source → LLM reads → summary page created → entity/concept pages updated → index updated → log entry appended. One source can touch 10–15 pages.
- **Query** — LLM reads index → reads relevant pages → synthesises answer with citations. Good answers get filed back as new wiki pages so explorations compound.
- **Lint** — periodic health check: orphan pages, missing cross-refs, contradictions, stale claims, data gaps.

## Indexing and logging

- **index.md** — content-oriented catalog. LLM reads this first on every query to find relevant pages. Works at ~100 sources / hundreds of pages without needing vector RAG.
- **log.md** — append-only chronological record. Parseable with `grep "^## \[" log.md`.

## Human vs LLM division of labour

- **Human**: curate sources, direct analysis, ask good questions.
- **LLM**: summarise, cross-reference, file, maintain consistency, bookkeeping.

The key insight: maintenance burden is what kills human-maintained wikis. LLMs don't get bored, don't forget cross-references, can touch 15 files in one pass.

## Related pages

- [[LLM Wiki Architecture]]
- [[Persistent Knowledge Base]]
- [[Obsidian]]
