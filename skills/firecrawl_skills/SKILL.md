---
name: firecrawl-skills
description: "Firecrawl 搜索:用 Firecrawl 开展开放式研究、整理资料并沉淀研究文档,高效完成信息收集与知识沉淀。当需做研究调研时触发。"
when_to_use: "需要做开放式研究、整理结论或沉淀研究文档时。"
argument-hint: "[query] (搜索关键词, 可选 max_results/time_range)"
version: "1.0.0"
---

# Firecrawl 研究搜索

支持开展研究、整理资料并沉淀研究文档,适合在需要做开放式研究、整理结论或沉淀研究文档时调用,通过 Firecrawl 搜索高效完成信息收集与知识沉淀。

## 何时使用

- 开展开放式研究
- 整理资料与结论
- 沉淀研究文档
- 高效收集信息

## 工作流

1. 提供搜索关键词(query)。
2. 可设置 max_results、time_range(day/week/month/year)、language、region。
3. 可选 include_content 提取页面内容。
4. 整理结果并沉淀为研究文档。

## 常见陷阱

- query 为必填项。
- 提取页面内容会增加耗时。
- 需正确配置 Firecrawl 访问凭证。

## 输出

- 返回搜索结果并支持沉淀为研究文档。
