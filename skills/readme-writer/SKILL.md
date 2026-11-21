---
name: readme-writer
description: Write or rewrite a repository root README.md in Chinese, English, or bilingual form like a maintainer—clear repo front-door navigation with grounded prose. Not for API/architecture docs, CONTRIBUTING, changelogs, reports, or marketing.
---

# README Writer

Write a root `README.md` as both a clear repository front door and a maintainer explaining the project to a peer. Keep prose concrete and asymmetric; scale layout only to match project scope.

## Before Writing

- Inspect repo/docs first. Never invent features, commands, compatibility, metrics, badges, or status; use `<placeholder>` for missing essentials.
- Scope: root `README.md` only (no reports, API/architecture docs, tutorials, or marketing).

## Core Writing Rules

Help visitors quickly grasp what it is, why it exists, what it does, how to use it, and where deeper docs live.

- **Concrete over abstract**: Describe actions, not stacked nouns (`evidence`, `characterization`, `feasibility`, `integration`, `validation`, `workflow`). Do not invent motivation.
  - *Bad*: "Provides hardware-validation evidence for downstream integration."
  - *Better*: "Talks to the hardware directly and records results for testing."
- **No report-style prose**: Drop milestones (`M0`, `M4`), handoffs, agent instructions, acceptance gates, and phase jargon.
  - *Bad*: "M4 closed as a host-DSP feasibility result. M6/TX has not started."
  - *Better*: "Receive experiments work. Transmit support has not started yet."
- **No over-qualification**: State normal behavior; put caveats next to affected steps. Avoid repeating `currently`, `verified`, `tested`, `optional`, `read-only`, `supported`, `depending on`.
- **No forced symmetry**: Do not pad sections or bullets for equal length, grammar, or taglines; uneven is fine.
- **No redundant navigation**: Never echo filenames (`Architecture | Architecture design`). Link inline, add context, or use an intent index.
- **Natural style**:
  - Ban AI/corporate filler (`旨在`, `致力于`, `赋能`, `一站式`, `强大而灵活`, `seamless`, `robust solution`, `powerful and flexible`, `feature-rich`, `blazingly fast`, "not only ... but also ...").
  - Skip decorative emojis unless repo-consistent; cut lines merely summarizing the prior sentence.
  - Write idiomatic Chinese or developer English. For bilingual READMEs, keep facts aligned and rewrite naturally.

## Repository Front-Door Defaults

A README is a landing entry point, not an internal dev log. Apply these lightweight defaults to public repos:

- **Scannable header**: Title, 1–2 line summary, verified badges (if applicable), and a compact jump bar (`Download · Quick Start · Docs · Issues`).
- **Early visual**: Place a screenshot, GIF, or CLI output near the top when available.
- **User-first flow**: Lead with value and usage before caveats. Split end-user entry (Releases/install) from source builds; fold verbose build, driver, or telemetry steps into `<details><summary><b>...</b></summary></details>`. Put status/limitations *after* usage so they inform without blocking the door.

## Scale-Up Patterns (Large Projects Only)

Use selectively for mature apps or self-hosted platforms; skip for small tools, libs, or early experiments:

- **Adaptive hero**: Centered `<div align="center">` with `<picture>` (`prefers-color-scheme: dark`, `prefers-reduced-motion: reduce`, GIF->SVG) for dark/animated logos, plus language links.
- **Workflow grouping**: Group large feature sets by adoption path (setup, run, observe, self-host), not code modules; keep lengths uneven.
- **Compact lookups**: Paired columns (`Provider | CLI | Provider | CLI`) for >8 items; `I want to... | Start here` for >=6 docs; 75–85 char ASCII topology + `Layer | Stack` table; 1–2 plain sentences for custom licenses (`LICENSE`/`NOTICE`).

## Final Pass

Reread as a first-time visitor. Cut reports, proposals, handoffs, raw feature inventories, SaaS pitches, and template filler. Keep layout elements only if they reduce friction.