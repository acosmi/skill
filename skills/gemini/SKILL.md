---
name: gemini
description: "Gemini CLI：用命令行做一次性问答、内容摘要、文本生成与分析，快速调用 Google Gemini。当需要快速问答或用 Gemini 生成/分析文本时触发。"
when_to_use: "需要快速向 Gemini 提问、生成或分析文本时"
argument-hint: "[prompt] (可选 task/input/model)"
version: "1.0.0"
---

# Gemini CLI

通过 Gemini CLI 即时调用 Google Gemini 能力。

## 何时使用

- 一次性问答
- 内容摘要与文本生成
- 对给定内容做分析

## 能力

- `task`：qa 问答 / summarize 摘要 / generate 生成 / analyze 分析

## 工作流

1. 提供 `prompt`。
2. 选 `task`，需处理已有内容时带 `input`。
3. 可用 `model` 指定 Gemini 模型。

## 常见陷阱

- 长文摘要受上下文上限约束。
- 一次性调用不保留会话记忆。

## 输出

- 模型回复（答案/摘要/生成内容/分析结论）。
