---
type: entity
summary: "codebase-memory-mcp 是一个把代码仓库索引成持久化知识图谱并通过 MCP 提供结构化查询的代码理解基础设施。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-22-raw-candidates.md"
updated: "2026-06-22"
---

# codebase-memory-mcp

## 类型

- 项目
- MCP 代码理解基础设施

## 本次新增信息

- 它把代码仓库编译成持久化知识图谱，而不是依赖 file-by-file 搜索。
- 项目强调结构化查询、低 token 消耗和单二进制部署。
- README 明确把 Claude Code、Codex CLI、Gemini CLI 等都视为目标代理环境。

## 为什么值得记录

- 它代表“代码库记忆”开始独立成一层，不再只是 IDE 搜索增强。
- 这条路线把 MCP、知识图谱、代码理解和记忆系统串到了一起，和编码代理的长期可用性直接相关。

## 关联概念

- MCP
- 代码知识图谱
- 代码库记忆
- 结构化查询

## 对当前知识库的启发

- 它和 [[wiki 知识层/entities 实体页/TencentDB Agent Memory]] 对应的是不同层级的记忆：前者更偏代码仓库结构，后者更偏交互历史与经验蒸馏。
- 对你后续做项目知识库、自动化代码审查和本地 Agent 来说，这类“仓库级记忆”比纯向量检索更值得跟踪。

## 关注点

- 目前强调速度和 token 节省，后续要继续观察真实回答质量与安装维护成本。
- 若类似项目持续出现，适合建立一页“代码图谱记忆 vs 普通 RAG 搜索”的比较分析。
