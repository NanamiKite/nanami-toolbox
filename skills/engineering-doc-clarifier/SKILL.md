# Engineering Documentation Clarifier

Improve the clarity and readability of technical documentation without changing its technical meaning.

Supports English and Chinese engineering documentation.

## When to use

Use this skill when the user asks to:

- rewrite, polish, simplify, clarify, or improve technical documentation;
- improve the readability of a README, architecture document, design document, protocol description, API/CLI documentation, installation guide, troubleshooting guide, or engineering notes;
- make Chinese or English technical writing more precise and easier to read;
- apply ASD-STE100-inspired writing principles to engineering documentation.

Do not use this skill for:

- creative writing;
- marketing copy;
- ordinary conversation;
- code refactoring;
- requests that primarily require changing the technical design rather than improving its documentation.

## Rules

Preserve technical meaning.

Do not add new facts, conclusions, assumptions, architecture, or implementation details.

Preserve:

- requirements and constraints;
- uncertainty and evidence strength;
- `must` / `should` / `may` / `can` distinctions and Chinese equivalents;
- commands, APIs, identifiers, state names, error names, protocol terms, paths, numbers, versions, and code;
- headings, lists, tables, code blocks, links, and document order unless restructuring is explicitly requested.

Use consistent terminology, but only normalize terms when they clearly refer to the same concept.

If the source is ambiguous, do not guess.

## English

Use ASD-STE100-inspired principles without requiring strict STE compliance:

- prefer direct sentences;
- make subjects and conditions explicit;
- use active voice when it improves clarity;
- prefer simple common words;
- split dense sentences when useful;
- avoid vague, decorative, and marketing language.

## Chinese

Use equivalent natural engineering-writing principles:

- keep sentences compact;
- make conditions, actions, and results explicit;
- prefer direct verbs;
- reduce long modifiers and nested “的” structures;
- avoid empty formal wording such as unnecessary “进行”, “实现”, “相关”, “对应”, and “相应”;
- keep precise technical terms unchanged.

Do not mechanically shorten every sentence. Preserve natural paragraph flow and tightly related technical logic.

## Output

Return the rewritten document directly.

Do not explain individual edits unless the user asks for a comparison or review.