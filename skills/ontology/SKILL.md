---
name: ontology
description: "知识图谱记忆：创建/查询/关联/遍历/更新/删除类型化实体（人/项目/任务/事件/文档/概念），用于结构化智能体长期记忆。当需要结构化存取关系记忆时触发。"
when_to_use: "需要把人/项目/任务等实体及其关系结构化存储与检索时"
argument-hint: "[action] (create 需 entity_type+name，link 需 relation+target)"
version: "1.0.0"
---

# 知识图谱记忆

类型化知识图谱，为智能体提供可组合的结构化记忆。

## 何时使用

- 记录实体（人员、项目、任务、事件、文档、概念）及属性
- 建立实体间关系并按图遍历检索上下文

## 能力（action）

- `create_entity` 创建实体 · `query` 查询 · `link` 建立关系
- `traverse` 图遍历 · `update` 更新 · `delete` 删除

## 工作流

1. `create_entity`：指定 `entity_type` + `name`，可带 `properties`。
2. `link`：用 `relation` 把当前实体连到 `target`。
3. `query`/`traverse`：用 `query` 表达式或自然语言检索，`depth` 控制遍历深度（默认 2）。

## 常见陷阱

- link/traverse 前确保两端实体已存在，否则关系悬空。
- depth 过大易返回噪声，按需限制遍历层数。

## 输出

- `success`、`entities` 实体列表、`relations` 关系列表、`message`。
