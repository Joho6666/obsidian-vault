---
type: entity
summary: "Foveance 是一个把上下文压缩建立在未来相关性预测上的开源项目，代表了 Agent 上下文预算优化的新增路线。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-07-06-zh.md"
updated: "2026-07-06"
---

# Foveance

## 类型

- 项目
- 开源上下文压缩工具

## 本次新增信息

- 它不只按最近窗口裁剪上下文，而是预测历史消息对未来查询的相关性。
- 提供 Python 库、代理服务器，以及针对 `Claude Code`、`Codex` 等工具的封装。
- 附带可复现 benchmark，主打在保留关键信息的同时节省 token。

## 为什么值得记录

- 它把你已经在跟踪的 `Agent 上下文压缩` 主线，从三条路线扩展到第四条。
- 它更贴近实际 Agent 使用场景，而不是只做抽象论文式压缩描述。

## 关联概念

- [[wiki 知识层/concepts 概念页/Agent 上下文压缩]]
- future relevance
- context compression
- token optimization

## 关注点

- benchmark 是否能稳定迁移到真实编码工作流
- 相比 `Headroom`、`context-mode`、`RTK` 的接入成本和收益差异
