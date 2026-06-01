---
name: self-improving
description: "主动自进化智能体：自我反思/批评/学习/记忆组织与召回，桌面智能体核心 meta 技能。当需要复盘、自我改进或沉淀经验时触发。"
when_to_use: "需要复盘任务、批判性自检、沉淀或召回经验时"
argument-hint: "[action] [content]"
version: "1.0.0"
---

# 主动自进化智能体

通过反思—批评—学习—召回闭环实现智能体持续自我改进。

## 何时使用

- 任务结束后复盘得失（reflect）
- 对自身产出做批判性审视（critique）
- 把经验沉淀为可复用知识（learn/organize）
- 任务开始前召回相关经验（recall）

## 能力

- `reflect` 反思 · `critique` 自我批评 · `learn` 学习沉淀 · `organize` 记忆组织 · `recall` 召回

## 工作流

1. 选 `action` 并提供 `content`（反思/批评/学习的内容）。
2. learn/organize 时归入 `category`，recall 时用 `query` 检索。
3. 可带 `task_result` 作为复盘依据。

## 常见陷阱

- recall 前确保已有 learn 沉淀，否则召回为空。
- critique 要给出可执行改进项，而非泛泛而谈。

## 输出

- 反思/批评结论、沉淀的知识条目或召回结果。
