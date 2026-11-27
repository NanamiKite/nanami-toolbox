---
name: engineering-doc-clarifier
description: Rewrite and clarify English or Chinese technical documentation (architecture, design, protocol, API/CLI, roadmap, troubleshooting) while stripping AI/agent collaboration artifacts, worklog receipts, and defensive contract-style disclaimers.
---

# Engineering Documentation Clarifier

Improve the clarity and readability of technical documentation without changing its technical meaning, and strip AI/agent collaboration artifacts so docs read like they were written by a real engineer.

Supports English and Chinese engineering documentation.

## When to use

Use this skill when the user asks to:

- rewrite, polish, simplify, clarify, or improve technical documentation;
- improve the readability of a README, architecture document, design document, protocol description, API/CLI documentation, roadmap, changelog, installation guide, troubleshooting guide, or engineering notes;
- remove AI/agent collaboration traces, defensive disclaimers, or worklog-style boilerplate from project docs ("de-AI" / humanize docs);
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
- real limitations, uncertainty, and known gaps (expressed concisely once, without repetitive hedging);
- `must` / `should` / `may` / `can` distinctions and Chinese equivalents;
- commands, APIs, identifiers, state names, error names, protocol terms, paths, numbers, versions, and code;
- headings, lists, tables, code blocks, links, and document order unless restructuring or removing AI boilerplate is requested.

Use consistent terminology, but only normalize terms when they clearly refer to the same concept.

If the source is ambiguous, do not guess.

## Strip AI and Agent Artifacts

When clarifying or humanizing project documentation, actively remove traces left by AI coding agents:

1. **Remove agent worklogs and permission receipts**:
   - Delete sentences where an assistant reports back to a user or proves compliance with session rules (e.g., "按用户要求…", "经用户授权/获准运行…", "本批仅完成静态检查，未运行测试", "没有使用付费 API / 未修改虚拟环境", "已清理临时目录", "不拼成全项目通过数", "do not infer X from compilation", "this is not a replacement for Y").
   - Strip internal evidence-grading tags or prompt instructions leaked into public docs (such as `VERIFIED_FROM_DEVICE`, `VERIFIED_FROM_APK`, `INFERRED`, or "A receive-side schema does not authorize sending...").

2. **Eliminate defensive "X is not Y" disclaimer chains**:
   - Keep real limitations and unimplemented features, and consolidate them into a short, plain `Known Limitations` / `TODO` list (e.g., "Windows installer is still experimental; run from source for now").
   - Delete repetitive legalistic hedging appended to every section (e.g., "连接成功不代表模型支持工具调用", "源码构建成功不代表安装包可用", "接口返回成功不表示数据已备份", "A log timestamp is not proof that the machine clock was correct", "a visible control does not mean every operation has been hardware-accepted"). State normal behavior directly instead of endlessly defining what something is *not*.

3. **Simplify mechanical contract tables and internal jargon**:
   - Simplify rigid `| Component | Owns | Must not own |` (`| 组件 | 负责 | 不负责 |`) tables into straightforward responsibility descriptions; drop the "Must not own / 不负责" column unless a specific boundary is non-obvious and critical to prevent bugs.
   - Replace internal AI-workflow jargon (`Gate 2`, `Stage 3b`, `M4`, `handoff`, `acceptance ledger`, `双轨防破防`, `语料治理与确定性质检`) and uniform 4-character bold bullet prefixes (`运行时与状态分离：`, `异构实时协议接入：`) with plain, direct engineering prose.

4. **Never introduce new AI artifacts (and flag repo scaffolding)**:
   - Never append meta-disclaimers to any document after editing (do not write "Only documentation was updated; tests were not re-run").
   - When cleaning a whole repository for public sharing, check for non-product AI scaffolding files (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, `implementation_plan.md`, `.ai/`, `.codex/`, `.cursor/`) and flag them for removal or `.gitignore` (distinguishing them from product-owned skill directories if the app itself uses skills).

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
- reduce long modifiers and nested "的" structures;
- avoid empty formal wording such as unnecessary "进行", "实现", "相关", "对应", and "相应", as well as repetitive four-character bold headers;
- keep precise technical terms unchanged.

Do not mechanically shorten every sentence. Preserve natural paragraph flow and tightly related technical logic.

## Output

Return or update the rewritten document directly.

Do not explain individual edits or add testing disclaimers to the document unless the user asks for a comparison or review.
