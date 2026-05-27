# Log

Append-only chronological record of all wiki operations.

Parse entries with: `grep "^## \[" log.md`

---

## [2026-05-07] setup | Minimal LLM Wiki scaffold

Created the minimal structure explicitly described by Karpathy's LLM Wiki pattern: `raw/` for immutable source material, `raw/assets/` for optional local Obsidian attachments, `wiki/` for LLM-generated markdown pages, `AGENTS.md` as the schema, `index.md` as the content-oriented catalog, `log.md` as the chronological activity record.

---

## [2026-05-07] ingest | Figma Design System 2025 - Colour Tokens Ep 1

Processed YouTube video transcript (channel: TD Sunshine). Created source page `wiki/sources/Figma Design System 2025 - Colour Tokens Ep 1.md`. Created concept pages: `Colour Token Architecture.md`, `Figma Variables.md`, `Dark Mode Design.md`. Updated `index.md`, `overview.md`, and `log.md`.

---

## [2026-05-07] ingest | LLM Wiki — Karpathy

Processed Karpathy's GitHub Gist on the LLM wiki pattern. Created source page `wiki/sources/LLM Wiki — Karpathy.md`. Created concept pages: `LLM Wiki Architecture.md`, `Persistent Knowledge Base.md`, `Obsidian.md`. Updated `index.md`, `overview.md`, and `log.md`.

---

## [2026-05-09] ingest | 13 new sources (product strategy, UX, behavioural psychology, philosophy)

Processed 13 raw files added to `raw/`. Created 13 source pages, 10 new concept pages, and 4 entity pages. Updated `index.md`, `overview.md`, and `log.md`.

**Source pages created:** `Building a Winning UX Strategy Using the Kano Model - Jared Spool.md`, `Flywheel Effect - Why Positive Feedback Loops are a Meta-Competitive Advantage.md`, `Growth Without Ads - Kunal Shah, Founder CRED.md`, `Hooked How to Build Habit-Forming Products with Nir Eyal (Long).md`, `How to Build Habit-Forming Products - Nir Eyal (Short).md`, `How to Use First Principles Thinking for Business.md`, `Jared Spool – Beyond The UX Tipping Point.md`, `Kunal Shah at Tech Sparks 2016.md`, `PDC 1996 Keynote with Douglas Adams.md`, `The MAYA Principle.md`, `The Science of Successful Things - Derek Thompson.md`, `Where Teams and Agents Work Together.md`, `Why Do Competitors Open Their Stores Next to One Another.md`.

**Concept pages created:** `Kano Model.md`, `Hook Model.md`, `Delta 4 Framework.md`, `Flywheel Effect.md`, `First Principles Thinking.md`, `UX Design Maturity Model.md`, `Hotelling's Model.md`, `Variable Rewards.md`, `User Journey Mapping.md`, `MAYA Principle.md`.

**Entity pages created:** `Jared Spool.md`, `Nir Eyal.md`, `Kunal Shah.md`, `Douglas Adams.md`.

**Domains added:** product strategy & growth, behavioural psychology & habit design, UX strategy & design thinking, first principles & mental models. Overview updated to reflect all six domains and their cross-domain connections.

---

## [2026-05-18] setup | Work and thoughts memory scaffold

Created backups for `AGENTS.md`, `index.md`, and `log.md` before modifying them. Added the work memory structure (`work/Work Index.md`, `work/Work Inbox Index.md`, `work/Work Tasks.md`, `work/Work Task History.md`, `work/Work Log.md`, `work/products/`) and thoughts memory structure (`thoughts/Thoughts Index.md`, `thoughts/Thoughts Log.md`, `thoughts/topics/`). Added future raw capture folders under `raw/knowledge/`, `raw/work/inbox/`, and `raw/thoughts/inbox/`. Updated `AGENTS.md` and `index.md` to keep durable knowledge, work memory, and thoughts memory separate.

---

## [2026-05-27] ingest | Health and wellness sources

Processed 2 raw health/wellness source files. Created source pages `wiki/sources/The REAL Reason Diabetes Is So Dangerous.md` and `wiki/sources/You're Exercising Wrong.md`. Created concept pages `Diabetes and Metabolic Health.md` and `Longevity Exercise Pillars.md`. Updated `index.md`, `overview.md`, and `log.md`.

Organised legacy top-level raw knowledge captures into broad topical folders under `raw/knowledge/`: `product-and-design/`, `technology/`, `mental-models/`, and `health-and-wellness/`. Product and design material uses subfolders under `product-and-design/`; AI material lives under `technology/ai/`. Updated source-page `raw_path` frontmatter to point to the new locations. Moved processed work captures from `raw/work/inbox/` to `raw/work/processed/` and updated current source links.
