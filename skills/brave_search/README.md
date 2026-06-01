# Brave 网络搜索

通过 Brave Search API 进行网页搜索和内容提取，适用于搜索文档、事实核查或任何网络内容，轻量高效无需浏览器。

## 概述

**Brave 网络搜索** 是一个调研分析领域的执行动作类技能。通过 5 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `query` | string | 是 | 搜索关键词 |
| `count` | integer | 否 | 返回结果数量，默认 10，最大 20 |
| `freshness` | string | 否 | 时间过滤：pd=24h, pw=一周, pm=一月, py=一年 可选值: `pd`, `pw`, `pm`, `py` |
| `country` | string | 否 | 国家代码过滤（如 CN/US/JP） |
| `search_lang` | string | 否 | 搜索语言（如 zh-hans/en） |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `results` | array | 搜索结果 |
| `query` | string | - |
| `total` | integer | - |

## 使用示例


```json
{
  "query": "示例搜索关键词",
  "count": null,
  "freshness": "pd",
  "country": "示例国家代码过滤（如 CN/US/",
  "search_lang": "示例搜索语言（如 zh-hans/"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `brave_search`
- 分类: 执行动作类 / 调研分析
- 必填参数: `query`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
