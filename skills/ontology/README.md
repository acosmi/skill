# 知识图谱记忆

用于结构化智能体记忆和可组合技能的类型化知识图谱，支持创建/查询实体（人员、项目、任务、事件、文档），支持实体关联和图遍历。

## 概述

**知识图谱记忆** 是一个效率工具领域的执行动作类技能。支持 6 种操作模式：创建entity, 查询, link, traverse, 更新, 删除。通过 7 个可配置参数实现灵活控制。

## 功能特性

- **create_entity** — 创建entity
- **query** — 查询
- **link** — link
- **traverse** — traverse
- **update** — 更新
- **delete** — 删除

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 知识图谱操作类型 可选值: `create_entity, query, link, traverse, update, delete` |
| `entity_type` | string | 否 | 实体类型 可选值: `person`, `project`, `task`, `event`, `document`, `concept` |
| `name` | string | 否 | 实体名称 |
| `properties` | object | 否 | 实体属性键值对 |
| `relation` | string | 否 | 关系类型（link 操作时使用） |
| `target` | string | 否 | 目标实体名称（link 操作时使用） |
| `query` | string | 否 | 查询表达式或自然语言描述 |
| `depth` | integer | 否 | 图遍历深度（traverse 时使用），默认 2 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `entities` | array | 查询结果实体列表 |
| `relations` | array | 关系列表 |
| `message` | string | - |

## 使用示例

### 示例 1: 创建entity

```json
{
  "action": "create_entity",
  "entity_type": "person",
  "name": "示例name",
  "relation": "示例值",
  "target": "示例值",
  "query": "知识图谱记忆相关查询",
  "depth": 10
}
```

### 示例 2: 查询

```json
{
  "action": "query",
  "entity_type": "person",
  "name": "示例name",
  "query": "知识图谱记忆相关查询",
  "depth": 10
}
```

### 示例 3: link

```json
{
  "action": "link",
  "entity_type": "person",
  "name": "示例name",
  "query": "知识图谱记忆相关查询",
  "depth": 10
}
```

### 示例 4: traverse

```json
{
  "action": "traverse",
  "entity_type": "person",
  "name": "示例name",
  "query": "知识图谱记忆相关查询",
  "depth": 10
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `ontology`
- 分类: 执行动作类 / 效率工具
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
