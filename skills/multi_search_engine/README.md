# 多搜索引擎聚合

集成 17 个搜索引擎（8 个中文 + 9 个国际），支持高级搜索语法、时间过滤、站内搜索、隐私引擎和 WolframAlpha 知识查询，完全免费无需 API 密钥。

## 概述

**多搜索引擎聚合** 是一个调研分析领域的执行动作类技能。通过 5 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `query` | string | 是 | 搜索关键词 |
| `engines` | array | 否 | 指定搜索引擎（留空使用全部），可选：baidu/google/bing/duckduckgo/sogou/360/zhihu/bilibili/yandex/brave/wolfram 等 |
| `time_range` | string | 否 | 时间范围过滤 可选值: `day`, `week`, `month`, `year` |
| `site` | string | 否 | 站内搜索限定域名 |
| `max_results` | integer | 否 | 每个引擎最大结果数，默认 5 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `results` | array | 搜索结果列表 |
| `total` | integer | 总结果数 |
| `engines_used` | array | - |

## 使用示例


```json
{
  "query": "示例搜索关键词",
  "time_range": "day",
  "site": "示例站内搜索限定域名",
  "max_results": null
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `multi_search_engine`
- 分类: 执行动作类 / 调研分析
- 必填参数: `query`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
