# 股票与加密货币分析

使用 Yahoo Finance 数据分析股票和加密货币，支持投资组合管理、观察清单、股息分析、8 维度评分、趋势检测（热点扫描）和早期信号检测。

## 概述

**股票与加密货币分析** 是一个财务金融领域的执行动作类技能。支持 7 种操作模式：quote, 分析, portfolio, watchlist, dividends, 对比。通过 3 个可配置参数实现灵活控制。

## 功能特性

- **quote** — quote
- **analyze** — 分析
- **portfolio** — portfolio
- **watchlist** — watchlist
- **dividends** — dividends
- **compare** — 对比
- **trend** — trend

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 分析操作 可选值: `quote, analyze, portfolio, watchlist, dividends, compare, trend` |
| `symbol` | string | 否 | 股票/加密货币代码（如 AAPL/BTC-USD） |
| `symbols` | array | 否 | 多个代码（compare 时使用） |
| `period` | string | 否 | 时间周期 可选值: `1d`, `5d`, `1mo`, `3mo`, `6mo`, `1y`, `5y` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: quote

```json
{
  "action": "quote",
  "symbol": "示例值",
  "symbols": [
    "item1",
    "item2"
  ],
  "period": "1d"
}
```

### 示例 2: 分析

```json
{
  "action": "analyze",
  "symbols": [
    "item1",
    "item2"
  ],
  "period": "1d"
}
```

### 示例 3: portfolio

```json
{
  "action": "portfolio",
  "symbols": [
    "item1",
    "item2"
  ],
  "period": "1d"
}
```

### 示例 4: watchlist

```json
{
  "action": "watchlist",
  "symbols": [
    "item1",
    "item2"
  ],
  "period": "1d"
}
```

## 适用场景

- 财务报表分析或预算编制时
- 投资分析或风险评估时
- 发票管理或税务计算时

## 注意事项

- 技能标识: `stock_analysis`
- 分类: 执行动作类 / 财务金融
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
