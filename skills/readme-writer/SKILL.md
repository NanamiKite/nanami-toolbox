---
name: readme-writer
description: Write or rewrite a repository root README.md in natural Chinese or English. Use for project introductions, quick starts, feature summaries, usage examples, status notes, and documentation links. Do not use for API docs, architecture docs, CONTRIBUTING guides, release notes, product landing pages, or general technical writing.
---

# README Writer

Write repository root `README.md` files that sound like they were written by the project's maintainer.

## When to use

Use this skill when the task is to:

- create a project `README.md`
- rewrite or simplify an existing root README
- improve README structure or wording
- produce Chinese, English, or bilingual README content

Do not use it for:

- API/reference documentation
- design or architecture documents
- CONTRIBUTING guides
- changelogs or release notes
- tutorials
- product marketing pages
- generic Markdown editing unrelated to a project README

## Before writing

Inspect the repository and existing documentation.

Use verified project behavior as the source of truth. Do not invent features, compatibility, commands, performance claims, or project status.

## Writing rules

Treat the README as the project's front page, not its complete manual.

A reader should quickly understand:

1. what the project is
2. what it can do
3. how to try it
4. where to find more details

Prefer concrete facts, commands, screenshots, and examples over abstract descriptions.

Keep implementation details, long limitations, architecture, testing policy, migration notes, and troubleshooting in dedicated documentation when possible.

Do not list every feature just because it exists.

## Style

Write naturally and directly.

Avoid corporate or AI-style filler such as:

- 旨在 / 致力于 / 赋能 / 一站式 / 强大而灵活
- seamless / powerful and flexible / robust solution / feature-rich
- unnecessary “not only ... but also ...” constructions
- conclusions that merely repeat the previous paragraph

Do not attach disclaimers and qualifications to every sentence.

Write Chinese as natural Chinese technical prose, not translated English.

Write English as straightforward developer English, not marketing copy.

For bilingual README files, keep facts consistent but do not translate sentence by sentence.

## Structure

Choose sections based on the project. Do not force a fixed template.

A common order is:

```text
Project name
Short description
Screenshot/demo if useful
Highlights
Quick start
Examples
Current status if necessary
Documentation
Development / Contributing
License
```

Remove sections that do not help a new reader.

## Final check

Before finishing:

- remove repetition and filler
- remove unnecessary adjectives
- move deep details out of the root README
- verify commands and links
- remove unsupported claims

The first 20–30 lines should be enough for a new visitor to understand the project.

Prefer a shorter README that leads readers to good documentation over a complete README that tries to contain everything.