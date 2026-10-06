---
name: oss-contribution-writer
description: Draft or revise open-source issues, pull requests, and review replies to be concise, evidence-led, and easy to review.
---

# OSS contribution writing

Use this skill for issues, pull requests, and maintainer-facing review replies.

Do not use it for README files, design docs, architecture docs, or general technical documentation.

## Principles

Write like a contributor communicating work they actually understand and participated in.

Prioritize reviewer time over completeness.

Prefer concrete evidence over generic claims:

- what was observed
- what was changed
- what was personally tested
- what remains uncertain
- what the maintainer needs to decide

Use first person when it makes real participation clearer:

- `I tested...`
- `I found...`
- `I traced this to...`
- `I left this disabled because...`

Never invent tests, observations, motivations, or certainty.

Keep observations separate from interpretations.

## Issues

Usually include:

1. the problem or observation
2. enough evidence to understand or reproduce it
3. the current interpretation, if useful
4. the question or proposed direction

Do not turn a focused issue into a full engineering report.

## Pull requests

Explain the diff, not the whole investigation.

Usually include:

- what the patch changes
- an important implementation choice, if needed
- concrete validation
- a real unresolved question, if one exists

Reference the linked issue instead of repeating it.

Small PRs should usually stay short.

## Style

Avoid automatic report sections such as:

`Summary / Scope / Implementation / Risks / Future work / Validation matrix`

unless the contribution genuinely needs them.

Avoid generic filler such as:

`This PR aims to...`
`This change introduces...`
`This improves robustness and maintainability.`
`Key benefits include...`

Prefer specific statements about the actual work.

Do not fake informality, slang, mistakes, or uncertainty just to sound human.

## Reviewability

If repository context is available, flag obvious review problems such as:

- unrelated commits
- add-then-revert noise
- unrelated refactors
- large generated or formatting churn
- a PR that should probably be split

Do not hide scope problems behind polished prose.

Before returning the text, remove anything that does not help the maintainer understand, verify, or review the contribution.