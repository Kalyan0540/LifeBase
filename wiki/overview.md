---
type: overview
created: 2026-05-07
updated: 2026-08-10
---

# Overview

This wiki currently covers nine interconnected domains sourced from 39 ingested documents.

## Domain 1 — LLM-Powered Knowledge Management

The [[llm-wiki|LLM Wiki — Karpathy]] pattern: using an LLM to incrementally build and maintain a [[Persistent Knowledge Base]] rather than re-deriving answers via RAG. The three-layer [[LLM Wiki Architecture]] (raw sources → wiki → schema) powers this wiki itself. [[Obsidian]] is the browsing interface; `AGENTS.md` is the schema.

This domain also covers two separate practical lanes for AI-assisted software work:

- [[Deploying AI-Generated Websites]] documents a website deployment pipeline: Claude → GitHub → Hostinger → Supabase. Source: [[The RIGHT Way to Deploy A Claude AI Website + FREE Database (Nobody Explains This)|The RIGHT Way to Deploy a Claude AI Website + Free Database]].
- [[AI-Assisted App Building]] documents a mobile app build workflow: reference research → design generation → Expo React Native implementation → backend/API/storage/subscriptions → real-device testing and launch readiness. [[App Store Review Readiness for AI-Built Apps]] expands the launch-readiness layer for AI-built iOS apps: secrets, dynamic code execution, stability, AI privacy, payments, SDK compliance, and reviewer support. Sources: [[How I Vibe Coded a Recipe App using Claude Code (Full Build + Marketing)|How I Vibe Coded a Recipe App using Claude Code]], [[App Store Approval Checklist]].

These are implementation and delivery workflows. How AI experiences should *behave* and be *designed* is covered separately in Domain 5.

The newer [[AI-First Business Systems]] material extends the same LLM Wiki architecture from personal knowledge management into agency/business operations. The pattern is raw work inputs → structured wiki/JSON memory → schema and skills that tell agents where to retrieve controlled context. Source: [[Karpathy's LLM Wiki Goes Further Than Everyone Realised]].

[[Claude Code Capability Extensions]] adds a practical tooling-stack view: use specialist extensions for video, research, memory, frontend design, and token efficiency rather than expecting the base coding agent to cover every modality well. Source: [[5 Open Source Repos That Fix 95% of Claude Code's Problems]].

[[AI Writing Signals]] captures a lightweight editing checklist for AI-assisted prose: simplify inflated verbs, remove manufactured drama and generic praise, and trace vague authority claims to named evidence. These signals are revision prompts rather than reliable proof of authorship because both human and model styles change once a marker becomes widely recognised. Source: [[I Found the Easiest Sign of AI Writing]].

## Domain 2 — Figma Design Systems

Episode 1 of a practical series on building a design system in Figma. Covers the full colour layer: a two-tier [[Colour Token Architecture]] (primitives → usage tokens), [[Figma Variables]] for implementation, and [[Dark Mode Design]] via shade inversion. Source: [[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]].

The newer [[Unitless Typography Tokens in Figma]] note extends the same token thinking into typography handoff. It documents a workaround for Figma's unitless line-height gap: store calculated pixel values in variables, then use Code Syntax so developers see the semantic implementation token. Source: [[Going Unitless in Figma - Text Line-heights & letter-spacing|Going Unitless in Figma]].

[[Subtle UI Shadows]] adds a focused visual-detail pattern for card and dashboard surfaces: use negative spread values, lowered opacity, and repeated-layout testing so shadows support hierarchy without making the UI feel heavy. Source: [[Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes)]].

## Domain 3 — Product Strategy & Growth

Four areas for understanding how products spread, convert demand, and compound value:

- **[[Delta 4 Framework]]** ([[Kunal Shah]]): when a product's efficiency delta is ≥ 4, users won't go back, will tolerate glitches, and will spontaneously tell others (UBP). Products below Delta 4 require ads and discounts. Sources: [[Growth Without Ads- Is This The End Of The Ad World As We Know It? - Kunal Shah, Founder Cred|Growth Without Ads - Kunal Shah, Founder CRED]], [[Kunal Shah, Founder & CEO, Freecharge talks at Tech Sparks 2016  From the Vault|Kunal Shah at Tech Sparks 2016]].
- **[[Flywheel Effect]]**: positive feedback loops as a meta-competitive advantage. Not a source of competitive advantage itself — a force-multiplier on existing advantages. Source: [[Flywheel Effect Why Positive Feedback Loops are a Meta-Competitive Advantage|Flywheel Effect - Why Positive Feedback Loops are a Meta-Competitive Advantage]].
- **[[Hotelling's Model]]**: competing businesses cluster rather than distribute because Nash Equilibrium drives both toward the median customer, even when social optimum requires distribution. Source: [[Why do competitors open their stores next to one another? - Jac de Haan|Why Do Competitors Open Their Stores Next to One Another]].
- **[[App Store Optimization]]**: a two-part discovery and conversion system built on keyword placement, screenshot testing, and ratings/reviews. It requires iterative measurement and can take months or years to compound. Source: [[My App Makes $50K per Month - This Is My ASO Playbook]].

## Domain 4 — Behavioural Psychology & Habit Design

Two complementary frameworks for changing user behaviour:

- **[[Hook Model]]** ([[Nir Eyal]]): four steps — trigger (external vs. internal/emotional), action (simplest behaviour via BJ Fogg's ability factors), [[Variable Rewards]] (tribe/hunt/self), investment (loads next trigger, stores value). Sources: [[Hooked How to Build Habit-Forming Products with Nir Eyal|Hooked How to Build Habit-Forming Products with Nir Eyal (Long)]], [[How to Build Habit-Forming Products - Nir Eyal|How to Build Habit-Forming Products - Nir Eyal (Short)]].
- **[[UX Psychology]]**: practical behavioural design levers for conversion moments — smart defaults, goal-gradient progress, reciprocity, ownership, loss framing, and contrast. Source: [[The UX Psychology Behind Apps People Can’t Stop Using]].

## Domain 5 — UX Strategy & Design Thinking

Four interconnected frameworks:

- **[[Kano Model]]** ([[Jared Spool]]): three satisfaction curves — basic expectations, performance payoff, excitement generators. The move from usable to delightful is additive, not subtractive. Source: [[Building a Winning UX Strategy Using the Kano Model - Jared Spool, at USI|Building a Winning UX Strategy Using the Kano Model - Jared Spool]].
- **[[UX Design Maturity Model]]** (Spool): five organisational stages from Dark Ages to Infused UX. Maturity is set by the least mature influencer. Source: [[Jared Spool – Beyond The UX Tipping Point]].
- **[[User Journey Mapping]]**: mapping all touchpoints on frustration-to-delight scale as the foundational tool for both frameworks above.
- **[[MAYA Principle]]** (Raymond Loewy): Most Advanced Yet Acceptable — the design sweet spot balancing neophilia and neophobia. Applied via the iPod→iPhone progression, Star Wars structure, and the failure of Google Glass. Sources: [[The MAYA Principle Design for the Future, but Balance it with Your Users’ Present|The MAYA Principle]], [[The Science of Successful Things Star Wars, Steve Jobs, and Google’s Epic Fail  Derek Thompson|The Science of Successful Things - Derek Thompson]].
- **[[Action Visibility in UX]]**: choose hidden, disabled, read-only, or enabled states based on whether an action is temporarily unavailable, permanently irrelevant, permission-restricted, or useful for workflow learning. Source: [[Hidden vs. Disabled In UX]].
- **Designing for AI**: [[Generative AI UX Design]] and the [[Human-AI Interaction Guidelines]] (18 research-validated guidelines across four interaction phases) cover how AI experiences should behave — focus frameworks (immersive/assistive/embedded), the human-in-control principle, avoiding anthropomorphization, and collaborative input/output design with *appropriate friction* as a deliberate counter to frictionless-design dogma. Sources: [[Creating a dynamic UX guidance for generative AI applications|Creating a Dynamic UX - Guidance for Generative AI Applications]], [[Guidelines for Human-AI Interaction]].

## Domain 6 — First Principles & Mental Models

- **[[First Principles Thinking]]**: identify assumptions → break to fundamentals → create new solutions. Contrasted with reasoning by analogy. Illustrated via Tesla/SpaceX ([[How to Use First Principles Thinking for Business]]), the airplane/rocket analogy ([[Airplane and Rocket Analogy]]), and Douglas Adams's epistemology of mental models ([[PDC 1996 Keynote with Douglas Adams]]).
- **[[Conflict De-escalation and Frame Control]]**: a communication model for diagnosing identity, control, and safety threats underneath conflict, then keeping the conversation framed around clarity, process, and shared outcome. Source: [[The Cheat Code for Controlling Conflict]].

## Domain 7 — Health, Wellness & Longevity

- **[[Diabetes and Metabolic Health]]**: blood glucose regulation, insulin signalling, type 1 vs. type 2 diabetes, insulin resistance, long-term complications, and type 2 remission. Source: [[The REAL Reason Diabetes Is So Dangerous]].
- **[[Longevity Exercise Pillars]]**: a balanced training model across strength, low-intensity cardio, high-intensity cardio, mobility, and balance. Source: [[You're Exercising Wrong]].
- **[[Bone Remodeling and Mechanical Loading]]**: bone is active tissue that adapts to repeated mechanical loading through osteoclast/osteoblast remodeling. Source: [[How Bones Get Stronger With Exercise]].
- **[[Vitamin D and Bone Health]]**: vitamin D3 synthesis through UVB exposure, liver and kidney activation, calcium absorption, deficiency risks, bone consequences, and supplementation/testing tradeoffs. Source: [[What Vitamin D REALLY Does to the Body]].
- **[[Tendon Load Management and Rehabilitation]]**: tendon capacity can lag behind muscular strength, so rehabilitation uses gradual load progression, movement-specific isometrics, and next-day symptom monitoring instead of complete rest. Source: [[Why Your Tendons Never Heal (And How To Fix Them)]].
  The newer E3 Rehab source adds a fuller rehab frame: tendinopathy terminology, pain as a dosage signal, load management, heavy slow resistance, energy storage/release work, return-to-sport progression, systemic recovery factors, and caution around passive adjuncts or injections. Source: [[How To Rehab Tendon Injuries & Pain (Exercises & Education for Tendinitis, Tendinosis, Tendinopathy)]].
- **[[Scaling Laws]]**: biological traits such as metabolism, heart rate, and lifespan often scale nonlinearly with body mass. The source covers surface-law vs. Kleiber's Law debate, WBE theory, lifetime heartbeat estimates, and an extension into city scaling. Source: [[Why does every mammal get 1 billion heartbeats in their life?]].
- **[[Cancer as a Mitochondrial Metabolic Disease]]** and **[[Glucose Ketone Index]]**: Thomas Seyfried's cancer-metabolism framework argues that cancer is driven by mitochondrial energy failure and glucose/glutamine fermentation dependency. The source connects this to GKI, ketogenic or fasting-like metabolic pressure, and press-pulse therapy claims, but these are medically high-stakes and should be treated as source-specific claims rather than standard-care guidance. Source: [[Leading Cancer Researcher They’re Ignoring My Research]].

## Domain 8 — Learning & Memory

- **[[Spaced Repetition]]**: active recall distributed across expanding review intervals. The practical method is to review near the “almost forgotten” point, make cards small, connected, and meaningful, and tie memory work to real activity. Source: [[spaced-repetition-notes|How To Remember Anything Forever-ish — Notes]].

## Domain 9 — Software Engineering & Architecture

- **[[System Design Fundamentals]]**: system design as tradeoff reasoning across statelessness, caching, CAP consistency/availability choices, queues, data guarantees, and API contracts. Source: [[900+ hours of Learning System Design in 9 Minutes]].

## Cross-domain connections

All nine domains share a deeper pattern: **compounding systems beat re-derivation**. The LLM wiki compounds knowledge. Spaced repetition compounds recall through successful retrieval at increasing intervals. Delta 4 products compound growth via UBP. The Flywheel compounds competitive advantages. ASO compounds search visibility, conversion, and review credibility. The Hook Model compounds habit strength through investment. UX maturity compounds organisational design capability. First principles unlock step-changes that analogy-based thinking cannot reach. System design compounds engineering judgment by turning repeated architecture situations into reusable tradeoff questions.

The MAYA Principle sits as a constraint across domains: it sets the acceptance ceiling for how quickly any of these compounding systems can advance user expectations in a single step.

The health and wellness sources add a biological version of the same compounding pattern: small repeated inputs such as training, glucose control, mobility work, gradual tendon loading, long-term skeletal loading, and mitochondrial-health behaviours accumulate into resilience and long-term independence. [[Scaling Laws]] adds the size dimension: larger systems can gain efficiency in some ways while amplifying costs, risks, or pace in others.
