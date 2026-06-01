---
name: multi-search-engine
description: "多搜索引擎聚合：集成 17 个引擎（8 中文+9 国际），支持高级语法、时间过滤、站内/隐私搜索与知识查询，全免费。当需要多源搜索时触发。"
when_to_use: "需要跨多个搜索引擎检索、对比或做隐私搜索时"
argument-hint: "[query] (可选 engines/time_range/site/max_results)"
version: "1.0.0"
---

# 多搜索引擎聚合

一处覆盖 17 个搜索引擎，免费无需 API 密钥。

## 何时使用

- 跨多引擎检索同一问题并聚合
- 站内搜索、时间范围过滤
- 用隐私引擎搜索、做知识计算

## 工作流

1. 提供 `query`。
2. 可选 `engines` 限定引擎、`time_range`(day/week/month/year)。
3. 可选 `site` 站内搜、`max_results` 控制数量。

## 常见陷阱

- 引擎名需在支持列表内；空 engines 走默认聚合。
- 站内搜的 site 用裸域名。

## 输出

- 聚合后的搜索结果列表（标题、摘要、链接）。
