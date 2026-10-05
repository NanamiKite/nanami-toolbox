# Nanamiの妙妙工具

一些我自己会用，也可能对别人有用的小工具。

这里主要收录：

- AI / Agent skills
- 开发辅助脚本
- 文档处理工具
- 小型 CLI
- 零散但实用的工程工具

不值得单独开一个仓库，但又确实能解决问题的东西，会放在这里。

## Tools

### Engineering Documentation Clarifier

用于重写中英文技术文档，提高可读性，同时尽量保持原有技术语义不变。

适用于：

- README
- Architecture / Design 文档
- API / CLI 文档
- Protocol 文档
- Installation Guide
- Troubleshooting
- Engineering Notes

主要原则：

- 保留技术含义、约束和证据强度
- 不擅自修改 API、命令、状态名和技术术语
- 减少长句、歧义和空泛表达
- 英文参考 ASD-STE100 的部分写作原则
- 中文使用对应的工程写作规则
- 不把技术文档润色成营销文案

目录：

```text
skills/
└── engineering-doc-clarifier/
    └── SKILL.md
```

## Repository Structure

```text
.
├── skills/      # AI / Agent skills
├── scripts/     # 开发和系统辅助脚本
├── cli/         # 小型命令行工具
├── snippets/    # 可复用的小片段
└── docs/        # 说明和示例
```

目录会随着工具增加而调整，不强行维持固定分类。

## Philosophy

这里的工具通常满足至少一个条件：

- 解决一个明确的小问题
- 可以重复使用
- 比每次手工处理更省事
- 不值得单独维护成一个完整项目

如果某个工具逐渐变成独立项目，它可能会从这里搬出去。

## License

See `LICENSE`.