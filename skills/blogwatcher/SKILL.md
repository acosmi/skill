---
name: blogwatcher
description: "博客与 RSS 监控：用 blogwatcher CLI 监控博客与 RSS/Atom 订阅源更新，及时获取最新动态。当需要订阅或追踪博客/RSS 更新时触发。"
when_to_use: "想订阅某博客/网站、追踪其 RSS 更新时"
argument-hint: "[action] (可选 feed_url/keywords/limit)"
version: "1.0.0"
---

# 博客与 RSS 监控

订阅与追踪 RSS/Atom 源，第一时间获取更新。

## 何时使用

- 添加/移除 RSS/Atom 订阅源
- 检查订阅源有无新内容
- 按关键词读取最新文章

## 能力

- `add` 添加 · `list` 列出 · `check` 检查更新 · `read` 读取 · `remove` 移除

## 工作流

1. `add`/`remove` 带 `feed_url`。
2. `check`/`read` 可用 `keywords` 过滤、`limit` 控量。

## 常见陷阱

- feed_url 必须是有效 RSS/Atom 地址，普通网页不一定有 feed。
- 高频 check 注意目标站点限流。

## 输出

- 订阅列表、更新条目或文章内容。
