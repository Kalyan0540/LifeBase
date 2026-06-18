# LifeBase Agent Router

Read this file first. Then read only the rule file needed for the user's request.

## Routing

- Knowledge/wiki request: read `rules/Wiki.md`.
- Generic process/ingest unprocessed files request: check all inboxes and read the matching rules for each non-empty inbox (`rules/Wiki.md` for `raw/knowledge/inbox/`, `rules/work/Work.md` plus `rules/work/Process Work.md` for `raw/work/inbox/`, and `rules/Thoughts.md` for `raw/thoughts/inbox/`).
- Work query, product status, tasks, decisions, or patterns: read `rules/work/Work.md`.
- Work inbox processing: read `rules/work/Work.md`, then `rules/work/Process Work.md`.
- Work page or task creation/update: also read `rules/work/Work Formats.md`.
- Thoughts/ideas request: read `rules/Thoughts.md`.

If a request crosses areas, read the relevant rule files. Keep wiki, work, and thoughts separate unless the user explicitly asks to connect or promote material.

## Global Rules

- Read the smallest useful set of files. Start from indexes, then open only the pages needed.
- Existing captured files in `raw/` are source material. Do not edit their contents unless the user explicitly asks.
- Do not process rule/helper files in `rules/`.
- Do not process files named `_README.md` inside `Concepts/`, `Decisions/`, or `Patterns/` folders.
- Keep language simple and close to the user's notes.
- Obsidian resolves links by filename. Page filenames should match the visible link text exactly.
- Metadata is for the LLM, not the user. Keep frontmatter minimal. Put IDs, dates, and source links at the bottom when possible.
