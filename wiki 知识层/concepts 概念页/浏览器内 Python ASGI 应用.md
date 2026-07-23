---
type: concept
summary: "利用 Pyodide 与 Service Worker，可以把部分 Python Web 应用搬到浏览器本地执行，形成零后端分发模式。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-05-31-zh.md"
updated: "2026-05-31"
---

# 浏览器内 Python ASGI 应用

## 定义

这类方案用 Pyodide 把 Python 运行时搬进浏览器，再利用 Service Worker 拦截请求，让 ASGI 应用在客户端本地运行。

## 这次新增认识

- 旧的 Web Worker 路线会卡在 `<script>` 执行能力，导致很多交互功能失效。
- 改用 Service Worker 后，可以保留更完整的网页行为，适合 Datasette 这类带插件或脚本依赖的应用。
- 这意味着“Python 小工具”不一定需要服务器，也不一定要改写成纯前端框架。

## 适用场景

- 可离线的知识库检索原型
- 课程辅助小工具
- 数据浏览器
- 可直接分享的演示应用

## 关键概念

- [[wiki 知识层/entities 实体页/Pyodide]]
- WebAssembly
- ASGI
- Service Worker
- 离线优先

## 对我的意义

- 很适合做轻量学习工具和可展示 demo。
- 对独立开发有价值，因为它降低了后端部署、账号、数据库等初始成本。

## 下一步问题

- 哪些现有 Python 工具最值得改造成浏览器离线版？
- 性能瓶颈在初始化、包体积还是浏览器存储？

