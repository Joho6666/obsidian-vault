---
type: log
status: active
updated: 2026-07-20
---

# wiki 知识层/log 日志

## [2026-05-31] restructure | 三层知识库结构初始化

- 创建 `raw 原始资料/` 原始资料层。
- 创建 `wiki 知识层/` 知识层。
- 创建根目录 `TheSchema.md` 与 `README.md`。
- 将现有资料按用途归类迁移。
- 更新主要 Markdown wikilink 前缀。

### 迁移记录
- `Clippings` → `raw 原始资料/clippings 网页剪藏`
- `Projects` → `raw 原始资料/projects 项目资料`
- `Obsidian教程` → `raw 原始资料/tutorials 教程`
- `卡帕西obsidian` → `raw 原始资料/references 参考资料/卡帕西obsidian`
- `AI信息收集系统` → `wiki 知识层/overview 总览综合/AI信息收集系统`
- `99-归档` → `raw 原始资料/archive 归档`
- `00-首页.md` → `raw\archive\旧导航\00-首页.md`
- `未命名.base` → `raw\archive\旧导航\未命名.base`

## [2026-05-31] rename | 左侧目录双语化

- `raw/` → `raw 原始资料/`
- `wiki/` → `wiki 知识层/`
- `Attachments/` → `Attachments 附件/`
- raw/wiki 子目录改为英文 + 中文说明。
- 更新主要 wikilink 与来源路径。


## [2026-05-31] update | 工作流说明图解化

- 更新 [[wiki 知识层/overview 总览综合/AI信息收集系统/01-系统机制/目录结构与工作流]]。
- 加入整体结构图、目录职责图、Ingest/Query/Lint 流程图。

## [2026-05-31] skill | 加入 LLM Wiki 工作流 Skill

- 更新 `.agents/skills/obsidian-knowledge-system/SKILL.md`。
- 新建 [[ai有关的装备/skills/LLM Wiki 知识库工作流 Skill]]。
- 新建/更新 [[ai有关的装备/skills/skills 索引]]。
- 将 [[ai有关的装备/workflow工作流/历史说明/目录结构与工作流 1]] 关联到 Skill。

## [2026-05-31] automation | 创建自动更新知识库工作流

- 新建 [[ai有关的装备/workflow工作流/自动更新知识库]]。
- 新建 [[ai有关的装备/workflow工作流/workflow 索引]]。
- 新建 [[ai有关的装备/workflow工作流/自动化运行记录/README]]。

## [2026-05-31] horizon-auto | Horizon 自动更新知识库

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- 新增来源摘要：1 个
- 新增概念页：4 个
- 新增实体页：5 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 修复 Horizon 同步脚本的 vault 根目录与旧路径问题
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-05-31]]

## [2026-06-01] horizon-auto | Horizon 自动更新知识库

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 抓取成功，但 AI 分析阶段大量 `APIConnectionError`
- 2026-06-01 原始日报已保存，但无有效高分条目
- 按回退策略改处理既有 summary：`horizon-2026-05-30-zh.md`
- 新增来源摘要：1 个
- 新增概念页：3 个
- 新增实体页：0 个
- 更新总览页：1 个
- 修复 `sync_obsidian_digest.py` 对空日报的降级处理与最新日报选择逻辑
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-01]]

## [2026-06-08] horizon-auto | Horizon 自动更新知识库

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- 本次未抓取到新资料；项目入口脚本中的 `python -m uv` 失效，直接 `uv run horizon --hours 24` 在 10 分钟内未完成
- 按回退策略处理既有 summary：`horizon-2026-05-30-zh.md` 与 `horizon-2026-05-31-zh.md`
- 新增来源摘要：1 个
- 新增概念页：1 个
- 新增实体页：2 个
- 更新总览页：1 个
- 修复 Horizon 运行脚本与中英对照构建脚本：2 处
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-08]]

## [2026-06-08] horizon-auto | Horizon 自动更新知识库（最终版）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- DeepSeek 返回 `402 Insufficient Balance`，分析阶段已改为启发式 fallback
- `uv run horizon --hours 24` 最终成功完成，生成 2026-06-08 summary，耗时约 9.6 秒（降级后）
- 新增来源摘要：2 个
- 新增概念页：2 个
- 新增实体页：3 个
- 更新总览页：1 个
- 修复脚本问题：4 处
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-08]]

## [2026-06-09] translate | Horizon 2026-06-08 中文日报标题汉化

- 更新 [[raw 原始资料/projects 项目资料/Horizon/docs/_posts/2026-06-08-summary-zh]]。
- 更新 [[raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-06-08-zh]]。

## [2026-06-09] horizon-config | 加强 AI 与 GitHub 信息抓取

- 更新 `raw 原始资料/projects 项目资料/Horizon/data/config.json`。
- OSSInsight 关键词扩展到 agent / MCP / Codex / goose / OpenClaw / vLLM / Ollama 等。
- GitHub release 监控新增 OpenAI、MCP、goose、LangChain、LlamaIndex、AutoGen、CrewAI、browser-use 等项目。
- 新增 GitHub Trending Python / TypeScript / Rust / Go RSS。
- 暂时关闭 Reuters / BBC / JAMA / Nature / Quanta 等泛新闻源，降低噪音。

## [2026-06-12] organize | Skills/MCP/Plugin 中文分类整理

- 重组 `ai有关的装备/skills/` 为中文分类目录。
- 新建 [[ai有关的装备/skills/00-索引/skills 分类总览]]。
- 新建 MCP 与 Plugin 分类目录及索引。
- 移动条目：
  - `ai-experiment-report-zh` → `01-教育学习类`
  - `proteus-stm32-homework` → `01-教育学习类`
  - `proteus-stm32-homework-zh` → `01-教育学习类`
  - `Proteus STM32 作业调试.md` → `01-教育学习类`
  - `jiujiu 的中文论文写作与修改助手.md` → `01-教育学习类`
  - `LLM Wiki 知识库工作流 Skill.md` → `02-知识库与Obsidian类`
  - `obsidian-cli` → `02-知识库与Obsidian类`
  - `obsidian-markdown` → `02-知识库与Obsidian类`
  - `obsidian-bases` → `02-知识库与Obsidian类`
  - `json-canvas` → `02-知识库与Obsidian类`
  - `defuddle` → `02-知识库与Obsidian类`
  - `doc` → `03-文档资料处理类`
  - `pdf` → `03-文档资料处理类`
  - `markitdown` → `03-文档资料处理类`
  - `bilingual-reporting` → `03-文档资料处理类`
  - `frontend-design` → `04-编程开发与网页类`
  - `playwright` → `04-编程开发与网页类`
  - `ui-ux-pro-max` → `04-编程开发与网页类`
  - `planning-with-files` → `05-AI Agent效率与规划类`
  - `planning-with-files.md` → `05-AI Agent效率与规划类`
  - `using-superpowers` → `05-AI Agent效率与规划类`
  - `using-superpowers.md` → `05-AI Agent效率与规划类`
  - `codex手动技能索引.md` → `05-AI Agent效率与规划类`
  - `sora` → `06-多媒体与创意生成类`
  - `hatch-pet` → `06-多媒体与创意生成类`
  - `skills 索引.md` → `99-待分类`

## [2026-06-12] cleanup | skills 目录去技能包化

- 将 `ai有关的装备/skills/` 中的技能包文件夹转换为可直接打开的 Markdown 笔记。
- 删除原技能包文件夹、中文样本、README 等侧栏噪音。
- 更新 [[ai有关的装备/skills/00-索引/skills 分类总览]] 链接。

## [2026-06-12] simplify | 顶层目录减负整理

- 合并 `Clippings/` 到 `raw 原始资料/clippings 网页剪藏/`。
- 合并 `工作流使用说明/` 到 `ai有关的装备/workflow工作流/历史说明/`。
- 合并 `AI信息收集系统/` 到 `wiki 知识层/overview 总览综合/AI信息收集系统/旧顶层补充/`。
- 合并 `其他资料/` 到 `raw 原始资料/archive 归档/其他资料/`。
- 移动根目录 `Attachments 附件.md` 到 `Attachments 附件/附件索引.md`。
- 根目录现在只保留核心入口。

## [2026-06-15] horizon-auto | Horizon 自动更新知识库

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 抓取成功，但 AI 分析阶段卡在 `Analyzing content with AI...` 之后，未生成新的 summary
- 保留失败日志：`raw 原始资料/projects 项目资料/Horizon/data/last-run.log`
- 按回退策略处理既有 summary：`horizon-2026-06-08-zh.md`
- 新增来源摘要：1 个
- 新增概念页：1 个
- 新增实体页：2 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-15]]

## [2026-06-15] horizon-auto | Horizon 自动更新知识库（实际日报补录）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 重新运行成功，实际生成 `horizon-2026-06-15-{zh,en}.md`
- 新增来源摘要：1 个
- 新增概念页：2 个
- 新增实体页：4 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 修正同日回退版判断，以实际 summary 为准
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-15]]

## [2026-06-22] horizon-auto | Horizon 自动更新知识库（原始候选蒸馏）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 本轮真实完成抓取与分析，但 10 分钟自动化窗口内未完成富化与最终 summary 写盘
- 新建原始候选摘要：`horizon-2026-06-22-raw-candidates.md`
- 新增来源摘要：1 个
- 新增概念页：1 个
- 更新概念页：1 个
- 新增实体页：3 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 保留运行日志：`last-run-2026-06-22.log`、`last-run-2026-06-22-full.log`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-22]]

## [2026-06-29] horizon-auto | Horizon 自动更新知识库（回退蒸馏）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- 本次重新运行 `uv run horizon --hours 24` 超过 5 分钟仍未产出新 summary，按回退策略处理既有 `horizon-2026-06-15-zh.md`
- 新增来源摘要：1 个
- 新增比较页：1 个
- 新增实体页：1 个
- 更新概念页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-06-29]]

## [2026-07-06] horizon-auto | Horizon 自动更新知识库（实际日报）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- 首次运行因 Windows `gbk` 控制台无法输出 emoji 而中断，改以 UTF-8 环境重新执行 `uv run horizon --hours 24`
- Horizon 重新运行成功，实际生成 `horizon-2026-07-06-{zh,en}.md`
- 同步更新 `Horizon快速浏览`、`Horizon中英对照日报`、`Horizon逐段中英对照`
- 新增来源摘要：1 个
- 新增概念页：2 个
- 新增实体页：1 个
- 更新概念页：1 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-07-06]]

## [2026-07-13] horizon-auto | Horizon 自动更新知识库（实际日报）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 重新运行成功，实际生成 `horizon-2026-07-13-{zh,en}.md`
- 同步更新 `Horizon快速浏览`、`Horizon中英对照日报`、`Horizon逐段中英对照`
- 新增来源摘要：1 个
- 新增概念页：1 个
- 新增比较页：1 个
- 更新概念页：1 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-07-13]]

## [2026-07-20] horizon-auto | Horizon 自动更新知识库（实际日报）

- 扫描：`raw 原始资料/projects 项目资料/Horizon/`
- Horizon 重新运行成功，实际生成 `horizon-2026-07-20-{zh,en}.md`
- 同步更新 `Horizon快速浏览`、`Horizon中英对照日报`、`Horizon逐段中英对照`
- 新增来源摘要：1 个
- 新增概念页：1 个
- 新增实体页：1 个
- 更新概念页：1 个
- 更新总览页：1 个
- 更新 `wiki 知识层/index 索引.md`
- 运行报告：[[ai有关的装备/workflow工作流/自动化运行记录/2026-07-20]]
