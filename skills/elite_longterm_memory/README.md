# 精英长期记忆系统

AI 智能体终极记忆系统，集成 WAL 协议、向量搜索、git-notes 和云备份，适用于 Cursor、Claude、ChatGPT 和 Copilot，永不丢失上下文。

## 概述

**精英长期记忆系统** 是一个效率工具领域的执行动作类技能。支持 6 种操作模式：存储, 经验回忆, 搜索, 同步, 备份, prune。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **store** — 存储
- **recall** — 经验回忆
- **search** — 搜索
- **sync** — 同步
- **backup** — 备份
- **prune** — prune

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 记忆操作 可选值: `store, recall, search, sync, backup, prune` |
| `content` | string | 否 | 记忆内容 |
| `query` | string | 否 | 语义搜索查询 |
| `tags` | array | 否 | 标签 |
| `importance` | string | 否 | 重要程度 可选值: `low`, `medium`, `high`, `critical` |
| `ttl` | string | 否 | 记忆有效期（如 7d/30d/permanent） |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 存储

```json
{
  "action": "store",
  "content": "示例记忆内容",
  "query": "精英长期记忆系统相关查询",
  "tags": [
    "item1",
    "item2"
  ],
  "importance": "low",
  "ttl": "示例值"
}
```

### 示例 2: 经验回忆

```json
{
  "action": "recall",
  "content": "示例记忆内容",
  "query": "精英长期记忆系统相关查询",
  "tags": [
    "item1",
    "item2"
  ],
  "importance": "low"
}
```

### 示例 3: 搜索

```json
{
  "action": "search",
  "content": "示例记忆内容",
  "query": "精英长期记忆系统相关查询",
  "tags": [
    "item1",
    "item2"
  ],
  "importance": "low"
}
```

### 示例 4: 同步

```json
{
  "action": "sync",
  "content": "示例记忆内容",
  "query": "精英长期记忆系统相关查询",
  "tags": [
    "item1",
    "item2"
  ],
  "importance": "low"
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `elite_longterm_memory`
- 分类: 执行动作类 / 效率工具
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
