# 博客与 RSS 监控

博客与 RSS 监控 — 使用 blogwatcher CLI 监控博客和 RSS/Atom 订阅源的更新，及时获取关注内容的最新动态。

## 概述

**博客与 RSS 监控** 是一个效率工具领域的触发器类技能。支持 5 种操作模式：写入, rewrite, polish, expand, 摘要。通过 3 个可配置参数实现灵活控制。

## 功能特性

- **write** — 写入
- **rewrite** — rewrite
- **polish** — polish
- **expand** — expand
- **summarize** — 摘要

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 写作操作类型 可选值: `write, rewrite, polish, expand, summarize` |
| `text` | string | 是 | 输入文本内容 |
| `style` | string | 否 | 目标写作风格 |
| `language` | string | 否 | 输出语言 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 写入

```json
{
  "action": "write",
  "text": "示例输入文本内容",
  "style": "示例值",
  "language": "示例值"
}
```

### 示例 2: rewrite

```json
{
  "action": "rewrite",
  "text": "示例输入文本内容"
}
```

### 示例 3: polish

```json
{
  "action": "polish",
  "text": "示例输入文本内容"
}
```

### 示例 4: expand

```json
{
  "action": "expand",
  "text": "示例输入文本内容"
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `blogwatcher`
- 分类: 触发器类 / 效率工具
- 必填参数: `text`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
