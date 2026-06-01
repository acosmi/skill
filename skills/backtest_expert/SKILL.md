---
name: backtest-expert
description: "交易策略系统化回测的专家指导,优先稳健性而非乐观结果。当需要回测策略、评估稳健性时触发。"
when_to_use: "需要对交易策略做系统化回测并评估稳健性时"
argument-hint: "[action: run|configure|status|help] (可选 input/output_format)"
version: "1.0.0"
---

# 回测专家

基于专业方法论对交易策略进行系统化回测,优先稳健性而非乐观结果。

## 何时使用

- 需要对一个交易策略做回测
- 需要评估策略在不同条件下的稳健性
- 需要避免过拟合、识别乐观偏差
- 需要规范化的回测流程指导

## 能力

- `run`:运行一次回测
- `configure`:配置回测参数
- `status`:查看回测状态
- `help`:查看用法说明

## 工作流

1. 选择 action(run/configure/status/help)。
2. 通过 input 提供策略或数据,通过 options 设置参数。
3. 通过 output_format 选择结果格式。

## 常见陷阱

- action 为必填参数。
- 警惕过拟合与乐观偏差,优先稳健性。
- 回测结果不代表实盘表现。

## 输出

- 返回回测指标与稳健性评估结论。
