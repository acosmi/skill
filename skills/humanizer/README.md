# AI 文本去痕

去除文本中的 AI 写作特征，使其更自然、更像人类书写。基于维基百科「AI 写作特征」指南，检测并修复 24 种模式，包括 em 破折号滥用、AI 词汇、冗余连词等。

## 概述

**AI 文本去痕** 是一个写作创作领域的数据变换类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `text` | string | 是 | 需要去痕处理的 AI 生成文本 |
| `intensity` | string | 否 | 去痕强度：light=轻度调整, moderate=中度改写, aggressive=深度重写 可选值: `light`, `moderate`, `aggressive` |
| `preserve_meaning` | boolean | 否 | 是否严格保留原意，默认 true |
| `style` | string | 否 | 输出文风 可选值: `casual`, `professional`, `academic`, `creative` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `text` | string | 去痕后的文本 |
| `changes` | array | 修改点列表 |
| `ai_score_before` | number | 处理前 AI 检测分数 |
| `ai_score_after` | number | 处理后 AI 检测分数 |
| `patterns_fixed` | integer | 修复的 AI 写作模式数量 |

## 使用示例


```json
{
  "text": "示例需要去痕处理的 AI 生成文本",
  "intensity": "light",
  "preserve_meaning": true,
  "style": "casual"
}
```

## 适用场景

- 需要撰写文案、博客、报告等文字内容时
- 创意写作或内容创作需要灵感时
- 文本润色、改写或风格调整时

## 注意事项

- 技能标识: `humanizer`
- 分类: 数据变换类 / 写作创作
- 必填参数: `text`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
