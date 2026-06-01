---
name: summarize
description: "内容摘要：对网页/PDF/图片/音频/YouTube/纯文本生成摘要，支持要点/段落/一句话/结构化格式，无需 API 密钥。当需要快速提炼长内容时触发。"
when_to_use: "用户给出 URL、文件或长文本并想要摘要/要点/TLDR 时"
argument-hint: "[source] (可选 format / language / max_length)"
version: "1.0.0"
---

# 内容摘要

使用 summarize CLI 对多种来源生成摘要，自动识别内容类型。

## 何时使用

- 需要把长网页/文档/视频压缩成要点或一句话
- 跨格式（PDF、图片、音频、YouTube）统一提炼

## 工作流

1. 接收 `source`：URL（网页/YouTube）、文件路径（PDF/图片/音频）或纯文本。
2. 选择 `format`：bullet（要点）/ paragraph（段落）/ tldr（一句话）/ structured（结构化）。
3. 可选设置 `language`（默认随原文）与 `max_length`（字数上限）。
4. 生成摘要并标注识别到的内容类型与关键要点。

## 参数

- `source`（必填）。
- `format`、`language`、`max_length`（可选）。

## 常见陷阱

- source 是本地文件时确保路径可访问；是 YouTube 时确保有字幕。
- max_length 过小会丢失关键信息，结构化场景优先用 structured。

## 输出

- `summary` 摘要、`source_type` 内容类型、`word_count` 字数、`key_points` 关键要点。
