---
type: entity
summary: "Headroom 是一个用于压缩日志、工具输出、文件和 RAG 块的开源库，目标是在不明显损伤回答质量的前提下降低 60-95% 的 LLM 令牌消耗。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
updated: "2026-06-15"
---

# Headroom

## 类型

- 项目
- 上下文压缩工具

## 本次新增信息

- 这是一个 Python 项目，面向工具输出、日志、文件和 RAG 块做前置压缩。
- 它提供三层压缩栈，并支持按需恢复未压缩片段。
- 除了库本身，还提供代理和 MCP server 形态，方便接入现有工作流。

## 为什么值得记录

- 它说明上下文预算优化已经从零散技巧变成标准化组件。
- 对大上下文 Agent、RAG 和日志分析场景来说，这种“先压再看”的模式很实用。

## 关联概念

- 上下文压缩
- token optimization
- RAG
- MCP

## 关注点

- 它和 `context-mode` 分别代表可逆压缩与意图筛选两条路线。
- 如果后续类似工具继续出现，值得建立专门的比较页。
