---
title: 嘉立创EDA MCP 接入记录
date: 2026-07-24
tags:
  - mcp
  - pcb
  - eda
  - 嘉立创EDA
  - codex
aliases:
  - jlceda MCP
  - 嘉立创EDA MCP
  - JLCEDA MCP
status: installed
---

# 嘉立创EDA MCP 接入记录

> [!summary]
> 当前 Codex 已接入 `jlceda` MCP，用于让 Agent 通过本地桥接控制嘉立创EDA专业版中的 PCB / 原理图工程。

## 当前结论

已接入的是社区项目 [hyl64/jlcmcp](https://github.com/hyl64/jlcmcp)，不是嘉立创官方主线 MCP。

它的定位是：通过 Model Context Protocol 暴露 PCB / 原理图自动化工具，让 AI IDE 经由本地 WebSocket bridge 操作嘉立创EDA。项目 README 描述其包含 MCP Server 和 `jlc-bridge` 嘉立创EDA 扩展插件，并要求 Node.js、gateway、EDA 内扩展同时运行。

官方相关项目 [easyeda/extension-dev-mcp-tools](https://github.com/easyeda/extension-dev-mcp-tools) 更偏嘉立创EDA / EasyEDA 专业版扩展调试，例如导入插件、收集控制台日志，不是直接画 PCB 的主工作流。

## 本机安装状态

Codex MCP 名称：`jlceda`

本地源码目录：

```text
C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp
```

当前安装 commit：

```text
e40a64f52a873afc46541588873a8dfd56ea53b0
```

Codex 配置位置：

```text
C:\Users\JOHO\.codex\config.toml
```

配置片段：

```toml
[mcp_servers.jlceda]
command = "node"
args = ['C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\codex-start.mjs']
```

本地包装入口：

```text
C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\codex-start.mjs
```

本地 relay：

```text
C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\codex-gateway.mjs
```

relay 地址：

```text
ws://127.0.0.1:18800/ws/bridge
```

嘉立创EDA 扩展包：

```text
C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\jlc-bridge\build\jlc-bridge.eext
```

## 架构

```mermaid
flowchart LR
    A["Codex / Agent"] -->|"stdio MCP"| B["jlceda MCP Server"]
    B -->|"WebSocket"| C["本机 relay: 127.0.0.1:18800"]
    C -->|"WebSocket"| D["jlc-bridge.eext"]
    D --> E["嘉立创EDA专业版"]
```

## 使用前置步骤

1. 重启 Codex 或新开一个 Codex 任务，让 `jlceda` MCP 被加载。
2. 打开嘉立创EDA专业版。
3. 在嘉立创EDA扩展管理器里安装：

```text
C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\jlc-bridge\build\jlc-bridge.eext
```

4. 打开目标原理图或 PCB 工程。
5. 在 Codex 里直接描述 PCB 操作，例如：

```text
读取当前 PCB 状态
运行 DRC
把 U1 移到指定位置
给 GND 网络铺铜
查询 USB_DP / USB_DN 差分对
```

## 已验证能力

MCP 协议初始化和工具列表已测试通过。当前可列出 37 个工具，覆盖：

- PCB 状态读取
- PCB 截图
- DRC 检查
- 元件移动、批量移动、选择、删除
- 走线、过孔、删除走线
- 铺铜、禁布区
- 丝印查询和自动整理
- 差分对、等长组
- 原理图状态、网表、原理图 DRC
- 阻抗计算
- 走线载流宽度计算

## 相关 skill

已经安装并同步到本目录：

- [[eda-pcb]]
- [[easyeda-api]]

本机原有 PCB / 制造相关 skill：

- [[kicad]]
- [[jlcpcb]]
- [[bom]]
- [[lcsc]]
- [[datasheets]]
- [[spice]]
- [[emc]]

## 维护命令

查看 MCP 列表：

```powershell
codex mcp list
```

更新社区 MCP 源码：

```powershell
cd C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp
git pull
npm install
npm run build
```

重新构建嘉立创EDA扩展包：

```powershell
cd C:\Users\JOHO\Documents\Codex\2026-07-24\new-chat\work\jlcmcp\jlc-bridge
npm install
npm run build
```

## 注意事项

> [!warning]
> 这个 MCP 能实际修改 EDA 工程。执行移动元件、走线、删除、铺铜等操作前，应确认当前工程已保存或有备份。

> [!note]
> `hyl64/jlcmcp` 当前 GitHub releases 页面没有正式 release，安装记录使用的是源码 commit，而不是版本号。

> [!info]
> 如果 EDA 端没有安装或启动 `jlc-bridge.eext`，Codex 虽然能加载 `jlceda` MCP，但实际 PCB 操作会连不上 bridge。

## 外部链接

- [hyl64/jlcmcp](https://github.com/hyl64/jlcmcp)
- [hyl64/jlcmcp releases](https://github.com/hyl64/jlcmcp/releases)
- [easyeda/extension-dev-mcp-tools](https://github.com/easyeda/extension-dev-mcp-tools)
- [EasyEDA API Skill](https://github.com/easyeda/easyeda-api-skill)
