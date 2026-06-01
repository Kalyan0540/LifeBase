---
type: source
source_title: "How I Vibe Coded a Recipe App using Claude Code (Full Build + Marketing)"
source_url: "https://www.youtube.com/watch?v=9atd5lczG2k"
raw_path: "raw/knowledge/technology/ai/How I Vibe Coded a Recipe App using Claude Code (Full Build + Marketing).md"
created: 2026-06-01
updated: 2026-06-01
---

# How I Vibe Coded a Recipe App using Claude Code

Jason Lee walks through building a ReciMe-style recipe app with AI-assisted design and code generation. The video is less about recipes specifically and more about a repeatable workflow for building, testing, and preparing a mobile app with AI tools.

## Product Pattern

The reference app lets users import recipes from websites, YouTube videos, or photos. AI extracts ingredients, steps, metadata, and sometimes calories into clean recipe cards.

The stickiness comes from the user's saved recipe library. As the library grows, switching away becomes harder.

## Build Workflow

The workflow has four stages:

1. Research the reference product and ask the coding agent for a feature breakdown.
2. Use a dedicated design tool to generate high-fidelity mobile screens from that feature spec and visual references.
3. Bring the design files into Claude Code or Codex and ask it to implement the app with Expo React Native and TypeScript.
4. Add backend functionality, AI calls, local testing, database, payments, and app-store preparation.

The suggested stack:

- Expo React Native for iOS/Android mobile development
- local device storage for early saved data
- small Node/Express backend for AI calls so API keys stay off the phone
- OpenAI API for recipe extraction and transformation
- Supabase for production data storage
- RevenueCat for subscriptions
- Expo Go for real-phone preview

## AI Features

The app can use AI to extract recipes from links or images, scan handwritten or printed recipes, estimate calories, generate recipe cards, and make a recipe healthier by suggesting substitutions.

## Marketing Notes

The suggested marketing approach starts with competitor acquisition channels, especially short-form video.

Three options are named:

- create organic short-form content
- pay UGC creators
- use AI-generated UGC personas, then put ad spend behind winners

The key lesson is that building the app is only part of the job; distribution needs to be designed too.

## App Store Readiness

The video warns that AI-built apps can fail review if they lack reliability, security, and production-quality safeguards. It recommends using a checklist before submission.

---

*Concepts: [[AI-Assisted App Building]] · [[Deploying AI-Generated Websites]]*
*Updated: 2026-06-01*
