---
tags: [AI信息收集, Horizon, 配置]
created: 2026-05-30
status: 已切换DeepSeek，待填写DEEPSEEK_API_KEY后测试运行
---

# Horizon 配置记录

项目地址：[Thysrael/Horizon](https://github.com/Thysrael/Horizon)

## 当前已完成

- 已克隆 Horizon 到：`Projects/Horizon`
- 已安装 `uv`：`python -m uv --version`
- 已安装项目依赖：`python -m uv sync`
- 已复制并改写：`Projects/Horizon/.env`
- 已生成适合“学生 + AI 热爱者”的配置：`Projects/Horizon/data/config.json`\n- 已将 AI Provider 切换为 DeepSeek：`provider=deepseek`, `model=deepseek-chat`, `api_key_env=DEEPSEEK_API_KEY`
- 已验证配置文件可被 Horizon 正确读取。

## 当前信息源

已启用：

- Hacker News
- Reddit：MachineLearning、LocalLLaMA、ArtificialInteligence
- RSS：OpenAI、Anthropic、Google DeepMind、Hugging Face、Simon Willison、Latent Space、The Batch
- GitHub Release：openai-python、anthropic-sdk-python、MCP Python SDK、transformers
- OSS Insight：AI / LLM / Agent / RAG / MCP 相关开源趋势

未启用：

- Twitter / X
- Telegram
- 邮件推送
- Webhook 推送
- OpenBB 金融新闻

## 你需要提供 / 决定的内容

### 必需

至少提供一种 AI 模型 API Key：

当前已选择 DeepSeek。请把你的 DeepSeek API Key 填到 `Projects/Horizon/.env` 的这一行后面：\n\n```env\nDEEPSEEK_API_KEY=你的key\n```\n\nOpenAI 和 DashScope 暂时不需要填写。

### 可选

- `GITHUB_TOKEN`：提高 GitHub API 限额，不填也能运行。
- `HORIZON_WEBHOOK_URL`：如果你想推送到飞书 / 钉钉 / Slack / Discord。
- `APIFY_TOKEN`：如果你想启用 Twitter/X 抓取。

## 本地运行命令

在 vault 根目录执行：

```powershell
cd Projects\Horizon
python -m uv run horizon --hours 24
```

报告会生成在：

```text
Projects/Horizon/data/summaries/
```

## 安全提醒

不要把 `.env` 内容粘贴到公开笔记、GitHub、截图或聊天群里。`.env` 已在 Horizon 的 `.gitignore` 中被忽略。


