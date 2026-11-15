# Nanamiの妙妙工具

一些我自己会用，也可能对别人有用的小工具。

这里主要收录：

- AI / Agent skills
- 开发辅助脚本
- 文档处理工具
- 小型 CLI
- 零散但实用的工程工具

不值得单独开一个仓库，但又确实能解决问题的东西，会放在这里。

## Skills

目前有三个，都是写作相关的 agent skill。索引和选型见 [skills/README.md](skills/README.md)。

## Repository Structure

```text
.
└── skills/
    ├── README.md     # skill 索引
    ├── engineering-doc-clarifier/
    │   ├── SKILL.md    # agent 指令
    │   └── README.md   # 功能说明
    ├── oss-contribution-writer/
    │   ├── SKILL.md
    │   └── README.md
    └── readme-writer/
        ├── SKILL.md
        └── README.md
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

MIT，见 [LICENSE](LICENSE)。