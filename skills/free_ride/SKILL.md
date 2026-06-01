---
name: free-ride
description: "FreeRide 免费模型网关：聚合管理免费 AI 模型额度，支持列模型/对话/状态/切换。当需要用免费模型对话或切换时触发。"
when_to_use: "想用免费 AI 模型对话，或在多个免费模型间切换时"
argument-hint: "[action] (可选 prompt/model)"
version: "1.0.0"
---

# FreeRide 免费模型网关

管理来自 OpenRouter 等渠道的免费模型额度并统一调用。

## 何时使用

- 列出可用的免费模型
- 用免费模型直接对话
- 查看额度状态、切换默认模型

## 能力

- `list_models` · `chat` · `status` · `switch_model`

## 工作流

1. `chat` 带 `prompt`；可用 `model` 指定模型。
2. `switch_model` 设默认模型；`status` 看额度。

## 常见陷阱

- 免费模型有速率/额度限制，高强度任务可能被限流。
- 不同模型能力差异大，按任务选型。

## 输出

- 模型列表、对话回复或额度状态。
