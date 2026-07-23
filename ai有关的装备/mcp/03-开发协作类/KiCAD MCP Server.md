---
type: mcp
status: installed
updated: 2026-07-19
tags:
  - mcp
  - kicad
  - pcb
  - hardware
---

# KiCAD MCP Server

> [!summary]
> KiCAD MCP Server 可以让 Codex/支持 MCP 的客户端通过工具调用控制 KiCad：创建项目、画 PCB、放封装、走线、铺铜、导出 Gerber/BOM/视图等。适合 PCB 自动化草图、硬件设计辅助、KiCad 项目检查与制造文件导出。

## 来源

- GitHub：<https://github.com/mixelpixx/KiCAD-MCP-Server>
- README：<https://github.com/mixelpixx/KiCAD-MCP-Server/blob/main/.github/README.zh.md>
- 本机安装目录：`C:\Users\JOHO\Documents\Codex\2026-07-19\readme-zh-md-https-github-com\work\KiCAD-MCP-Server`
- KiCad 安装目录：`E:\kidcad`
- KiCad 版本：`10.0.4`

## Codex 配置

配置文件：`C:\Users\JOHO\.codex\config.toml`

```toml
[mcp_servers.kicad]
command = "node"
args = ['C:\Users\JOHO\Documents\Codex\2026-07-19\readme-zh-md-https-github-com\work\KiCAD-MCP-Server\dist\index.js']
startup_timeout_sec = 30

[mcp_servers.kicad.env]
NODE_ENV = "production"
PYTHONPATH = 'E:\kidcad\bin\Lib\site-packages'
PATH = 'E:\kidcad\bin;...'
LOG_LEVEL = "info"
KICAD_AUTO_LAUNCH = "false"
KICAD_INTERACTIVE_SCHEMATIC = "false"
KICAD_MCP_DEV = "0"
```

> [!note]
> 关键点是 `PYTHONPATH` 必须指向 KiCad 自带 Python 的 `site-packages`，并且 `PATH` 里要包含 `E:\kidcad\bin`，否则 Python 能找到 `pcbnew.py` 但会因为 DLL 路径缺失而导入失败。

## 已验证状态

- Node / npm / Python / Git 环境满足要求。
- KiCad 的 Python API 可导入：`pcbnew.GetBuildVersion()` 返回 `10.0.4`。
- MCP 服务启动日志出现：`KiCAD MCP SERVER READY`。
- Codex MCP 列表中 `kicad` 为 `enabled`。
- 实测可通过 MCP 创建 KiCad 项目、画板框、放封装、加文字、建 net、走线、加 via、铺铜、导出 SVG / Gerber / Drill。

## 实战样例

### 简单 demo

位置：

- `C:\Users\JOHO\Documents\Codex\2026-07-19\readme-zh-md-https-github-com\outputs\kicad_mcp_demo`

内容：

- 60mm × 40mm 圆角 PCB
- 丝印文字
- 2D SVG 视图导出

### ESP32 传感器节点 demo

位置：

- `C:\Users\JOHO\Documents\Codex\2026-07-19\readme-zh-md-https-github-com\outputs\esp32_sensor_node_mcp_v2`

内容：

- ESP32-WROOM-32E 模块
- USB-C 接口
- 3.3V LDO 电源区
- LiPo 电池接口
- I2C 传感器排针
- UART/SWD 调试排针
- RESET / BOOT 按键
- 状态 LED、电阻、电容
- 92mm × 58mm 圆角板框
- 4 个安装孔
- 多个 net、30 段走线、10 个过孔、GND 铜皮
- Gerber 和 Drill 文件已导出

## 主要能力

- 项目：新建、打开、保存 KiCad 项目。
- PCB：设置板子尺寸、画板框、加安装孔、加丝印、查询层和板子信息。
- 元件：放置、移动、旋转、查询封装和焊盘。
- 网络：创建 net、查询 net、走线、打 via、差分线、GND stitching vias。
- 规则：设置设计规则、检查 clearance、运行 DRC。
- 输出：导出 Gerber、Drill、PDF、SVG、3D、BOM、坐标文件。

## 使用注意

- 这个 MCP 更适合快速生成 PCB 草图、自动化布局/布线样例、批量导出和设计检查；正式打样前仍需要人工检查原理图、封装、管脚映射、电气规则和 DFM。
- KiCad 10 的层名在该 MCP 中显示为 `F.Silkscreen` / `B.Silkscreen`，不是常见简写 `F.SilkS` / `B.SilkS`。
- `place_component` 实测中 `componentId` 需要填 footprint 全名，例如 `RF_Module:ESP32-WROOM-32E`，不能只填 `U1` / `R1` 这种参考编号。
- MCP 调用较重的命令时偶尔会出现超时或响应顺序错位；Gerber/Drill 导出可直接用 `E:\kidcad\bin\kicad-cli.exe` 兜底。

## 可继续探索

- 用自然语言生成一个完整传感器板的 PCB 草图。
- 对已有 `.kicad_pro` / `.kicad_pcb` 做 DRC、BOM、Gerber 导出。
- 把 MCP 输出和 [[ai有关的装备/skills/04-编程开发与网页类/kicad|kicad skill]] 结合，做 PCB 设计审查。
- 与 [[ai有关的装备/skills/04-编程开发与网页类/jlcpcb|jlcpcb]] / [[ai有关的装备/skills/04-编程开发与网页类/bom|bom]] / [[ai有关的装备/skills/04-编程开发与网页类/datasheets|datasheets]] 串成硬件设计工作流。
