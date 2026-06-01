# YouTube 字幕提取

通过 yt-dlp 直接从 YouTube 视频 URL 提取字幕和文本，无需音频处理，快速获取视频内容文字版。

## 概述

**YouTube 字幕提取** 是一个多媒体处理领域的数据变换类技能。通过 3 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `url` | string | 是 | YouTube 视频 URL |
| `language` | string | 否 | 字幕语言代码（如 zh/en），留空自动选择 |
| `format` | string | 否 | 输出格式 可选值: `text`, `srt`, `json` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例


```json
{
  "url": "示例YouTube 视频 URL",
  "language": "示例字幕语言代码（如 zh/en）",
  "format": "text"
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `youtube_transcript`
- 分类: 数据变换类 / 多媒体处理
- 必填参数: `url`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
