---
layout: default
title: "Horizon Summary: 2026-06-01 (ZH)"
date: 2026-06-01
lang: zh
---

> 从 132 条内容中筛选出 3 条重要资讯。

---

1. [GitHub 仓库为 AI 代理映射 754 项网络安全技能](#item-1) ⭐️ 8.0/10
2. [微软发布 AI 智能体治理工具包](#item-2) ⭐️ 7.0/10
3. [Chrome DevTools MCP：AI 代理获得浏览器调试能力](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GitHub 仓库为 AI 代理映射 754 项网络安全技能](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) ⭐️ 8.0/10

一个新的 GitHub 仓库 mukul975/Anthropic-Cybersecurity-Skills 已发布，提供了 754 项网络安全技能到五个主要框架（包括 MITRE ATT&CK、NIST CSF 2.0、MITRE ATLAS、D3FEND 和 NIST AI RMF）的结构化映射。 该仓库通过使 Claude Code、GitHub Copilot 和 Codex CLI 等 AI 编码代理能够理解并应用标准化的网络安全技能，满足了日益增长的 AI 安全需求，有望提升 AI 生成代码的安全水平。 这些技能按照 agentskills.io 开放标准格式化，涵盖 26 个安全领域，采用 Apache 2.0 许可证。该仓库支持超过 20 个平台，包括 Claude Code、GitHub Copilot、Codex CLI、Cursor 和 Gemini CLI。

ossinsight · mukul975 · 6月1日 06:43

**背景**: AI 编码代理是通过生成或建议代码来帮助开发者的工具。为了确保这些代理生成安全的代码，它们需要结构化的网络安全实践知识。像 MITRE ATT&CK 这样的框架记录了对手的战术，而 D3FEND 则列出了防御技术。agentskills.io 标准提供了一种以可移植格式定义 AI 代理能力的方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/agentskills/agentskills">GitHub - agentskills/agentskills: Specification and documentation for Agent Skills · GitHub</a></li>
<li><a href="https://atlas.mitre.org/">MITRE ATLAS™</a></li>
<li><a href="https://d3fend.mitre.org/">D3FEND Matrix | MITRE D3FEND™</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI agents`, `#MITRE ATT&CK`, `#NIST CSF`, `#agent skills`

---

<a id="item-2"></a>
## [微软发布 AI 智能体治理工具包](https://github.com/microsoft/agent-governance-toolkit) ⭐️ 7.0/10

微软发布了 Agent Governance Toolkit，这是一个开源 Python 库，为自主 AI 智能体提供策略执行、零信任身份、执行沙箱和可靠性工程，覆盖 OWASP Agentic Top 10 的全部 10 项。 该工具包解决了部署自主 AI 智能体时的关键安全和治理缺口，帮助组织缓解身份滥用和代码注入等风险，随着 AI 智能体在企业环境中日益普及，这一点变得越来越重要。 该工具包使用 Python 编写，过去 24 小时内在 GitHub 上获得 28 颗星，18 次推送和 1 次 fork，表明处于早期但活跃的开发阶段。它专门针对 OWASP Agentic Top 10，包括身份和权限滥用（ASI03）等风险。

ossinsight · microsoft · 6月1日 06:43

**背景**: OWASP Agentic Top 10 是一个框架，识别自主 AI 智能体最关键的安全风险，如身份滥用和代码注入。零信任身份将 AI 智能体视为具有自身生命周期和威胁模型的一等身份。执行沙箱将智能体代码隔离在安全环境中，以防止未经授权的访问和数据泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/OWASP_Top_10_for_Agentic_Applications_2026">OWASP Top 10 for Agentic Applications 2026</a></li>
<li><a href="https://www.linkedin.com/pulse/agentic-ai-needs-zero-trust-identity-problem-one-talking-derek-doerr-icvqe">Agentic AI Needs Zero Trust Identity The Identity Problem No One Is...</a></li>
<li><a href="https://addozhang.medium.com/ai-agent-code-execution-sandboxes-isolation-from-containers-to-microvms-e80848effea5">AI Agent Code Execution Sandboxes: Isolation from... | Medium</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#Governance`, `#Security`, `#Python`, `#OWASP`

---

<a id="item-3"></a>
## [Chrome DevTools MCP：AI 代理获得浏览器调试能力](https://github.com/ChromeDevTools/chrome-devtools-mcp) ⭐️ 7.0/10

Chrome DevTools 团队发布了一个开源的模型上下文协议（MCP）服务器，使 AI 编码代理能够检查、调试和控制实时的 Chrome 浏览器。该项目使用 TypeScript 编写，过去 24 小时内获得了 14 颗星，并正在积极维护中。 这一集成将 AI 编码助手与真实的浏览器调试连接起来，使得从代理提示中直接进行自动化测试、性能分析和可靠自动化成为可能。它显著增强了 Cursor、Claude 和 Gemini 等工具在 Web 开发工作流程中的能力。 该 MCP 服务器提供对 Chrome DevTools 功能的访问，包括 DOM 检查、控制台评估、网络监控和 Lighthouse 审计。还提供了一个 CLI，可在没有 MCP 的情况下使用，该项目托管在 ChromeDevTools 组织下的 GitHub 上。

ossinsight · ChromeDevTools · 6月1日 06:43

**背景**: 模型上下文协议（MCP）是一种开放标准，使 AI 代理能够以结构化方式与外部工具和数据源交互。Chrome DevTools 是内置于 Chrome 浏览器中的一套 Web 开发者工具，用于调试和分析 Web 应用程序。该项目将两者结合，使 AI 编码代理能够直接利用 DevTools 的功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ChromeDevTools/chrome-devtools-mcp/">GitHub - ChromeDevTools/chrome-devtools-mcp: Chrome DevTools ...</a></li>
<li><a href="https://developer.chrome.com/docs/devtools/agents">Chrome DevTools for agents</a></li>
<li><a href="https://modelcontextprotocol.io/docs/getting-started/intro">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>

</ul>
</details>

**标签**: `#Chrome DevTools`, `#AI agents`, `#developer tools`, `#debugging`, `#TypeScript`

---