---
type: skill
status: active
created: 2026-05-31
updated: 2026-05-31
tags:
  - skill
  - LLMWiki
  - Obsidian工作流
---

# LLM Wiki 知识库工作流 Skill

> [!summary]
> 这个 Skill 用来维护你的三层知识库：`raw 原始资料/` 存事实，`wiki 知识层/` 存理解，`TheSchema.md` 定规则。

## 1. 什么时候调用

当你想做这些事时，就调用这个工作流：

- 把一篇 raw 资料整理成 wiki
- 基于 wiki 回答问题
- 对 wiki 做健康检查
- 更新 index / log
- 把临时回答沉淀成长期知识页

## 2. 总流程图

```mermaid
flowchart LR
    A[新资料<br/>网页 / PDF / 项目 / 教程] --> B[raw 原始资料<br/>事实来源，只读为主]
    B --> C[TheSchema.md<br/>规则：怎么从 raw 到 wiki]
    C --> D[LLM Skill<br/>Ingest / Query / Lint]
    D --> E[wiki 知识层<br/>结构化知识网络]
    E --> F[index 索引<br/>快速定位]
    E --> G[log 日志<br/>记录演化]
    E --> H[输出 / 问答 / 决策]
    H --> E
```

## 3. Ingest 摄取流程

```mermaid
flowchart TD
    R[raw 原始资料中的一篇资料] --> Read[LLM 阅读]
    Read --> S[生成 sources 来源摘要]
    S --> C[抽取 concepts 概念页]
    S --> E[抽取 entities 实体页]
    C --> O[必要时更新 overview 总览]
    E --> O
    O --> I[更新 index 索引]
    I --> L[更新 log 日志]
```

你可以这样说：

```text
请基于 raw 原始资料/clippings 网页剪藏/xxx.md 进行 Ingest
```

## 4. Query 问答流程

```mermaid
flowchart TD
    Q[你的问题] --> I[先查 wiki 知识层/index 索引]
    I --> W[读取相关 wiki 页面]
    W --> Need{需要证据吗?}
    Need -- 是 --> Raw[回看 raw 原始资料]
    Need -- 否 --> Ans[综合回答]
    Raw --> Ans
    Ans --> Keep{未来还会用吗?}
    Keep -- 是 --> Write[写回 wiki]
    Keep -- 否 --> Temp[保留为临时回答]
```

你可以这样说：

```text
基于 wiki 知识层，回答我：xxx
```

## 5. Lint 审查流程

```mermaid
flowchart TD
    Start[开始 Lint] --> Scan[扫描 wiki 知识层]
    Scan --> A[找矛盾]
    Scan --> B[找过时内容]
    Scan --> C[找孤立页面]
    Scan --> D[找重复概念]
    Scan --> E[找缺失链接]
    A --> Report[生成建议清单]
    B --> Report
    C --> Report
    D --> Report
    E --> Report
    Report --> Confirm{确认后再改}
    Confirm -- 是 --> Fix[执行修改]
    Confirm -- 否 --> Stop[停止]
    Fix --> Log[记录 log 日志]
```

你可以这样说：

```text
请对 wiki 知识层做一次 Lint，先给建议清单，不要直接大改
```

## 6. 目录对应关系

| 层级 | 目录 | 作用 |
|---|---|---|
| 原始资料层 | [[raw 原始资料/index 索引]] | 保存事实来源 |
| 知识层 | [[wiki 知识层/index 索引]] | 保存结构化理解 |
| 配置层 | [[TheSchema]] | 定义规则和工作流 |
| 附件层 | [[Attachments 附件/附件索引]] | 图片、SVG、媒体资源 |

## 7. 使用口诀

```text
资料先进 raw
理解沉到 wiki
规则看 TheSchema
查找看 index
变化写 log
定期做 Lint
```

## 8. 对应的真实 Agent Skill

这个说明页对应本地 Agent Skill：

```text
.agents/skills/obsidian-knowledge-system/SKILL.md
```
