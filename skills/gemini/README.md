# Gemini 命令行
> Gemini CLI

使用 Gemini CLI 进行一次性问答、内容摘要和文本生成，快速调用 Google Gemini 模型能力。

## 概述

**Gemini 命令行** 是一个API集成领域的执行动作类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `prompt` | string | 是 | 问题或指令 |
| `task` | string | 否 | 任务类型 可选值: `qa`, `summarize`, `generate`, `analyze` |
| `input` | string | 否 | 附加输入内容（URL 或文本） |
| `model` | string | 否 | Gemini 模型名，默认 gemini-2.0-flash |

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
  "prompt": "示例问题或指令",
  "task": "qa",
  "input": "示例附加输入内容（URL 或文本）",
  "model": "示例Gemini 模型名，默认 g"
}
```

## 适用场景

- 第三方服务集成或 API 对接时
- 数据同步或跨平台操作时
- 服务编排或接口调试时

## 注意事项

- 技能标识: `gemini`
- 分类: 执行动作类 / API集成
- 必填参数: `prompt`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
