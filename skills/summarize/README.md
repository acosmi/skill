# 内容摘要

使用 summarize CLI 对 URL 或文件（网页、PDF、图片、音频、YouTube 视频）生成摘要，无需 API 密钥。

## 概述

**内容摘要** 是一个多媒体处理领域的数据变换类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `source` | string | 是 | 要摘要的内容来源：URL（网页/YouTube）、文件路径（PDF/图片/音频）或纯文本 |
| `format` | string | 否 | 摘要输出格式：bullet=要点列表, paragraph=段落, tldr=一句话, structured=结构化 可选值: `bullet`, `paragraph`, `tldr`, `structured` |
| `language` | string | 否 | 输出语言，默认与原文一致 |
| `max_length` | integer | 否 | 摘要最大字数限制 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `summary` | string | 生成的摘要内容 |
| `source_type` | string | 识别的内容类型：webpage/pdf/image/audio/video/text |
| `word_count` | integer | 摘要字数 |
| `key_points` | array | 关键要点列表 |

## 使用示例


```json
{
  "source": "示例要摘要的内容来源：URL（网页",
  "format": "bullet",
  "language": "示例输出语言，默认与原文一致",
  "max_length": null
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `summarize`
- 分类: 数据变换类 / 多媒体处理
- 必填参数: `source`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
