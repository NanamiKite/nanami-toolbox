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

### OSS Contribution Writer

用于起草和修改开源项目里的 issue、pull request 和 review 回复，让内容简洁、以证据为主、方便维护者审阅。

- 写得像一个真正参与过这项工作的人在沟通
- 优先写清楚：观察到了什么、改了什么、亲自测了什么、还有什么不确定
- 不编造测试、观察和结论
- 不用模板化的报告段落和空话填充

不用于 README、设计文档等一般技术文档。

### README Writer

用于编写或重写仓库根目录的 README.md，支持中文和英文。

- 让新读者快速看懂：项目是什么、能做什么、怎么试用、去哪找更多文档
- 用自然的语言写，避免报告腔和产品宣传腔
- 不发明仓库里不存在的功能、命令和进度

不用于架构文档、API 文档、CONTRIBUTING、changelog 这类文档。

## Repository Structure

```text
.
└── skills/
    ├── engineering-doc-clarifier/    # 技术文档重写
    ├── oss-contribution-writer/      # 开源 issue / PR / review 写作
    └── readme-writer/                # 仓库 README 写作
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