---
type: concept
summary: "Agent 上下文压缩指在工具输出、日志、文件或检索结果进入 LLM 前先压缩、过滤或重组，以降低令牌成本并提升长上下文利用率；近期还开始出现预测未来相关性的消息级压缩路线。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-15-zh.md"
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-07-06-zh.md"
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-07-20-zh.md"
updated: "2026-07-20"
---

# Agent 上下文压缩

## 定义

Agent 上下文压缩，是在上下文真正送进模型之前，先对工具输出、日志、文件片段或 RAG 结果做压缩、筛选和重组。

常见做法包括：

- 可逆压缩：先给简版，必要时再取原文
- 意图驱动过滤：按当前任务只返回相关片段
- 输出沙箱化：拦截冗长工具结果，避免直接灌满上下文窗口

## 这次新增认识

- 上下文优化正在从 prompt 技巧变成基础设施层。
- `Headroom`、`RTK`、`context-mode` 都在做同一件事：不要把原始工具输出原封不动交给 LLM。
- 重点已经从“模型更强”转向“给模型喂什么、喂多少、按什么粒度喂”。
- 三条路线已经可以粗分为：`Headroom` 的可逆压缩、`context-mode` 的意图驱动筛选、`RTK` 的命令输出代理压缩。
- `Foveance` 又补出第四条路线：预测历史消息对未来查询的相关性，再做消息级压缩，而不是只盯最近窗口。
- 2026 年 7 月 19 日的 Codex 变更把上下文窗口从 `372k` 调整到 `272k`，进一步说明“原始窗口越大越好”并不成立，工程重点会重新回到切块、过滤和压缩。

## 为什么重要

- 直接影响成本，因为令牌就是预算。
- 直接影响稳定性，因为长上下文里的无关信息会稀释任务信号。
- 直接影响 Agent 工作流质量，因为工具输出往往比自然语言更冗长、更噪声化。
- 它也会影响工具选型，因为平台本身都可能主动缩小窗口，逼迫工作流更精细地管理输入。

## 对我的意义

- 这和本地 AI 助手、RAG、编码代理、知识库自动化都有关。
- 如果后续要让 Agent 批量处理 Markdown、日志或搜索结果，上下文压缩会比单纯换模型更划算。
- 它也可以和 `Agentic 文本编辑原语` 形成互补：一个控制输入，一个控制输出动作。

## 相关页面

- [[wiki 知识层/entities 实体页/Headroom]]
- [[wiki 知识层/entities 实体页/context-mode]]
- [[wiki 知识层/entities 实体页/RTK]]
- [[wiki 知识层/entities 实体页/Foveance]]
- [[wiki 知识层/entities 实体页/OpenAI]]
- [[wiki 知识层/comparisons 比较分析/Agent 上下文预算优化：Headroom vs context-mode vs RTK]]
- [[wiki 知识层/concepts 概念页/Agentic 文本编辑原语]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-06-15 实际日报]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-07-06 实际日报]]
- [[wiki 知识层/sources 来源摘要/Horizon 2026-07-20 实际日报]]

## 下一步问题

- 哪些本库自动化任务最容易被长输出和噪声上下文拖慢？
