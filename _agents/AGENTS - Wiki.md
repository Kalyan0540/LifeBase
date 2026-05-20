# LifeBase Wiki Agent

Rules for durable knowledge sources, summaries, concepts, and entities.

## Purpose

Use the wiki for durable knowledge: articles, videos, essays, research, and reusable ideas.

Do not put work notes, todos, or personal thoughts into the wiki unless the user explicitly asks to promote them into durable knowledge.

## Structure

```text
raw/knowledge/       future knowledge source captures
wiki/sources/        one processed source page per raw source
wiki/concepts/       reusable ideas and themes
wiki/entities/       people, products, companies, places, events
wiki/overview.md     current synthesis of the knowledge wiki
index.md             top-level catalog
log.md               knowledge/wiki operation log
```

Legacy knowledge sources may still exist directly under `raw/`.

## Source Page Frontmatter

YouTube source:

```yaml
---
type: source
source_title: "<video title>"
source_url: "<YouTube video URL>"
channel_name: "<channel name>"
channel_url: "<YouTube channel URL>"
published: <YYYY-MM-DD>
duration_seconds: <integer>
raw_path: "raw/<filename>.md"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

Non-YouTube source:

```yaml
---
type: source
source_title: "<title>"
source_url: "<URL>"
raw_path: "raw/<filename>.md"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

## Concept/Entity Frontmatter

```yaml
---
type: concept
sources:
  - "<Obsidian source page link>"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

Use `type: entity` for entity pages.

## Knowledge Ingest

When the user asks to process knowledge sources:

1. Identify new knowledge files by comparing raw files against `raw_path` in `wiki/sources/`.
2. Read the source fully.
3. Create or update one source page in `wiki/sources/`.
4. Create or update concept/entity pages only when there is enough content.
5. Update `wiki/overview.md` when the synthesis changes.
6. Update root `index.md`.
7. Append a knowledge entry to root `log.md`.

## Link Rules

- Use Obsidian links for wiki pages.
- Page filenames must match visible link text.
- Do not use slugified filenames for generated wiki pages.
