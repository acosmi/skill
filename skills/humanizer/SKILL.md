---
name: humanizer
description: "AI 文本去痕：检测并修复 24 种 AI 写作特征，让文本更自然像人写、可保意。当需要让 AI 文本更像人写时触发。"
when_to_use: "用户有一段 AI 味重的文本想改得更自然时"
argument-hint: "[text] (可选 intensity / style / preserve_meaning)"
version: "1.0.0"
---

# AI 文本去痕

基于「AI 写作特征」指南，去除文本中的机器味。

## 何时使用

- 去除 em 破折号滥用、套话词汇、冗余连词等 AI 特征
- 在保持原意前提下让行文更自然

## 工作流

1. 提供 `text`。
2. 选 `intensity`：light / moderate / aggressive。
3. 选 `style`：casual / professional / academic / creative。
4. `preserve_meaning=true` 时严格保意。

## 常见陷阱

- aggressive 强度可能改动语义，重要文本配 preserve_meaning。
- 过度去痕会显得刻意，按场景选强度。

## 输出

- 改写后的文本（及可选的修改点说明）。
