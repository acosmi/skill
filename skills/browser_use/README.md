# Browser Use 浏览器自动化

通过 CLI 命令自动化浏览器交互，支持网站导航、表单填写、页面截图、数据提取和 Web 应用交互，适用于真实 Chromium 或无头浏览器。

## 概述

**Browser Use 浏览器自动化** 是一个调研分析领域的执行动作类技能。支持 8 种操作模式：navigate, click, type, screenshot, 提取, scroll。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **navigate** — navigate
- **click** — click
- **type** — type
- **screenshot** — screenshot
- **extract** — 提取
- **scroll** — scroll
- **wait** — wait
- **select** — select

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 浏览器操作 可选值: `navigate, click, type, screenshot, extract, scroll, wait, select` |
| `url` | string | 否 | 目标 URL（navigate 时必填） |
| `selector` | string | 否 | CSS/XPath 选择器 |
| `text` | string | 否 | 输入文本 |
| `headless` | boolean | 否 | 无头模式，默认 true |
| `timeout` | integer | 否 | 超时秒数，默认 30 |

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
  "text": "示例输入文本",
  "headless": true,
  "timeout": 10
}
```

### 示例 2: click

```json
{
  "action": "click",
  "url": "https://example.com/page",
  "text": "示例输入文本",
  "headless": true,
  "timeout": 10
}
```

### 示例 3: type

```json
{
  "action": "type",
  "url": "https://example.com/page",
  "text": "示例输入文本",
  "headless": true,
  "timeout": 10
}
```

### 示例 4: screenshot

```json
{
  "action": "screenshot",
  "url": "https://example.com/page",
  "text": "示例输入文本",
  "headless": true,
  "timeout": 10
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `browser_use`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
