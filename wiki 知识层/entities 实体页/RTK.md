---
type: entity
summary: "RTK（Rust Token Killer）是一个零依赖的 Rust CLI 代理，在命令输出进入 LLM 前做透明压缩，以降低 60-90% 的 token 消耗。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
updated: "2026-06-29"
---

# RTK

## 类型

- 项目
- CLI 代理
- 上下文压缩工具

## 本次新增信息

- `RTK` 采用单一 Rust 二进制、零依赖设计，定位是给 AI 编码代理做命令输出代理层。
- 它支持 `cargo test`、`git diff`、`grep`、`docker` 等常见开发命令。
- 它在输出真正发送给 LLM 之前做透明压缩，目标是把令牌消耗降低 60-90%。
- 项目支持通过 Claude Code 的 `PreToolUse` hook 全局安装，说明它更偏工作流接入而不只是一个独立库。

## 为什么值得记录

- 它补上了 `Headroom` 与 `context-mode` 之间的第三种实践样本：不是通用压缩库，也不是意图筛选 MCP，而是命令级 CLI 代理。
- 对你关心的编码代理、本地助手和自动化工作流来说，它更接近“马上能插到现有链路里”的工程方案。

## 关联概念

- 上下文压缩
- token optimization
- CLI proxy
- 编码代理

## 和当前知识库的关系

- 它能作为 [[wiki 知识层/concepts 概念页/Agent 上下文压缩]] 的命令输出压缩样本。
- 它适合放进 [[wiki 知识层/comparisons 比较分析/Agent 上下文预算优化：Headroom vs context-mode vs RTK]]，帮助区分“可逆压缩 / 意图筛选 / 命令代理”三条路线。

## 关注点

- 是否会扩展到 Claude Code 之外的 Codex、Cursor、Gemini CLI 等代理。
- 压缩收益是否依赖命令类型，尤其是 `git diff`、测试输出和容器日志这类高噪声场景。
