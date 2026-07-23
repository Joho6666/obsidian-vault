---
type: entity
summary: "SkillSpector 是 NVIDIA 开源的 AI agent skill 安全扫描器，用于在安装前识别恶意模式、漏洞和供应链风险。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-22-raw-candidates.md"
updated: "2026-06-22"
---

# SkillSpector

## 类型

- 项目
- Agent Skill 安全工具

## 本次新增信息

- 它的定位是扫描 AI agent skills，在安装前发现风险。
- 项目目标包含恶意模式、危险能力和安全问题识别。
- 从公开资料看，它把 skill 视作需要单独治理的供应链对象。

## 为什么值得记录

- 随着 skills / plugins / MCP server 生态增长，技能包会逐渐像浏览器扩展和 npm 包一样成为新的攻击面。
- 这让“AI Agent 工具效率”不再只看功能，还要看安全审查与安装边界。

## 关联概念

- Skill 安全
- Agent 扩展治理
- 供应链风险
- 安装前扫描

## 对当前知识库的启发

- 你的 vault 里已经有大量 Skill、MCP、Plugin 资料，但此前主要是分类与能力整理，安全视角较弱。
- SkillSpector 适合作为“技能治理”主线的起点样本。

## 关注点

- 后续是否会扩展到 MCP server registry 或插件市场级扫描。
- 是否会形成通用规则集，成为 Agent 开发生态里的标准安全步骤。
