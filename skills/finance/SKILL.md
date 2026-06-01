---
name: finance
description: "金融数据:用公共 API 获取股票/ETF/指数、外汇与加密货币的最新报价与历史序列。支持运行、查询、配置、查看状态。当你要查行情时触发。"
when_to_use: "需要查询股票/外汇/加密货币的最新报价或历史数据时"
argument-hint: "[action] (input/params/output_format)"
version: "1.0.0"
---

# 金融市场数据

使用公共 API 获取股票/ETF/指数(如 AAPL、MSFT、^GSPC、VOO)、外汇对(如 USD/ZAR、EURUSD)和加密货币的最新报价与历史序列。

## 何时使用

- 需要查询股票、ETF 或指数的实时报价
- 需要查询外汇对汇率
- 需要查询加密货币行情
- 需要获取历史价格序列

## 能力

- run:执行数据获取
- query:查询报价或历史数据
- configure:配置数据源
- status:查看状态

## 工作流

1. 选择 action,通过 input 提供代码(如 AAPL、EURUSD)
2. 用 params 指定时间范围等参数
3. 选择 output_format(json/text/markdown)
4. 获取报价或历史序列

## 常见陷阱

- action 为必填项
- 代码格式需符合所查市场规范
- 数据来自公共 API,可能有延迟或限频

## 输出

- 返回最新报价或历史价格序列数据
