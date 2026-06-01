---
name: evolver
description: "Evolver 能力进化器：自主智能体自我改进的元技能，分析/提案/进化/回滚/查历史。当需要让智能体自主优化自身能力时触发。"
when_to_use: "需要让智能体分析并自主优化自身能力时"
argument-hint: "[action] (可选 target/proposal)"
version: "1.0.0"
---

# Evolver 能力进化器

一个为自主智能体设计的能力自我进化元技能。

## 何时使用

- 分析当前能力与短板
- 提出可执行的改进方案
- 执行进化、必要时回滚、查看历史

## 能力

- `analyze` · `propose` · `evolve` · `rollback` · `history`

## 工作流

1. 先 `analyze` 定位 `target`，再 `propose` 方案。
2. `evolve` 落地改进；出问题用 `rollback`，`history` 看演进。

## 常见陷阱

- evolve 改动自身行为，先 propose 评审再执行。
- 重大进化前确认可 rollback。

## 输出

- 分析结论、改进方案、进化结果或历史记录。
