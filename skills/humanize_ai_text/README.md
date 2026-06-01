# AI 文本人性化

将 ChatGPT、Claude 等 AI 生成的文本改写得更自然，使其通过 GPTZero 等 AI 检测器，让内容更具人情味和真实感。

## 概述

**AI 文本人性化** 是一个写作创作领域的数据变换类技能。通过 3 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `text` | string | 是 | 需要人性化处理的 AI 生成文本 |
| `level` | string | 否 | 改写程度 可选值: `light`, `moderate`, `heavy` |
| `tone` | string | 否 | 目标语气 可选值: `casual`, `professional`, `academic` |

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
  "text": "示例需要人性化处理的 AI 生成文",
  "level": "light",
  "tone": "casual"
}
```

## 适用场景

- 需要撰写文案、博客、报告等文字内容时
- 创意写作或内容创作需要灵感时
- 文本润色、改写或风格调整时

## 注意事项

- 技能标识: `humanize_ai_text`
- 分类: 数据变换类 / 写作创作
- 必填参数: `text`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
