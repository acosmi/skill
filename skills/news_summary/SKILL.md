---
name: news-summary
description: "全球新闻摘要：从 BBC/路透/NPR/半岛等可信 RSS 获取新闻与每日简报，按主题分组并可生成语音摘要。当需要看头条、主题简报或每日简讯时触发。"
when_to_use: "想看新闻头条、某主题新闻或每日简报时"
argument-hint: "[action] (可选 topic/source/count/language/audio)"
version: "1.0.0"
---

# 全球新闻摘要

聚合可信来源的新闻，生成简报与语音摘要。

## 何时使用

- 获取头条新闻
- 按主题或来源筛选新闻
- 生成每日简报或语音摘要

## 能力

- `headlines` · `topic` · `briefing` · `source`

## 工作流

1. 选 `action`；按主题带 `topic`，按来源带 `source`。
2. 用 `count`/`language` 控量与语言，`audio=true` 生成语音。

## 常见陷阱

- 来源为英文媒体为主，中文需求注意 language。
- 新闻时效强，关注发布时间。

## 输出

- 新闻条目列表、简报文本或语音摘要。
