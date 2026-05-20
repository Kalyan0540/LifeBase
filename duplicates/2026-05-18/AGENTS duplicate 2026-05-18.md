# LifeBase Wiki — Schema

This file defines the structure, conventions, and workflows for the LifeBase wiki. Read it at the start of every session before touching any wiki files.

---

## Directory layout

```
LifeBase/
├── AGENTS.md      ← this file (schema)
├── index.md       ← catalog of all wiki pages
├── log.md         ← append-only session log
├── raw/           ← immutable source documents (never edit)
│   └── assets/    ← locally downloaded images and attachments
└── wiki/          ← LLM-generated wiki pages go here (empty to start)
```

**Rules:**
- `raw/` is read-only. Never create or edit files there — only the user adds sources.
- `wiki/` is owned entirely by the LLM. Users read it; the LLM writes it.
- `index.md` and `log.md` are updated on every ingest, every answered query that produces a new page, and every lint pass.
- **File naming**: wiki page filenames must match exactly the display text used in `[[wiki links]]` — including capitalisation, spaces, and special characters (e.g. `Colour Token Architecture.md`, `LLM Wiki — Karpathy.md`). Obsidian resolves links by filename, not by frontmatter title. Never use slugs or lowercase-hyphenated names.

---

## Page format

Frontmatter varies by page type. Only include what's relevant — don't add fields that don't apply.

**YouTube source pages:**
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
Extract `channel_name` and `channel_url` from the clipped file. If not found, leave as empty string. `published` and `duration_seconds` come from the clip metadata if available.

**Non-YouTube source pages:**
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

**Concept pages:**
```yaml
---
type: concept
sources:
  - "[[Source Page Title]]"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```
`sources` is a list of wiki links to the source pages this concept draws from.

**Overview page:**
```yaml
---
type: overview
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

**Entity pages:**
```yaml
---
type: entity
sources:
  - "[[Source Page Title]]"
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---
```

Body is plain markdown. Use Obsidian wiki links to cross-reference other wiki pages by their title. Every page should link to at least one other page.

---

## Operations

### Ingest

When the user says to ingest a source (drops a file in `raw/` or pastes content):

1. Read the source in full.
2. If the source is a YouTube video, extract the channel name from the clipped file (byline, author field, or link near the top).
3. Discuss key takeaways with the user if they want to stay involved.
4. Create a summary page in `wiki/sources/` named exactly as it will be linked in Obsidian. Do not use slugs. If the source is from YouTube, include `channel_name` and `channel_url` in the frontmatter.
5. Create or update entity pages in `wiki/entities/` for any people, places, products, or events mentioned.
6. Create or update concept pages in `wiki/concepts/` for any key ideas or themes.
7. Update `wiki/overview.md` if the source meaningfully changes the overall synthesis.
8. Update `index.md` — add the new source page, update any entity/concept pages that changed.
9. Append an entry to `log.md` with prefix `## [YYYY-MM-DD] ingest | <source title>`.

A single source may touch 5–15 wiki pages. That is normal and expected.

### Query

When the user asks a question:

1. Read `index.md` to identify relevant pages.
2. Read those pages in full.
3. Synthesize an answer with citations (link to wiki pages, not raw sources).
4. If the answer is substantial and reusable, write it as a new page in `wiki/` of type `query` and update `index.md`.
5. Append an entry to `log.md` with prefix `## [YYYY-MM-DD] query | <question summary>`.

### Lint

When the user asks for a health check:

1. Scan all wiki pages for: orphan pages (no inbound links), missing cross-references, contradictions between pages, stale claims superseded by newer sources, concepts mentioned but lacking their own page.
2. Report findings as a list.
3. Fix any clear issues (broken links, missing cross-refs).
4. Append an entry to `log.md` with prefix `## [YYYY-MM-DD] lint | <summary>`.

---

## index.md conventions

Organized by category. Each entry: `- <wiki link to page> — one-line summary`.

Categories in order: Overview, Sources, Entities, Concepts, Queries.

---

## log.md conventions

Append-only. Each entry:

```
## [YYYY-MM-DD] <operation> | <title>

<one short paragraph: what was done, what pages were created or updated>
```

Operations: `ingest`, `query`, `lint`, `setup`.

Entries are parseable with: `grep "^## \[" log.md`

---

## General rules

- Never delete wiki pages. Mark them stale in frontmatter (`stale: true`) if superseded.
- When new information contradicts an existing page, update the page and note the contradiction explicitly in the body.
- Keep cross-references bidirectional where practical: if page A links to B, B should link back to A.
- Do not create a page for something that does not yet have enough content to fill at least a few sentences.
- The wiki grows incrementally. It is always a work in progress.

## Imported Claude Cowork project instructions
