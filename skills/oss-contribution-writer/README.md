# OSS Contribution Writer

起草和修改开源项目里的 issue、pull request 和 review 回复，让内容简洁、以证据为主、方便维护者审阅。

指令本体见 [SKILL.md](SKILL.md)。

## 适用

- 给上游提 bug 或 feature issue
- 写 PR 描述
- 回应维护者的 review 意见

不适用：README、设计文档、架构文档等一般技术文档——那些用 engineering-doc-clarifier 或 readme-writer。

## 规则要点

- 像真正参与过这项工作的人那样写，把维护者的时间放在第一位
- 写具体证据：观察到了什么、改了什么、亲自测了什么、还有什么不确定、需要维护者决定什么
- 该用第一人称就用：I tested... / I found... / I traced this to...
- 不编造测试、观察、动机和确定性
- 观察和解释分开写

issue 聚焦问题和复现证据，不写成完整工程报告；PR 描述解释 diff 本身，不复述整个调查过程，小的 PR 保持简短。

避免模板化的 Summary / Scope / Implementation / Risks 段落，避免 "This PR aims to..."、"This improves robustness and maintainability." 这类空话。

## 使用

把本目录放进你的 agent 的 skills 目录。当你要求起草 issue、PR 描述或 review 回复时，agent 会自动选用它。
