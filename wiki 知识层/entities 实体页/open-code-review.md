---
type: entity
summary: "open-code-review 是 Alibaba 开源的混合式代码审查工具，把确定性规则管线和 LLM Agent 结合，用于输出更可控的行级审查意见。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-08-zh.md"
  - "raw 原始资料/projects 项目资料/Horizon/data/last-run.log"
updated: "2026-06-15"
---

# open-code-review

## 类型

- 项目
- 代码审查工具

## 本次新增信息

- 这是 Alibaba 开源的代码审查项目。
- 项目说明强调混合架构：确定性 pipelines + LLM Agent。
- 其定位不是泛泛聊天式 review，而是输出精确到行的评论，并内置 NPE、线程安全、XSS、SQL 注入等规则。

## 为什么值得记录

- 它体现了“规则检测 + 大模型解释/补充”的组合路线。
- 对你来说，这比单纯关注某个审查模型分数更有长期价值，因为它能转化成工作流设计思路。

## 关联概念

- 代码审查
- LLM reviewer
- 安全规则
- agent workflow

## 关注点

- 它是否支持更容易接入个人仓库或轻量 CI。
- 这类混合架构是否适合独立开发场景，而不只适用于大公司代码库。
