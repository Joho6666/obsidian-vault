---
type: entity
summary: "NVFP4 是 NVIDIA 面向模型量化与推理部署的重要格式，显著降低高参数模型的本地部署门槛。"
sources:
  - "raw 原始资料/projects 项目资料/Horizon/data/summaries/horizon-2026-05-31-zh.md"
updated: "2026-05-31"
---

# NVIDIA NVFP4

## 类型

- 量化格式
- 推理部署技术

## 本次新增信息

- 对 Qwen3.6-35B-A3B 的量化结果显示，内存/磁盘占用约缩小 3.06 倍，精度损失控制在 1% 以内。
- 已可直接用于 vLLM 推理。

## 为什么值得记录

- 它会直接影响“哪些模型能在消费级设备本地可用”。
- 对本地 RAG、本地助手和低成本 Agent 基础设施有现实意义。

## 关联概念

- [[wiki 知识层/concepts 概念页/本地 LLM 部署成本模型]]
- 量化
- MoE
- 本地 LLM

