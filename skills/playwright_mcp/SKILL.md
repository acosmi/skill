---
name: playwright-mcp
description: "Playwright MCP 浏览器：经 Playwright MCP 服务器做完整浏览器自动化——导航/点击/填写/截图/提取文本/选择/悬停。当需要稳定网页自动化或抓取时触发。"
when_to_use: "需要稳定可靠地自动化网页操作、表单或抓取时"
argument-hint: "[action] (navigate 需 url，click/fill 需 selector)"
version: "1.0.0"
---

# Playwright MCP 浏览器

基于 Playwright MCP 的高可靠浏览器自动化。

## 何时使用

- 导航、点击、填写表单
- 截图与提取文本
- 下拉选择、悬停等复杂交互

## 能力

- `navigate` · `click` · `fill` · `screenshot` · `extract_text` · `select` · `hover`

## 工作流

1. 先 `navigate` 到 `url`。
2. 用 `selector` 定位元素，fill 带 `text`，可执行 `script`。
3. 可设 `path`（截图保存）与 `timeout`。

## 常见陷阱

- selector 优先用稳定属性；动态页配 timeout。
- navigate 必须先于交互。

## 输出

- 操作结果、提取文本或截图。
