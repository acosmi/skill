---
name: automation-workflows
description: "自动化工作流设计：识别机会、设计流程、选型 Zapier/Make/n8n、规划测试维护。当需要设计自动化流程或选型自动化工具时触发。"
when_to_use: "用户想把某项重复性业务自动化、需要方案或工具选型时"
argument-hint: "[action] [goal] (可选 platform/constraints)"
version: "1.0.0"
---

# 自动化工作流设计

从机会识别到落地维护，规划端到端自动化方案。

## 何时使用

- 识别哪些重复劳动值得自动化
- 设计触发—动作—分支的工作流
- 在 Zapier/Make/n8n 间做工具选型
- 规划测试与长期维护

## 能力

- `identify` 机会识别 · `design` 工作流设计 · `select_tool` 工具选型 · `plan_test` 测试维护

## 工作流

1. 描述 `goal`（业务目标/现状）。
2. 选 `action`；指定或留空 `platform`（any 让方案推荐）。
3. 补充 `constraints`（预算、合规、已有工具）。

## 常见陷阱

- 不要脱离约束推荐重型平台；先评估 ROI 再设计。
- 跨系统数据流注意鉴权与合规边界。

## 输出

- 自动化方案：机会清单 / 工作流设计 / 选型建议 / 测试维护计划。
