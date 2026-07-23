---
type: entity
summary: "datasette-agent-edit 是 Simon Willison 为 Datasette Agent 生态发布的基础编辑插件，把文本修改抽象为可复用的查看、精确替换和插入工具。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-08-zh.md"
  - "raw 原始资料/projects 项目资料/Horizon/data/last-run.log"
updated: "2026-06-15"
---

# datasette-agent-edit

## 类型

- 项目
- agent 工具插件

## 本次新增信息

- 2026-06-07 发布 `0.1a0` 预发布版本。
- 其目标不是做完整编辑器，而是给其他 Datasette Agent 插件提供抽象编辑工具。
- 核心动作围绕 `view`、`str_replace`、`insert` 三类文本修改原语。

## 为什么值得记录

- 它代表一种更稳的 agent 执行策略：不是自由生成整份文件，而是把修改限制在少数可验证动作里。
- 这类设计对知识库自动维护、SQL 改写、Markdown 协作编辑都很有参考价值。

## 关联概念

- [[wiki 知识层/concepts 概念页/Agentic 文本编辑原语]]
- agent
- llm-tool-use
- datasette

## 关注点

- 它是否会扩展出更丰富的编辑约束和差异预览能力。
- 这套原语是否能迁移到 Obsidian、本地助手、MCP 工具链中。
