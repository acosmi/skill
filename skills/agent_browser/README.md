# 智能体浏览器

基于 Rust 的高性能无头浏览器自动化 CLI，支持导航、点击、输入和页面快照，带有 Node.js 回退机制，专为 AI 智能体设计。

## 概述

**智能体浏览器** 是一个调研分析领域的执行动作类技能。支持 7 种操作模式：navigate, click, type, snapshot, scroll, wait。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **navigate** — navigate
- **click** — click
- **type** — type
- **snapshot** — snapshot
- **scroll** — scroll
- **wait** — wait
- **evaluate** — evaluate

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 浏览器操作类型 可选值: `navigate, click, type, snapshot, scroll, wait, evaluate` |
| `url` | string | 否 | 目标网页 URL（navigate 时必填） |
| `selector` | string | 否 | CSS 选择器或文本内容定位元素（click/type 时使用） |
| `text` | string | 否 | 要输入的文本内容（type 时必填） |
| `script` | string | 否 | 要执行的 JavaScript 代码（evaluate 时使用） |
| `timeout` | integer | 否 | 操作超时时间（秒），默认 30 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `content` | string | 页面文本内容或截图 base64 |
| `title` | string | 页面标题 |
| `url` | string | 当前页面 URL |
| `elements` | array | 匹配的页面元素列表 |

## 使用示例

### 示例 1: navigate

```json
{
  "action": "navigate",
  "url": "https://example.com/page",
  "selector": "示例值",
  "text": "示例要输入的文本内容（type 时必填）",
  "script": "示例值",
  "timeout": 10
}
```

### 示例 2: click

```json
{
  "action": "click",
  "url": "https://example.com/page",
  "text": "示例要输入的文本内容（type 时必填）",
  "timeout": 10
}
```

### 示例 3: type

```json
{
  "action": "type",
  "url": "https://example.com/page",
  "text": "示例要输入的文本内容（type 时必填）",
  "timeout": 10
}
```

### 示例 4: snapshot

```json
{
  "action": "snapshot",
  "url": "https://example.com/page",
  "text": "示例要输入的文本内容（type 时必填）",
  "timeout": 10
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `agent_browser`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
