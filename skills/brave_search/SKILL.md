---
name: brave-search
description: "Brave 网络搜索：通过 Brave Search API 网页搜索与内容提取，支持时效过滤与地区/语言，轻量无需浏览器。当需要网页搜索或事实核查时触发。"
when_to_use: "需要快速做网页搜索、查资料或事实核查时"
argument-hint: "[query] (可选 count/freshness/country/search_lang)"
version: "1.0.0"
---

# Brave 网络搜索

用 Brave Search API 高效检索网络内容。

## 何时使用

- 搜索网页、查找文档与事实
- 按时效/地区/语言过滤结果

## 工作流

1. 提供 `query`。
2. 可选 `count` 数量、`freshness`(pd/pw/pm/py 近一天/周/月/年)。
3. 可选 `country`、`search_lang`。

## 常见陷阱

- freshness 仅四档；要最新资讯用 pd/pw。
- count 过大可能被 API 限制。

## 输出

- 搜索结果列表（标题、摘要、链接）。
