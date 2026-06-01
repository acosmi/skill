---
name: browser-automation
description: "自然语言浏览器自动化：用自然语言 CLI 指令自动化网页浏览/提取/截图/表单，无需写代码。当需要用自然语言驱动网页操作时触发。"
when_to_use: "想用自然语言描述来自动化网页操作而不写代码时"
argument-hint: "[action] (可选 url/instruction/selector/text)"
version: "1.0.0"
---

# 自然语言浏览器自动化

用自然语言指令驱动浏览器完成网页操作。

## 何时使用

- 用自然语言浏览网站、点击与填表
- 提取网页数据
- 截图与滚动等待

## 能力

- `navigate` · `click` · `type` · `screenshot` · `extract` · `scroll` · `wait`

## 工作流

1. 先 `navigate` 到 `url`。
2. 用 `instruction` 自然语言描述目标，或 `selector` 精确定位；输入带 `text`。

## 常见陷阱

- 自然语言指令要具体（“点右上角登录”优于“登录”）。
- 动态页面用 wait 等待加载。

## 输出

- 操作结果、提取的数据或截图。
