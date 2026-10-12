# Vibe Coding Workflow

一套给编程初学者的 AI 开发流程：从一句想法走到可运行、可验证、可发布的网页或 macOS 应用。你负责描述想法和判断体验，AI 负责调查、方案、实现和验证。

## 怎么用

1. 把 [`AGENTS.md`](AGENTS.md) 放进你的项目根目录（或把内容贴进项目已有的 `AGENTS.md` / `CLAUDE.md`）。
2. 对你的 AI 编程助手说：

   > 我想做一个网页／macOS 应用，主要帮我解决……，给……使用。我不懂代码，请按项目里的 AGENTS.md 流程推进，每次实际改动顺带解释一个概念。

3. 需要了解每个阶段你该做什么、AI 该交付什么时，读 [`docs/完整开发流程.md`](docs/完整开发流程.md)。
4. AI 在新产品或大功能上会按 [`templates/`](templates/) 里的模板写出可审查的规格，你确认后再开工。

适用于 Codex、Claude Code、Cursor、zCode 等读取 `AGENTS.md` 的工具。不读取该文件的工具，把 `AGENTS.md` 全文贴进对话开头即可。

## 流程一览

**想法 → 用户任务与范围 → 可审查规格（Spec Lock）→ 视觉与交互方向 → 一条完整功能 → 反馈迭代 → 验收 → 部署／分发 → 公布与反馈。**

| 规模 | 走法 |
|---|---|
| 新产品／大功能 | 完整链条，先出可审查方案，你批准后才写代码 |
| 已批准的范围 | 直接继续，不重复确认 |
| 错别字、孤立 Bug | 直接修复并验证，不建规格包 |

## 这套流程强调什么

- **先锁定范围再动手**：新产品先写清做什么、不做什么、怎么验收，你点头之后 AI 才能改代码。
- **一次打通一条完整路径**：例如“填写 → 校验 → 保存 → 刷新后仍能读到”，而不是先把所有界面画完。
- **证据分开记**：功能是否正确、你是否满意外观、是否已部署、是否已公布，是四件不同的事，不能互相代替。
- **边做边学**：每个可验证的小步只解释一个和本次改动相关的概念。
- **小修复保持轻量**：一行 Bug 不需要五份文档。

## 仓库内容

| 文件 | 用途 |
|---|---|
| [`AGENTS.md`](AGENTS.md) | 给 AI 的工作指令，流程的可执行版本 |
| [`docs/完整开发流程.md`](docs/完整开发流程.md) | 给人读的阶段说明 |
| [`templates/`](templates/) | brief、spec、plan、tasks、verification、DESIGN 模板 |

## 来源

这套流程综合了几位实践者公开的方法，并做了面向初学者的简化：

- [Matt Pocock 的 skills](https://github.com/mattpocock/skills)：可审查规格、小步实现、测试驱动、变更审查、交接。
- [Paul Bakaus 的 Impeccable](https://github.com/pbakaus/impeccable)：先读上下文、检查真实界面、再做有限修整。
- [Simon Willison](https://simonwillison.net/2026/Jul/2/llm-coding-agent/)：明确规格、小改动、可重复测试与真实手测。
- [Addy Osmani 的 agent-skills](https://github.com/addyosmani/agent-skills)：规划、实现、审查、交付分层。
- [Shape Up](https://basecamp.com/shapeup/1.5-chapter-06)：明确问题、投入边界与不做项（不照搬其团队周期）。

这是个人实践中整理的组合，**没有证据表明它一定比你现有的做法更好**。用的时候以你的项目实际结果为准。

## 许可

[MIT](LICENSE)。Matt Pocock skills 等上游内容有各自的许可证，本仓库只描述方法，不包含那些上游文件。
