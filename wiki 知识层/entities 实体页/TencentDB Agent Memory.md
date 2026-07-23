---
type: entity
summary: "TencentDB Agent Memory 是腾讯云开源的本地优先 Agent 长期记忆库，用 L0-L3 四层渐进式管道把原始交互蒸馏成结构化知识与经验。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
updated: "2026-06-15"
---

# TencentDB Agent Memory

## 类型

- 项目
- Agent 记忆基础设施

## 本次新增信息

- 这是一个 TypeScript 项目，强调完全本地化，无需外部 API。
- 其核心设计是四层渐进式记忆：
  - `L0` 原始捕获
  - `L1` 结构化记忆
  - `L2` 摘要知识
  - `L3` 概要经验
- 方案结合本地 LLM 与 SQLite 向量搜索，面向 OpenClaw 及其他 Agent 框架。

## 为什么值得记录

- 它把长期记忆从抽象能力变成了明确的数据管道。
- 对本地 Agent 和知识库自动化来说，这类“逐层蒸馏”比单纯堆积历史更可控。

## 关联概念

- 长期记忆
- 本地优先
- 渐进式蒸馏
- SQLite 持久化

## 关注点

- 是否容易脱离 TencentDB 品牌栈独立使用。
- 这种四层结构是否适合迁移到 Obsidian 或本地项目知识管理。
