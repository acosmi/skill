---
name: stock-analysis
description: "股票与加密货币分析：基于 Yahoo Finance 报价/分析/组合/观察清单/股息/对比/热点扫描/早期信号。当需要分析行情或管理组合时触发。"
when_to_use: "需要查股票/加密报价、做分析或管理投资组合时"
argument-hint: "[action] (可选 symbol/symbols/period)"
version: "1.0.0"
---

# 股票与加密货币分析

用 Yahoo Finance 数据做多维度行情与组合分析。

## 何时使用

- 查实时报价与基本面
- 8 维度评分与趋势/热点扫描
- 管理投资组合与观察清单、股息与多标的对比

## 能力

- `quote` · `analyze` · `portfolio` · `watchlist` · `dividends` · `compare` · `trend` 等

## 工作流

1. 选 `action`；单标的带 `symbol`，多标的带 `symbols`。
2. 用 `period`(1d/5d/1mo/3mo/6mo/1y/5y) 控制区间。

## 常见陷阱

- 数据有延迟，非实盘交易依据。
- 加密与美股代码格式不同，确认 symbol 正确。

## 输出

- 报价/分析/评分、组合或对比结果。
