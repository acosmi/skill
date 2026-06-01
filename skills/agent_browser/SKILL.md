---
name: agent-browser
description: "智能体浏览器：无头浏览器自动化，支持导航/点击/输入/滚动/等待/页面快照/执行JS。当需要访问网页、抓取内容或自动化网页操作时触发。"
when_to_use: "需要程序化访问网页、提取内容、截图或模拟点击/输入时"
argument-hint: "[action] (navigate 需 url，click/type 需 selector)"
version: "1.0.0"
---

# 智能体浏览器

基于 Rust 的高性能无头浏览器 CLI，带 Node.js 回退，专为 AI 智能体设计。

## 何时使用

- 抓取网页文本/结构化数据
- 自动化导航、点击、表单填写
- 对页面截图或快照供后续分析

## 能力（action）

- `navigate` 打开 URL · `click` 点击元素 · `type` 输入文本 · `snapshot` 页面快照
- `scroll` 滚动 · `wait` 等待 · `evaluate` 执行 JavaScript

## 工作流

1. 先 `navigate` 到目标 `url`。
2. 用 `selector`（CSS 或文本）定位元素，按需 `click` / `type`。
3. `snapshot` 获取页面内容或截图；复杂取数用 `evaluate` 执行 JS。
4. 必要时 `scroll` / `wait` 等待动态内容加载（`timeout` 默认 30s）。

## 常见陷阱

- navigate 必须先于 click/type；selector 失配是最常见失败，优先用稳定属性。
- 动态页面用 wait/timeout，不要假设元素立即就绪。

## 输出

- `success` 是否成功、`content` 文本或截图、`title` 标题、`url` 当前地址、`elements` 匹配元素。
