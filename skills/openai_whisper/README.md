# Whisper 语音转文字

使用本地 Whisper CLI 实现离线语音转文字，无需 API 密钥，支持多种语言和音频格式，保护数据隐私。

## 概述

**Whisper 语音转文字** 是一个多媒体处理领域的数据变换类技能。通过 5 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `audio_file` | string | 是 | 音频文件路径，支持 mp3/wav/m4a/flac/ogg 格式 |
| `language` | string | 否 | 音频语言代码（如 zh/en/ja），留空自动检测 |
| `model` | string | 否 | Whisper 模型大小，越大越准但越慢 可选值: `tiny`, `base`, `small`, `medium`, `large` |
| `output_format` | string | 否 | 输出格式：纯文本/SRT字幕/VTT字幕/JSON 可选值: `text`, `srt`, `vtt`, `json` |
| `translate` | boolean | 否 | 是否翻译为英文 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `text` | string | 转写的文本内容 |
| `language` | string | 检测到的语言 |
| `duration` | number | 音频时长（秒） |
| `segments` | array | 带时间戳的分段列表 |

## 使用示例


```json
{
  "audio_file": "示例音频文件路径，支持 mp3/w",
  "language": "示例音频语言代码（如 zh/en/",
  "model": "tiny",
  "output_format": "text",
  "translate": true
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `openai_whisper`
- 分类: 数据变换类 / 多媒体处理
- 必填参数: `audio_file`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
