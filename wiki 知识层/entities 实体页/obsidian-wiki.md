---
type: entity
summary: "obsidian-wiki 是一个用 Python 实现的 Obsidian 知识库框架，把 Karpathy 式 LLM Wiki 的三层结构直接落到本地 Markdown 工作流中。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
updated: "2026-06-15"
---

# obsidian-wiki

## 类型

- 项目
- Obsidian 知识库框架

## 本次新增信息

- 它把 `raw notes + compiled wiki + schema file` 做成了可执行框架。
- 项目定位是让 AI Agent 直接在 Obsidian 中维护 Karpathy 风格的 LLM Wiki。
- 技术实现基于 Python，强调 Markdown 与本地文件工作流。

## 为什么值得记录

- 这和当前知识库结构几乎同构，是极少数与本库方向直接重叠的公开项目。
- 它说明“Obsidian + LLM Wiki + Agent 自动维护”已经从概念进入框架化阶段。

## 关联概念

- LLM Wiki
- Obsidian 自动化
- 知识库编译
- 第二大脑

## 对当前知识库的启发

- 当前本库的 `raw 原始资料/`、`wiki 知识层/`、`TheSchema.md` 已经形成相似结构。
- 后续可以比较它的工作流编排、页面模板和自动更新策略，看哪些值得借鉴。
