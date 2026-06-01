---
name: humanize-ai-text
description: "AI 文本人性化：把 AI 生成文本改写得更自然、更有人情味，帮助通过 GPTZero 等检测器。当需要降低 AI 检测率或更像人写时触发。"
when_to_use: "用户想让一段 AI 文本更自然或通过 AI 检测时"
argument-hint: "[text] (可选 level/tone)"
version: "1.0.0"
---

# AI 文本人性化

改写 AI 文本的句式与用词，使其更接近人类写作。

## 何时使用

- 让 AI 生成内容读起来更自然
- 降低被 AI 检测器判定的概率

## 工作流

1. 提供 `text`。
2. 选 `level`：light / moderate / heavy。
3. 选 `tone`：casual / professional / academic。

## 常见陷阱

- heavy 可能改动语义；正式材料慎用。
- 检测器持续更新，不保证 100% 通过。

## 输出

- 人性化改写后的文本。
