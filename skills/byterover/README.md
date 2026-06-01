# 智能知识管理（ByteRover）

AI 智能体的知识管理系统，使用 brv 命令存储和检索项目模式、决策和上下文，在任务开始前必须使用此工具收集上下文。

## 概述

**智能知识管理（ByteRover）** 是一个调研分析领域的执行动作类技能。支持 5 种操作模式：存储, 检索, 搜索, 列出, 删除。通过 4 个可配置参数实现灵活控制。

## 功能特性

- **store** — 存储
- **retrieve** — 检索
- **search** — 搜索
- **list** — 列出
- **delete** — 删除

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 知识管理操作 可选值: `store, retrieve, search, list, delete` |
| `key` | string | 否 | 知识条目键名 |
| `content` | string | 否 | 知识内容（store 时使用） |
| `query` | string | 否 | 搜索查询（search 时使用） |
| `category` | string | 否 | 知识分类（pattern/decision/context） |

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
  "key": "示例值",
  "content": "示例知识内容（store 时使用）",
  "query": "智能知识管理（ByteRover）相关查询",
  "category": "示例值"
}
```

### 示例 2: 检索

```json
{
  "action": "retrieve",
  "content": "示例知识内容（store 时使用）",
  "query": "智能知识管理（ByteRover）相关查询"
}
```

### 示例 3: 搜索

```json
{
  "action": "search",
  "content": "示例知识内容（store 时使用）",
  "query": "智能知识管理（ByteRover）相关查询"
}
```

### 示例 4: 列出

```json
{
  "action": "list",
  "content": "示例知识内容（store 时使用）",
  "query": "智能知识管理（ByteRover）相关查询"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `byterover`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
