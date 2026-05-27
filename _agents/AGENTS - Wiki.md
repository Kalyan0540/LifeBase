# LifeBase Wiki Agent

Rules for durable knowledge sources, summaries, concepts, and entities.

## Purpose

Use the wiki for durable knowledge: articles, videos, essays, research, and reusable ideas.

Do not put work notes, todos, or personal thoughts into the wiki unless the user explicitly asks to promote them into durable knowledge.

## Structure

```text
raw/knowledge/inbox/ new unprocessed knowledge source captures
raw/knowledge/<broad-topic>/ processed raw knowledge sources, grouped by broad domain
raw/knowledge/<broad-topic>/<subtopic>/ optional subfolders when a broad topic gets crowded
wiki/sources/        one processed source page per raw source
wiki/concepts/       reusable ideas and themes
wiki/entities/       people, products, companies, places, events
wiki/overview.md     current synthesis of the knowledge wiki
index.md             top-level catalog
log.md               knowledge/wiki operation log
```

Legacy knowledge sources may still exist directly under `raw/`.

New knowledge files should be added to `raw/knowledge/inbox/`. During ingest, classify each inbox file first and move it to its final topic folder before creating generated wiki pages. Moving a file out of inbox is not a completed ingest; the source page, concept/entity pages, indexes, and log must still be updated in the same processing pass.

Keep `raw/knowledge/` top-level folders broad and few. Prefer names such as `product-and-design`, `technology`, `health-and-wellness`, `finance`, and `mental-models`. Use subfolders inside those broad folders only when the file count or retrieval need justifies it. For example: AI and cryptography belong under `technology/`, not as separate top-level folders.

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

1. Identify new knowledge files in `raw/knowledge/inbox/`. Also check for legacy unprocessed files by comparing raw files against `raw_path` in `wiki/sources/`.
2. Read each source enough to classify it into a stable broad topic folder under `raw/knowledge/`, and only choose/create a subfolder if the broad folder is already becoming crowded.
3. Move the raw file from `raw/knowledge/inbox/` to the chosen topic folder before generating pages.
4. Read the source fully from its final location.
5. Create or update one source page in `wiki/sources/` with `raw_path` pointing to the final raw location.
6. Create or update concept/entity pages only when there is enough content.
7. Update `wiki/overview.md` when the synthesis changes.
8. Update root `index.md`.
9. Append a knowledge entry to root `log.md`.

Do not leave a file merely moved into a topic folder without a corresponding wiki processing update.

## Link Rules

- Use Obsidian links for wiki pages.
- Page filenames must match visible link text.
- Do not use slugified filenames for generated wiki pages.
