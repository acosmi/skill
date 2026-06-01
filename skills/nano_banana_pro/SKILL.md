---
name: nano-banana-pro
description: "AI 图片生成与编辑：用 Gemini 3 Pro 图像模型文生图与编辑，分辨率 1K/2K/4K，支持参考图。当需要生成或编辑图片时触发。"
when_to_use: "需要根据文字生成图片，或基于参考图编辑图片时"
argument-hint: "[prompt] (可选 action/input_image/resolution/style)"
version: "1.0.0"
---

# AI 图片生成与编辑

基于 Nano Banana Pro 完成高质量文生图与图片编辑。

## 何时使用

- 根据文字描述生成图片
- 基于参考图进行编辑/改写
- 按需输出 1K/2K/4K 分辨率

## 能力

- `generate` 文生图 · `edit` 基于 `input_image` 编辑

## 工作流

1. 提供 `prompt`（必填，描述画面）。
2. `action=edit` 时给 `input_image`。
3. 可选 `resolution`(1k/2k/4k)、`style`、`output`。

## 常见陷阱

- edit 必须提供 input_image，否则退化为纯生成。
- 4k 更慢更贵，预览用 1k/2k。

## 输出

- 生成/编辑后的图片路径或 URL。
