---
type: entity
summary: "Recall 是一个面向 Claude Code 的本地离线项目记忆工具，目标是减少每次会话都要重新解释仓库上下文的成本。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-22-raw-candidates.md"
updated: "2026-06-22"
---

# Recall

## 类型

- 项目
- 本地 Agent 记忆工具

## 本次新增信息

- 项目定位是给 Claude Code 提供持久化项目记忆。
- 核心卖点是完全离线，强调减少重复解释项目背景和重复消耗 token。
- 这类工具不是通用聊天历史，而是更接近“当前仓库 / 当前任务”的本地记忆层。

## 为什么值得记录

- 它把“编码代理的跨会话连续性”做成了独立产品方向。
- 对项目开发、代码协作和自动化知识库来说，这类记忆层比单纯换更大上下文更实用。

## 关联概念

- 本地长期记忆
- 项目记忆
- Claude Code
- 跨会话连续性

## 对当前知识库的启发

- 它可以作为 [[wiki 知识层/concepts 概念页/渐进式 Agent 长期记忆]] 的一个轻量实现样本。
- 你的知识库当前已经有 `raw 原始资料/` 与 `wiki 知识层/` 两层；Recall 提示中间还可以有“当前项目状态记忆”这一层。

## 关注点

- 当前是否只适配 Claude Code，还是会扩展到 Codex、Cursor、Gemini CLI。
- 它是偏任务状态记忆，还是也能沉淀成结构化项目知识。
