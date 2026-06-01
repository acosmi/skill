---
name: ga4-analytics
description: "GA4 分析集成:整合 Google Analytics 4、Search Console 与索引数据,查询站点流量与搜索表现。当用户想分析网站数据或 SEO 表现时触发。"
when_to_use: "用户想查询 GA4 网站流量、Search Console 搜索表现或索引数据时。"
argument-hint: "query (read/send/search/list)"
version: "1.0.0"
---

# GA4 分析集成

整合 Google Analytics 4、Search Console 与索引数据的查询技能。

## 何时使用

- 用户想分析网站流量
- 想查看搜索表现
- 想了解用户来源与页面浏览
- 想检查索引数据

## 能力

- read:读取分析数据
- send:提交查询
- search:搜索维度/指标
- list:列出报告/属性

## 工作流

1. 提供 query(维度/指标/问题)。
2. 选择 action(read 读数据,search 查询)。
3. 经鉴权调用 GA4/Search Console API,返回数据。

## 常见陷阱

- 必填 query;需配置 GA4_PROPERTY_ID、GA4_PRIVATE_KEY、SEARCH_CONSOLE_SITE_URL。
- GA4 数据有采样与延迟。
- 维度与指标组合需合法。

## 输出

- 网站流量、搜索表现与索引数据。
