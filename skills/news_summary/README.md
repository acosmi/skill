# 全球新闻摘要

从 BBC、路透社、NPR、半岛电视台等可信 RSS 订阅获取新闻更新和每日简报，支持按主题分组，可生成语音摘要。

## 概述

**全球新闻摘要** 是一个多媒体处理领域的执行动作类技能。支持 4 种操作模式：头条新闻, 按主题, 每日简报, 按来源。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **headlines** — 头条新闻
- **topic** — 按主题
- **briefing** — 每日简报
- **source** — 按来源

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 新闻操作：headlines=头条, topic=按主题, briefing=每日简报, source=按来源 可选值: `headlines, topic, briefing, source` |
| `topic` | string | 否 | 新闻主题（technology/business/science/health/sports/world） |
| `source` | string | 否 | 新闻来源（bbc/reuters/npr/aljazeera） |
| `count` | integer | 否 | 新闻数量，默认 10 |
| `language` | string | 否 | 语言过滤 |
| `audio` | boolean | 否 | 是否生成语音摘要 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 头条新闻

```json
{
  "action": "headlines",
  "topic": "示例值",
  "source": "示例值",
  "count": 10,
  "language": "示例值",
  "audio": true
}
```

### 示例 2: 按主题

```json
{
  "action": "topic",
  "count": 10,
  "audio": true
}
```

### 示例 3: 每日简报

```json
{
  "action": "briefing",
  "count": 10,
  "audio": true
}
```

### 示例 4: 按来源

```json
{
  "action": "source",
  "count": 10,
  "audio": true
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `news_summary`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
