---
title: n8n Instance-level MCP
type: mcp
status: connected
updated: 2026-07-23
tags:
  - MCP
  - n8n
  - Codex
  - automation
aliases:
  - n8n MCP
---

# n8n Instance-level MCP

## 当前状态

- MCP 名称：`n8n`
- Codex 状态：`enabled`
- 认证方式：Bearer token
- token 保存位置：用户环境变量 `N8N_MCP_TOKEN`
- Server URL：`http://localhost:5678/mcp-server/http`
- n8n 页面：`http://localhost:5678/settings/mcp`
- Codex 配置文件：`C:\Users\JOHO\.codex\config.toml`

> [!important]
> 不要把 Bearer token 原文写进 Obsidian。当前只记录环境变量名：`N8N_MCP_TOKEN`。

## Codex 配置片段

```toml
[mcp_servers.n8n]
url = "http://localhost:5678/mcp-server/http"
bearer_token_env_var = "N8N_MCP_TOKEN"
```

## 已验证结果

2026-07-23 已通过本机 HTTP 请求验证连接成功：

- HTTP 状态：`200`
- 响应类型：`text/event-stream`
- MCP 服务名：`n8n MCP Server`
- MCP 服务版本：`1.1.0`
- 能力：`tools`、`resources`

## 使用提示

- 如果当前 Codex 会话里还看不到 n8n 工具，重启 Codex 或新开一个任务后再试。
- n8n 必须保持在本机 `http://localhost:5678` 运行。
- n8n 的 Instance-level MCP 页面需要保持 Enabled。
- 如果 token 被刷新，需要重新写入用户环境变量 `N8N_MCP_TOKEN`。

## 相关链接

- [[ai有关的装备/mcp/MCP 分类总览]]
- [[wiki 知识层/concepts 概念页/MCP（模型上下文协议）]]
