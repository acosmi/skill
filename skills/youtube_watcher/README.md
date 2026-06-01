# YouTube 视频分析

获取并阅读 YouTube 视频字幕，用于视频摘要、内容问答或从视频中提取特定信息，需要视频提供字幕或自动生成字幕。

## 概述

**YouTube 视频分析** 是一个多媒体处理领域的执行动作类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `url` | string | 是 | YouTube 视频 URL |
| `task` | string | 否 | 任务类型：summarize=生成摘要, qa=问答, extract=提取特定信息 可选值: `summarize`, `qa`, `extract` |
| `question` | string | 否 | 问题（qa 模式时使用） |
| `topic` | string | 否 | 要提取的主题（extract 模式时使用） |

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
  "task": "summarize",
  "question": "示例问题（qa 模式时使用）",
  "topic": "示例要提取的主题（extract "
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `youtube_watcher`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `url`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
