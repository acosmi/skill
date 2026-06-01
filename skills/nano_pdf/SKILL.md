---
name: nano-pdf
description: "PDF 自然语言编辑：用自然语言指令编辑 PDF（增删页/改文字/合并拆分等），无需复杂工具。当需要修改/处理 PDF 时触发。"
when_to_use: "用户给出 PDF 并用自然语言描述想做的修改时"
argument-hint: "[input] [instruction] (可选 output / pages)"
version: "1.0.0"
---

# PDF 自然语言编辑

使用 nano-pdf CLI，通过自然语言指令完成 PDF 编辑。

## 何时使用

- 按文字描述编辑 PDF 内容或页面
- 合并、拆分、删除/重排页面
- 为 PDF 添加文字、页码等

## 工作流

1. 提供 `input`（PDF 路径）与 `instruction`（自然语言指令）。
2. 可选 `pages` 限定作用页范围、`output` 指定输出路径。
3. 执行并返回结果文件路径。

## 常见陷阱

- 指令要明确目标页与动作，避免歧义（“删第2页”优于“删那页”）。
- 原文件重要时指定 output，避免就地覆盖丢失原件。

## 输出

- 处理后的 PDF 路径与操作摘要。
