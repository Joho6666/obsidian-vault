---
type: schema
status: active
created: 2026-05-31
updated: 2026-05-31
tags:
  - schema
  - wiki
  - knowledge-management
---

# TheSchema

> [!info] 核心目标
> 用 `raw 原始资料/` 保存不可变事实来源，用 `wiki 知识层/` 保存 LLM 维护的结构化知识网络。

## 0. 三层结构

```text
raw 原始资料/                    # 原始资料层，只读事实来源
wiki 知识层/                   # 知识层，LLM 维护
TheSchema.md            # 配置层，定义规则和工作流
Attachments 附件/            # 图片与附件资源
README.md               # 系统说明
```

## 1. raw 原始资料/ 原始资料层

原则：**只添加，不改写**。

```text
raw 原始资料/
├─ clippings 网页剪藏/       # 网页剪藏、长文
├─ projects 项目资料/        # 项目原始资料与过程材料
├─ tutorials 教程/           # 教程、工具学习资料
├─ references 参考资料/      # 外部方法论与参考库
├─ papers 论文文章/          # 论文、文章 PDF
├─ books 书籍摘录/           # 书摘、书籍资料
├─ media 媒体资源/           # 原始图片、视频、音频
└─ archive 归档/             # 旧结构、低频资料、历史导航
```

## 2. wiki 知识层/ 知识层

原则：**LLM 可以维护，但要保留来源引用**。

```text
wiki 知识层/
├─ sources 来源摘要/         # 来源摘要页
├─ entities 实体页/          # 人物、项目、工具、组织等实体页
├─ concepts 概念页/          # 方法、理论、模型等概念页
├─ comparisons 比较分析/     # 对比分析页
├─ overview 总览综合/        # 主题综述、系统总览
├─ index 索引.md             # 内容索引
└─ log 日志.md               # 操作日志
```

## 3. 页面格式

所有 wiki 页面建议使用：

```yaml
---
type: source|entity|concept|comparison|overview
summary: "一句话说明这页的核心内容"
sources: ["raw 原始资料/..."]
updated: "YYYY-MM-DD"
---
```

## 4. 三个日常操作

### Ingest / 摄取
当有新资料进入 `raw 原始资料/` 后：
1. 阅读原始资料。
2. 在 `wiki 知识层/sources 来源摘要/` 创建来源摘要。
3. 必要时更新 `wiki 知识层/entities 实体页/`、`wiki 知识层/concepts 概念页/`、`wiki 知识层/overview 总览综合/`。
4. 更新 `wiki 知识层/index 索引.md`。
5. 追加 `wiki 知识层/log 日志.md`。

### Query / 问答
当基于知识库提问时：
1. 先查 `wiki 知识层/index 索引.md`。
2. 再读相关 wiki 页面。
3. 必要时回看 raw 来源。
4. 有长期价值的回答，沉淀回 wiki。

### Lint / 审查
定期检查：
- 页面矛盾
- 过时内容
- 孤立页面
- 重复主题
- 缺失 cross-link

重大修改先列建议清单，再执行。

## 5. 本库分类说明

- 原 `raw 原始资料/clippings 网页剪藏/` → `raw 原始资料/clippings 网页剪藏/`
- 原 `Projects/` → `raw 原始资料/projects 项目资料/`
- 原 `Obsidian教程/` → `raw 原始资料/tutorials 教程/`
- 原 `卡帕西obsidian/` → `raw 原始资料/references 参考资料/卡帕西obsidian/`
- 原 `AI信息收集系统/` → `wiki 知识层/overview 总览综合/AI信息收集系统/`
- 旧导航与低频文件 → `raw 原始资料/archive 归档/`

