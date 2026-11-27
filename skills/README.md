# Skills

本目录下的 AI / Agent skills，都与写作相关，各管一块：

- [engineering-doc-clarifier](engineering-doc-clarifier/README.md) —— 重写中英文技术文档并清除 AI 协作痕迹与防御性免责腔，保持技术语义不变
- [oss-contribution-writer](oss-contribution-writer/README.md) —— 写开源项目的 issue、pull request 和 review 回复
- [readme-writer](readme-writer/README.md) —— 写或重写仓库根目录的 README

每个 skill 目录里有两个文件：

- `SKILL.md`：给 agent 用的指令本体
- `README.md`：给人看的功能说明（适用范围、规则要点、使用方式）

## 怎么选

三个 skill 都涉及“写文档”，按要写的东西选：

- 改技术文档（README、架构 / 设计文档、Roadmap、API / CLI 文档、安装指南、工程笔记）或给文档去 AI 痕迹 → **engineering-doc-clarifier**
- 提 issue、写 PR 描述、回 review 意见 → **oss-contribution-writer**
- 写或重写某个仓库的根 README → **readme-writer**