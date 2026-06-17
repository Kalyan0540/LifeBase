# Wiki Log

Append-only chronological record of wiki operations.

Parse entries with: `grep "^## \[" "wiki/Wiki Log.md"`

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

Created backups for `AGENTS.md`, `index.md`, and `log.md` before modifying them. Added the work memory structure (`work/Work Index.md`, `work/Work Inbox Index.md`, `work/Work Tasks.md`, `work/Work Task History.md`, `work/Work Log.md`, `work/products/`) and thoughts memory structure (`thoughts/Thoughts Index.md`, `thoughts/Thoughts Log.md`, and `thoughts/topics/`). Added future raw capture folders under `raw/knowledge/`, `raw/work/inbox/`, and `raw/thoughts/inbox/`. Updated `AGENTS.md` and `index.md` to keep durable knowledge, work memory, and thoughts memory separate.

---

## [2026-05-27] ingest | Health and wellness sources

Processed 2 raw health/wellness source files. Created source pages `wiki/sources/The REAL Reason Diabetes Is So Dangerous.md` and `wiki/sources/You're Exercising Wrong.md`. Created concept pages `Diabetes and Metabolic Health.md` and `Longevity Exercise Pillars.md`. Updated `index.md`, `overview.md`, and `log.md`.

Organised legacy top-level raw knowledge captures into broad topical folders under `raw/knowledge/`: `product-and-design/`, `technology/`, `mental-models/`, and `health-and-wellness/`. Product and design material uses subfolders under `product-and-design/`; AI material lives under `technology/ai/`. Updated source-page `raw_path` frontmatter to point to the new locations. Moved processed work captures from `raw/work/inbox/` to `raw/work/processed/` and updated current source links.

---

## [2026-05-27] rules | Wiki index and log moved under wiki

Moved the detailed knowledge catalog from root `index.md` to `wiki/Wiki Index.md`, and moved the wiki operation history from root `log.md` to `wiki/Wiki Log.md`.

Root `index.md` is now only the top-level LifeBase map. Updated the wiki rules to use `wiki/Wiki Index.md`, `wiki/Wiki Log.md`, and domain-specific raw assets folders.

---

## [2026-05-28] ingest | 3 AI design & build sources

Processed 3 files from `raw/knowledge/inbox/`. The two AI design/UX sources were classified as design material and moved to `raw/knowledge/product-and-design/design/`; the deployment tutorial was classified as AI/technology material and moved to `raw/knowledge/technology/ai/`. Added `raw_path` frontmatter to each.

**Source pages created:** `Creating a Dynamic UX - Guidance for Generative AI Applications.md`, `Guidelines for Human-AI Interaction.md`, `The RIGHT Way to Deploy a Claude AI Website + Free Database.md`.

**Concept pages created:** `Generative AI UX Design.md`, `Human-AI Interaction Guidelines.md` (enumerates the 18 published guidelines; the raw clip only contained the summary poster), `Deploying AI-Generated Websites.md`.

Extended Domain 1 of `overview.md` from "LLM knowledge management" to also cover designing and building AI applications. Updated `Wiki Index.md` (sources + concepts) and `overview.md` (source count 17 → 20). `raw/knowledge/inbox/` is now empty.

---

## [2026-05-29] rename | "Where Teams and Agents Work Together" → "Airplane and Rocket Analogy"

Corrected a misleading title. The note's content is purely the airplane/rocket mental model about paradigm change (its Notion source URL is even titled "Airplane and rocket analogy") and has nothing to do with AI agents. Renamed the raw file and wiki source page to `Airplane and Rocket Analogy`, updated `source_title` and the page heading, and reclassified the raw file from `raw/knowledge/technology/ai/` to `raw/knowledge/mental-models/` (it sits with First Principles Thinking and Douglas Adams). Updated all backlinks in `Wiki Index.md`, `overview.md`, and `First Principles Thinking.md`. Removed the now-inaccurate "human-as-pilot" cross-links to it from `Generative AI UX Design.md` and the two generative-AI source pages, since the analogy is not AI material.

---

## [2026-06-01] ingest | 2 AI build and operating-system sources

Processed two files from `raw/knowledge/inbox/` and moved them to `raw/knowledge/technology/ai/`.

**Source pages created:** `Karpathy's LLM Wiki Goes Further Than Everyone Realised.md`, `How I Vibe Coded a Recipe App using Claude Code.md`.

**Concept pages created:** `AI-First Business Systems.md`, `AI-Assisted App Building.md`.

Updated `LLM Wiki Architecture.md`, `Persistent Knowledge Base.md`, `Wiki Index.md`, and `overview.md`.

---

## [2026-06-01] correction | Tightened wiki relevance links

Removed overly broad AI-topic links between deployment material and generative AI UX material. `Deploying AI-Generated Websites` now links only to its source page, and `The RIGHT Way to Deploy a Claude AI Website + Free Database` no longer frames itself as a counterpart to `Generative AI UX Design`.

Also removed `Deploying AI-Generated Websites` from the recipe app source footer because that source is about mobile app build/launch workflow, not website deployment.

Updated `rules/Wiki.md` with a link-quality rule: related links need a meaningful shared problem, workflow, concept, source lineage, or explicit contrast; shared broad labels like "AI" are not enough.

---

## [2026-06-09] ingest | Vitamin D physiology source

Processed `raw/knowledge/inbox/What Vitamin D REALLY Does to the Body.md` and moved it to `raw/knowledge/health-and-wellness/What Vitamin D REALLY Does to the Body.md`.

Created source page [[What Vitamin D REALLY Does to the Body]] and concept page [[Vitamin D and Bone Health]]. Updated [[Wiki Index]] and [[overview]] to include the new health/wellness source and concept.

---

## [2026-06-16] ingest | App Store Approval Checklist

Processed `raw/knowledge/inbox/App Store Approval Checklist.md` and moved it intact to `raw/knowledge/technology/ai/App Store Approval Checklist.md`.

Created source page [[App Store Approval Checklist]] as an exact-format copy of the source content, without adding frontmatter or changing the body. Linked it from [[Wiki Index]], [[overview]], and [[AI-Assisted App Building]].

Follow-up mapping: created concept page [[App Store Review Readiness for AI-Built Apps]] and connected it to [[AI-Assisted App Building]], [[Wiki Index]], and [[overview]].
