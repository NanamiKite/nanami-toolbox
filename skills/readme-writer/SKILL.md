---
name: readme-writer
description: Write or rewrite a repository root README.md in natural Chinese or English. Use for project introductions, quick starts, usage examples, current status, and links to further documentation. Do not use for architecture docs, API/reference docs, CONTRIBUTING guides, changelogs, release notes, project reports, or marketing pages.
---

# README Writer

Write the root `README.md` like the project's maintainer explaining it to another person.

## Use this skill for

- creating a project README
- rewriting or simplifying an existing README
- improving README structure or wording
- Chinese, English, or bilingual README content

Do not use it for internal project reports, milestone summaries, architecture documents, API docs, CONTRIBUTING guides, changelogs, tutorials, or marketing copy.

## Before writing

Inspect the repository and relevant docs first.

Do not invent features, commands, compatibility, performance, project status, or completed work.

## README rules

The README is the project's front page, not a project report.

A new reader should quickly understand:

- what the project is
- why it exists or what problem it solves
- what they can actually do with it
- how to try it
- where to find deeper documentation

Prefer concrete examples and ordinary language over classifications and exhaustive descriptions.

A short explanation of why the maintainer built the project is often more useful than a formal product definition.

Bad:

> A Rust engineering workbench for hardware characterization, evidence collection, feasibility analysis, and downstream integration.

Better:

> I built this to make it easier to poke at the radio hardware I had on hand and keep the experiments reproducible.

Do not invent a personal motivation if the repository does not provide one. In that case, simply explain what the project is useful for.

## Avoid report-style writing

Do not expose internal planning language unless users genuinely need it.

Avoid things like:

- milestone numbers such as M0, M4, M6
- handoff notes
- agent instructions
- internal acceptance gates
- implementation-phase terminology
- status phrased like an engineering progress report

Translate internal state into something useful to a reader.

Instead of:

> M4 closed as a host-DSP integration-feasibility result. M6/TX feasibility has not started.

Prefer something like:

> Receive-side experiments are working. Transmit support has not been explored yet.

## Prefer concrete words

Avoid stacking abstract nouns.

Words such as `evidence`, `characterization`, `feasibility`, `integration`, `validation`, `restoration`, `architecture`, and `workflow` are fine when they are actually the clearest word, but several of them in one sentence usually make the README sound artificial.

Prefer describing what happens.

Bad:

> The platform provides hardware-validation evidence for prospective downstream integration.

Better:

> It can talk to the hardware directly and record the results for later testing.

## Do not over-qualify every sentence

README prose does not need to encode every edge case.

State the normal behavior clearly. Put important exceptions next to the setup or feature they affect, or link to detailed documentation.

Avoid repeatedly adding words such as:

- currently
- verified
- tested
- optional
- read-only
- supported
- depending on
- provided that

Use them only when the distinction matters to someone deciding whether or how to use the project.

## Do not force symmetry

Sections do not need equal length.

Bullets do not need identical grammar.

Not every feature needs one sentence.

Not every heading needs a paragraph.

Do not make the README look artificially balanced just because a template suggests it.

If one important topic needs ten lines and another needs one, that is fine.

## Avoid redundant navigation

Do not add a documentation table whose descriptions merely repeat the document titles.

Bad:

| Document | Contents |
| --- | --- |
| Architecture | Architecture design |
| Testing | Testing information |

Prefer a short list with meaningful context, or just link the documents directly.

## Style

Write naturally and directly.

Avoid generic AI or corporate phrasing such as:

- 旨在 / 致力于 / 赋能 / 一站式 / 强大而灵活
- seamless / robust solution / powerful and flexible / feature-rich
- unnecessary “not only ... but also ...” constructions

Do not add a concluding sentence merely to summarize the previous sentence.

Chinese should read like native Chinese technical writing.

English should read like straightforward developer English.

For bilingual READMEs, keep facts consistent but rewrite naturally rather than translating sentence by sentence.

## Structure

Do not force a fixed template.

A README often contains some of these:

```text
Project name
One or two natural introductory paragraphs
Screenshot or demo
What it can do
Quick start
Examples
Important limitations
Documentation
Development / Contributing
License
```

Use only the sections the project needs.

Keep deep implementation details, architecture, exhaustive compatibility notes, migration plans, test matrices, and troubleshooting in dedicated docs when possible.

## Final pass

Reread the README as if you had just discovered the repository.

Remove anything that sounds like:

- a project proposal
- a status report
- an agent handoff
- a feature inventory
- legalistic qualification
- documentation generated to fill every expected section

Also remove repetition, unnecessary adjectives, unsupported claims, and details that belong in secondary docs.

Do not optimize for completeness or structural neatness.

Optimize for the feeling that a real maintainer sat down and explained the project because they wanted someone else to understand and use it.