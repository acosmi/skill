---
name: model-usage
description: "模型用量与成本统计：用 CodexBar CLI 按模型汇总 Codex/Claude 用量与成本，支持当前/全量明细，输出 JSON/文本/表格。当需要查看用量或成本时触发。"
when_to_use: "想知道某模型用了多少 token、花了多少成本时"
argument-hint: "[scope] (可选 format/period/model)"
version: "1.0.0"
---

# 模型用量与成本统计

按模型聚合用量与成本，便于成本复盘。

## 何时使用

- 查看当前模型或全部模型的用量
- 按时段统计成本
- 导出 JSON/文本/表格

## 能力

- `scope`：current 当前模型 / all 全部

## 工作流

1. 选 `scope`；可指定单个 `model`。
2. 用 `period`(today/week/month/all) 限定时段、`format` 选输出。

## 常见陷阱

- 统计依赖本地用量记录，缺数据则不全。
- 成本为估算，以官方账单为准。

## 输出

- 按模型的用量与成本明细（JSON/文本/表格）。
