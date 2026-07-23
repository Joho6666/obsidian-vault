---
type: concept
summary: "渐进式 Agent 长期记忆指把 Agent 交互从原始记录逐层蒸馏为结构化记忆、摘要知识和经验提要，以兼顾可追溯性、成本和跨会话复用。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-22-raw-candidates.md"
updated: "2026-06-22"
---

# 渐进式 Agent 长期记忆

## 定义

渐进式 Agent 长期记忆，是把 Agent 的跨会话记忆拆成多层，而不是只保留完整历史或只保留一份摘要。

典型分层是：

- `L0`：原始捕获
- `L1`：结构化记忆
- `L2`：摘要知识
- `L3`：概要经验

## 这次新增认识

- 长期记忆不是“上下文越长越好”，而是要把原始交互逐步压缩成可复用知识。
- 这种设计兼顾了三件事：可追溯、低成本、可迁移。
- 和只做会话摘要相比，渐进式管道更适合项目协作、长期助手和知识库自动化。
- 新一轮 Horizon 候选显示，Agent 记忆正在继续分层：
  - `Recall` 更偏“当前项目 / 当前任务”的本地会话连续性
  - `codebase-memory-mcp` 更偏“整个代码仓库”的结构化知识图谱记忆
  - `TencentDB Agent Memory` 更偏“交互历史到知识经验”的渐进式蒸馏

## 为什么重要

- 能避免每次都把完整历史重新喂给模型。
- 能把一次性交互转成稳定经验，而不只是临时上下文。
- 更适合本地优先架构，因为中间层可以落在 SQLite、结构化文件或本地索引里。

## 对我的意义

- 当前知识库已经具备 `raw 原始资料 -> wiki 知识层` 的两层结构。
- 这个概念提醒我，中间还可以补“结构化记忆层”，例如任务状态、阶段总结、反复出现的事实卡片。
- 对自动化工作流来说，这有助于减少重复蒸馏和重复判断。

## 相关页面

- [[wiki 知识层/entities 实体页/TencentDB Agent Memory]]
- [[wiki 知识层/entities 实体页/Recall]]
- [[wiki 知识层/entities 实体页/codebase-memory-mcp]]
- [[wiki 知识层/concepts 概念页/SQLite 持久化工作流]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-06-15 实际日报]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-06-22 原始候选蒸馏]]

## 下一步问题

- 本库是否需要在 `raw` 与 `wiki` 之间增加结构化中间层？
- 哪些自动化任务适合优先使用渐进式记忆，而不是全文历史重放？
- 是否要把“项目记忆”“代码库记忆”“知识库记忆”明确拆成三种不同能力层？
