---
type: concept
summary: "Agent 技能安全扫描指在安装或启用 AI agent skills、plugins、MCP server 前，先对其能力、依赖、代码模式和供应链来源进行风险审查。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-22-raw-candidates.md"
updated: "2026-06-22"
---

# Agent 技能安全扫描

## 定义

Agent 技能安全扫描，是在 skill、plugin、MCP server 被安装或接入前，先检查其代码、依赖、能力范围和来源可信度。

它关注的不只是传统漏洞，还包括：

- 是否存在危险命令或高权限行为
- 是否通过提示词、脚本或依赖引入恶意模式
- 是否来自不可信来源
- 是否把“便捷能力”伪装成默认安全能力

## 这次新增认识

- Skill 生态越繁荣，安全边界就越像浏览器扩展和包管理器生态。
- 对 AI Agent 来说，扩展包不只是代码依赖，也是“能力注入点”。
- 因此安全扫描会逐渐变成 skills / MCP / plugin 工作流里的前置步骤，而不是事后补救。

## 为什么重要

- 可以减少把不透明第三方能力直接接入本地助手的风险。
- 可以让技能市场、团队共享 skill 包和自动化安装流程更可控。
- 对多 Agent 工作流来说，它能降低“工具被滥用”或“权限被放大”的隐患。

## 对我的意义

- 你的知识库里已经沉淀了大量 Skill、MCP、Plugin 资料，但大多站在能力与效率角度。
- 这页概念提醒后续要补“哪些 skill 可以默认信任、哪些要先扫描、哪些只适合隔离环境”。

## 相关页面

- [[wiki 知识层/entities 实体页/SkillSpector]]
- [[wiki 知识层/concepts 概念页/MCP（模型上下文协议）]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-06-22 原始候选蒸馏]]

## 下一步问题

- 是否要把 MCP server 也纳入同一套安全扫描视角？
- 对当前本库里的本地技能和第三方技能，是否需要最小权限与来源分级？
