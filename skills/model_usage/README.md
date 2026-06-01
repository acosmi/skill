# 模型用量与成本统计

使用 CodexBar CLI 按模型汇总 Codex 或 Claude 的用量和成本数据，支持当前模型或全量模型明细，提供 JSON 和文本两种输出格式。

## 概述

**模型用量与成本统计** 是一个效率工具领域的执行动作类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `scope` | string | 是 | 统计范围：current=当前模型, all=全量模型 可选值: `current`, `all` |
| `format` | string | 否 | 输出格式 可选值: `json`, `text`, `table` |
| `period` | string | 否 | 统计周期 可选值: `today`, `week`, `month`, `all` |
| `model` | string | 否 | 指定模型名（留空统计全部） |

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
  "scope": "current",
  "format": "json",
  "period": "today",
  "model": "示例指定模型名（留空统计全部）"
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `model_usage`
- 分类: 执行动作类 / 效率工具
- 必填参数: `scope`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
