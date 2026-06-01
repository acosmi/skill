# Playwright MCP 浏览器

通过 Playwright MCP 服务器实现完整的浏览器自动化，支持网站导航、元素点击、表单填写、数据提取和页面截图。

## 概述

**Playwright MCP 浏览器** 是一个调研分析领域的执行动作类技能。支持 9 种操作模式：navigate, click, fill, screenshot, 提取text, select。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **navigate** — navigate
- **click** — click
- **fill** — fill
- **screenshot** — screenshot
- **extract_text** — 提取text
- **select** — select
- **hover** — hover
- **wait_for** — waitfor
- **evaluate** — evaluate

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | Playwright 操作 可选值: `navigate, click, fill, screenshot, extract_text, select, hover, wait_for, evaluate` |
| `url` | string | 否 | 导航目标 URL |
| `selector` | string | 否 | CSS/文本选择器 |
| `text` | string | 否 | 输入文本（fill 时使用） |
| `script` | string | 否 | JavaScript 代码（evaluate 时使用） |
| `path` | string | 否 | 截图保存路径 |
| `timeout` | integer | 否 | 等待超时 ms |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: navigate

```json
{
  "action": "navigate",
  "url": "https://example.com/page",
  "selector": "示例值",
  "text": "示例输入文本（fill 时使用）",
  "script": "示例值",
  "path": "/path/to/file.txt",
  "timeout": 10
}
```

### 示例 2: click

```json
{
  "action": "click",
  "url": "https://example.com/page",
  "text": "示例输入文本（fill 时使用）",
  "path": "/path/to/file.txt",
  "timeout": 10
}
```

### 示例 3: fill

```json
{
  "action": "fill",
  "url": "https://example.com/page",
  "text": "示例输入文本（fill 时使用）",
  "path": "/path/to/file.txt",
  "timeout": 10
}
```

### 示例 4: screenshot

```json
{
  "action": "screenshot",
  "url": "https://example.com/page",
  "text": "示例输入文本（fill 时使用）",
  "path": "/path/to/file.txt",
  "timeout": 10
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `playwright_mcp`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
