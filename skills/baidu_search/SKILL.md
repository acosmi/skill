---
name: baidu-search
description: "百度 AI 搜索：获取实时中文信息、文档与研究内容，支持时间过滤与数量控制，专为中文优化。当需要中文网络搜索时触发。"
when_to_use: "需要检索中文实时信息、国内资讯或中文资料时"
argument-hint: "[query] (可选 count/time_range/site)"
version: "1.0.0"
---

# 百度 AI 搜索

用百度 AI 搜索引擎做中文优化的网络检索。

## 何时使用

- 检索中文实时信息与资讯
- 查找中文文档与研究内容
- 按时间范围与站点过滤

## 工作流

1. 提供 `query`（中文命中更佳）。
2. 可选 `count`、`time_range`(day/week/month/year)、`site` 站内搜。

## 常见陷阱

- 中文场景优于通用英文引擎；英文需求改用其他搜索技能。

## 输出

- 搜索结果列表（标题、摘要、链接）。
