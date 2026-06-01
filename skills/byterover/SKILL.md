---
name: byterover
description: "智能知识管理（ByteRover）：用 brv 存储/检索项目模式、决策与上下文，任务前先收集上下文，跨工具复用。当需要保存或调取项目知识时触发。"
when_to_use: "任务开始前收集已有上下文，或想沉淀项目决策/模式时"
argument-hint: "[action] (可选 key/content/query/category)"
version: "1.0.0"
---

# 智能知识管理（ByteRover）

为智能体提供跨会话、跨工具的项目知识库。

## 何时使用

- 任务前检索相关上下文与历史决策
- 存储项目模式、决策与经验
- 按类别组织与查找知识

## 能力

- `store` · `retrieve` · `search` · `list` · `delete`

## 工作流

1. 开始任务前先 `retrieve`/`search` 收集上下文。
2. `store` 带 `key`+`content`，归入 `category`。

## 常见陷阱

- 不先检索就动手易重复踩坑；store 的 key 要稳定可复查。
- delete 不可逆。

## 输出

- 命中的知识条目或存储结果。
