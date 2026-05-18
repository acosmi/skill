# Firecrawl 搜索

Firecrawl 搜索 — 支持开展研究、整理资料并沉淀研究文档，适合在需要做开放式研究、整理结论或沉淀研究文档时调用通过Firecrawl 搜索高效完成信息收集和知识沉淀。

## 概述

**Firecrawl 搜索** 是一个调研分析领域的触发器类技能。通过 6 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `query` | string | 是 | 搜索关键词 |
| `max_results` | integer | 否 | 最大结果数，默认 10 |
| `time_range` | string | 否 | 时间过滤 可选值: `day`, `week`, `month`, `year` |
| `language` | string | 否 | 搜索语言 |
| `region` | string | 否 | 地区代码 |
| `include_content` | boolean | 否 | 是否提取页面内容 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `metadata` | object | 附加元信息 |

## 使用示例


```json
{
  "query": "示例搜索关键词",
  "max_results": null,
  "time_range": "day",
  "language": "示例搜索语言",
  "region": "示例地区代码",
  "include_content": true
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `firecrawl_skills`
- 分类: 触发器类 / 调研分析
- 必填参数: `query`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
