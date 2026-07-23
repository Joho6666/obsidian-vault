# Horizon Daily - 2026-06-01

> From 132 items, 3 important content pieces were selected

---

1. [GitHub repo maps 754 cybersecurity skills for AI agents](#item-1) ⭐️ 8.0/10
2. [Microsoft Releases Agent Governance Toolkit for AI Agents](#item-2) ⭐️ 7.0/10
3. [Chrome DevTools MCP: AI Agents Gain Browser Debugging Power](#item-3) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GitHub repo maps 754 cybersecurity skills for AI agents](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) ⭐️ 8.0/10

A new GitHub repository, mukul975/Anthropic-Cybersecurity-Skills, has been released, providing a structured mapping of 754 cybersecurity skills to five major frameworks including MITRE ATT&CK, NIST CSF 2.0, MITRE ATLAS, D3FEND, and NIST AI RMF. This repository addresses the growing need for AI safety and security by enabling AI coding agents like Claude Code, GitHub Copilot, and Codex CLI to understand and apply standardized cybersecurity skills, potentially improving the security posture of AI-generated code. The skills are formatted according to the agentskills.io open standard and cover 26 security domains, licensed under Apache 2.0. The repository works with over 20 platforms including Claude Code, GitHub Copilot, Codex CLI, Cursor, and Gemini CLI.

ossinsight · mukul975 · Jun 1, 06:43

**Background**: AI coding agents are tools that assist developers by generating or suggesting code. To ensure these agents produce secure code, they need structured knowledge of cybersecurity practices. Frameworks like MITRE ATT&CK catalog adversary tactics, while D3FEND lists defensive techniques. The agentskills.io standard provides a way to define AI agent capabilities in a portable format.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/agentskills/agentskills">GitHub - agentskills/agentskills: Specification and documentation for Agent Skills · GitHub</a></li>
<li><a href="https://atlas.mitre.org/">MITRE ATLAS™</a></li>
<li><a href="https://d3fend.mitre.org/">D3FEND Matrix | MITRE D3FEND™</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#AI agents`, `#MITRE ATT&CK`, `#NIST CSF`, `#agent skills`

---

<a id="item-2"></a>
## [Microsoft Releases Agent Governance Toolkit for AI Agents](https://github.com/microsoft/agent-governance-toolkit) ⭐️ 7.0/10

Microsoft has released the Agent Governance Toolkit, an open-source Python library that provides policy enforcement, zero-trust identity, execution sandboxing, and reliability engineering for autonomous AI agents, covering all 10 items of the OWASP Agentic Top 10. This toolkit addresses critical security and governance gaps in deploying autonomous AI agents, helping organizations mitigate risks like identity abuse and code injection, which are increasingly important as AI agents become more prevalent in enterprise environments. The toolkit is written in Python and has gained 28 stars in the past 24 hours on GitHub, with 18 pushes and 1 fork, indicating early-stage but active development. It specifically addresses the OWASP Agentic Top 10, including risks like identity and privilege abuse (ASI03).

ossinsight · microsoft · Jun 1, 06:43

**Background**: The OWASP Agentic Top 10 is a framework identifying the most critical security risks for autonomous AI agents, such as identity abuse and code injection. Zero-trust identity treats AI agents as first-class identities with their own lifecycle and threat models. Execution sandboxing isolates agent code in secure environments to prevent unauthorized access and data breaches.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/OWASP_Top_10_for_Agentic_Applications_2026">OWASP Top 10 for Agentic Applications 2026</a></li>
<li><a href="https://www.linkedin.com/pulse/agentic-ai-needs-zero-trust-identity-problem-one-talking-derek-doerr-icvqe">Agentic AI Needs Zero Trust Identity The Identity Problem No One Is...</a></li>
<li><a href="https://addozhang.medium.com/ai-agent-code-execution-sandboxes-isolation-from-containers-to-microvms-e80848effea5">AI Agent Code Execution Sandboxes: Isolation from... | Medium</a></li>

</ul>
</details>

**Tags**: `#AI Agents`, `#Governance`, `#Security`, `#Python`, `#OWASP`

---

<a id="item-3"></a>
## [Chrome DevTools MCP: AI Agents Gain Browser Debugging Power](https://github.com/ChromeDevTools/chrome-devtools-mcp) ⭐️ 7.0/10

The Chrome DevTools team released an open-source Model Context Protocol (MCP) server that allows AI coding agents to inspect, debug, and control a live Chrome browser. The project, written in TypeScript, gained 14 stars in the past 24 hours and is actively maintained. This integration bridges AI coding assistants with real browser debugging, enabling automated testing, performance analysis, and reliable automation directly from agent prompts. It significantly enhances the capabilities of tools like Cursor, Claude, and Gemini for web development workflows. The MCP server provides access to Chrome DevTools features including DOM inspection, console evaluation, network monitoring, and Lighthouse audits. A CLI is also available for use without MCP, and the project is hosted on GitHub under the ChromeDevTools organization.

ossinsight · ChromeDevTools · Jun 1, 06:43

**Background**: The Model Context Protocol (MCP) is an open standard that enables AI agents to interact with external tools and data sources in a structured way. Chrome DevTools is a set of web developer tools built into the Chrome browser for debugging and profiling web applications. This project combines both, allowing AI coding agents to leverage DevTools capabilities directly.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ChromeDevTools/chrome-devtools-mcp/">GitHub - ChromeDevTools/chrome-devtools-mcp: Chrome DevTools ...</a></li>
<li><a href="https://developer.chrome.com/docs/devtools/agents">Chrome DevTools for agents</a></li>
<li><a href="https://modelcontextprotocol.io/docs/getting-started/intro">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>

</ul>
</details>

**Tags**: `#Chrome DevTools`, `#AI agents`, `#developer tools`, `#debugging`, `#TypeScript`

---

