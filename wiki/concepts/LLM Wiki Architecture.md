---
type: concept
sources:
  - "[[LLM Wiki — Karpathy]]"
created: 2026-05-07
updated: 2026-05-14
---

# LLM Wiki Architecture

The three-layer architecture behind the [[Persistent Knowledge Base]] pattern described in [[LLM Wiki — Karpathy]]. This wiki is an implementation of it.

## Layer 1 — Raw sources

Immutable source documents. Articles, papers, transcripts, images, data files. The LLM reads from them but never modifies them. Source of truth.

Location: `raw/`, attachments in `raw/assets/`.

## Layer 2 — The wiki

LLM-generated markdown pages. Summaries, entity pages, concept pages, comparisons, synthesis, query results. The LLM owns this layer entirely — creates pages, updates them, maintains cross-references.

Location: `wiki/` and subdirectories.

## Layer 3 — The schema

A config document (here: `AGENTS.md`) that tells the LLM how the wiki is structured, what conventions to follow, and what workflows to run for each operation. Co-evolved by the human and LLM over time.

## Navigation files

- **index.md** — content-oriented catalog. LLM reads first on every query to locate relevant pages. Scales to ~100s of sources without vector RAG.
- **log.md** — append-only chronological record. Parseable with grep. Helps the LLM understand recent history.

## Operations

- **Ingest** — read source → create/update pages → update index → append log entry
- **Query** — read index → read relevant pages → synthesise → optionally file result
- **Lint** — scan for orphans, contradictions, stale content, missing cross-refs

## Related pages

- [[LLM Wiki — Karpathy]]
- [[Persistent Knowledge Base]]
- [[Obsidian]]
