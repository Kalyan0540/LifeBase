# Wiki Rules

Use `wiki/` for durable knowledge: articles, videos, essays, research, PDFs, and reusable ideas.

Do not put work notes, todos, or personal thoughts into the wiki unless the user explicitly asks to promote them into durable knowledge.

## Structure

```text
raw/knowledge/inbox/    new unprocessed knowledge captures
raw/knowledge/assets/   images, PDFs extracts, and attachments for knowledge notes
raw/knowledge/<topic>/  processed raw knowledge sources, grouped by broad domain
wiki/Wiki Index.md      knowledge catalog
wiki/Wiki Log.md        knowledge operation log
wiki/sources/           one processed source page per raw source
wiki/concepts/          reusable ideas and themes
wiki/entities/          people, products, companies, places, events
wiki/overview.md        current synthesis of the knowledge wiki
```

Keep `raw/knowledge/` top-level folders broad and few. Use subfolders only when a broad folder gets crowded.

## Reading Rules

- For knowledge queries, start with `wiki/Wiki Index.md` and `wiki/overview.md`.
- Read source pages, concept pages, or entity pages only when needed.
- Read raw source files only when the generated wiki page does not contain enough detail or the user asks for source-level fidelity.

## Source Files

New knowledge files go in `raw/knowledge/inbox/`. During ingest, classify each inbox file first and move it to a stable topic folder before creating generated wiki pages.

PDFs are valid raw sources. Read or extract the PDF before creating wiki pages. Preserve important tables, images, headings, and source structure when they matter.

Attachments should live in `raw/knowledge/assets/`, not inside inbox folders.

## Source Page Frontmatter

```yaml
---
type: source
source_title: "<title>"
source_url: "<URL if available>"
raw_path: "raw/knowledge/<topic>/<filename>"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

For YouTube sources, add channel or duration details only when useful.

## Concept/Entity Frontmatter

```yaml
---
type: concept
sources:
  - "[[Source Page]]"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

Use `type: entity` for entity pages.

## Knowledge Ingest

When processing knowledge sources:

1. Check `raw/knowledge/inbox/`.
2. Also check legacy unprocessed files by comparing raw files against `raw_path` in `wiki/sources/`.
3. Move each inbox file to its final topic folder before generating pages.
4. Read the source fully from its final location.
5. Create or update one source page in `wiki/sources/`.
6. Create or update concept/entity pages only when there is enough content.
7. Update `wiki/Wiki Index.md`, `wiki/overview.md`, and `wiki/Wiki Log.md`.

Do not leave a file merely moved into a topic folder without a corresponding wiki processing update.

## Link Rules

- Use Obsidian links for wiki pages.
- Page filenames must match visible link text.
- Do not use slugified filenames for generated wiki pages.

