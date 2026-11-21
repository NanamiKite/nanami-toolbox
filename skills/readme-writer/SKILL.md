---
name: readme-writer
description: Write or rewrite a repo root README.md (ZH/EN/bilingual) like a maintainer—clear front-door navigation, grounded prose. Not for API/arch docs, CONTRIBUTING, changelogs, reports, or marketing.
---

# README Writer

Write a root `README.md` as a repo front door in a maintainer's voice: what it is, why it exists, what it does, how to use it, and deeper docs. Keep prose concrete and asymmetric.

## Before Writing

- Inspect repo/docs first; never invent features, commands, compatibility, metrics, badges, or status (`<placeholder>` if missing). Root `README.md` only (no reports, API/arch docs, tutorials, or marketing).

## Core Writing Rules

- **Concrete over abstract**: Describe actions, not stacked nouns (`evidence`, `characterization`, `feasibility`, `integration`, `validation`, `workflow`); don't invent motivation.
  - *Bad*: "Provides hardware-validation evidence for downstream integration."
  - *Better*: "Talks to hardware directly and records results for testing."
- **No report-style prose**: Drop milestones (`M0`, `M4`), handoffs, agent notes, acceptance gates, phase jargon.
  - *Bad*: "M4 closed as a host-DSP feasibility result. M6/TX has not started."
  - *Better*: "Receive experiments work. Transmit support has not started yet."
- **No over-qualification**: State normal behavior; put caveats by affected steps. Avoid repeating `currently`, `verified`, `tested`, `optional`, `read-only`, `supported`, `depending on`.
- **No forced symmetry**: Uneven sections/bullets are fine; never pad for balance.
- **No redundant navigation**: Never echo titles (`Architecture | Architecture design`); link inline or add context.
- **Natural style**: Ban AI/corporate filler (`旨在`, `致力于`, `赋能`, `一站式`, `强大而灵活`, `seamless`, `robust solution`, `powerful and flexible`, `feature-rich`, `blazingly fast`, "not only...but also..."). No decorative emojis/summary filler; use idiomatic ZH/EN, rewrite bilingual docs naturally.

## Repository Front-Door Defaults

- **Scannable header**: Title, 1–2 line summary, badges, and jump bar (`Download · Quick Start · Docs · Issues`).
- **Badges by repo form (0–4, 1 row, `style=flat`, clickable)**: Verify targets; never guess `ci.yml` or emit `0`/`not found`/red CI.
  - *Desktop/binary*: Release (`/releases/latest`), CI, Downloads (real volume), 1 OS limit.
  - *Library/CLI/Plugin*: Registry/store version or installs (npm/PyPI/crates.io/Marketplace), docs, CI, License.
  - *Self-hosted/Docker*: Release, public pulls/size, CI, License.
  - *Early/PoC*: CI + License, or none.
  - *Ban*: Tech-stack walls, `PRs Welcome`, redundant stats (`Repo Size`, `Top Language`), low-count `Stars` unless asked.
- **Early visual**: Put a screenshot, GIF, or CLI output near the top if available.
- **User-first flow**: Lead with value and usage. Split Releases/install from source builds; fold verbose build/driver/telemetry steps in `<details><summary><b>...</b></summary></details>`. Put limits *after* usage.

## Scale-Up Patterns (Large Projects)

For mature apps/platforms only; skip for small tools, libs, or PoCs:

- **Adaptive hero**: `<div align="center">` + `<picture>` (`prefers-color-scheme: dark`, `prefers-reduced-motion: reduce`, GIF->SVG) for dark/animated logos + language links.
- **Workflow grouping**: Group large features by adoption path (setup, run, observe, self-host), not modules.
- **Compact lookups**: Paired columns (`Provider | CLI | ...`) if >8 items; `I want to... | Start here` if >=6 docs; 75–85 char ASCII topology + `Layer | Stack`; 1–2 plain lines for custom licenses (`LICENSE`/`NOTICE`).

## Final Pass

Reread as a first-time visitor. Cut reports, handoffs, feature lists, SaaS pitches, and filler; keep layout only if it cuts friction.