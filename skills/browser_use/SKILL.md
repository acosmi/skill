---
name: browser-use
description: "Browser Use 浏览器自动化：CLI 自动化导航/点击/输入/截图/提取/滚动/等待，支持真实 Chromium 或无头。当需要自动化网页操作或抓取时触发。"
when_to_use: "需要程序化操作网页、提取数据或截图时"
argument-hint: "[action] (navigate 需 url，click/type 需 selector)"
version: "1.0.0"
---

# Browser Use 浏览器自动化

用 CLI 命令驱动真实或无头浏览器完成网页交互。

## 何时使用

- 导航网站、点击与填表
- 截图与提取页面数据
- 滚动与等待动态内容

## 能力

- `navigate` · `click` · `type` · `screenshot` · `extract` · `scroll` · `wait` · `select`

## 工作流

1. 先 `navigate` 到 `url`。
2. 用 `selector` 定位元素做 click/type/extract。
3. 可设 `headless` 与 `timeout`。

## 常见陷阱

- selector 失配是主要失败点；动态页配 wait/timeout。
- navigate 必须先于交互操作。

## 输出

- 操作结果、页面文本/截图或提取的数据。
