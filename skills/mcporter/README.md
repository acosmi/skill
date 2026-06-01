# MCP 服务器管理

使用 mcporter CLI 列出、配置、授权和调用 MCP 服务器及工具，支持 HTTP 和 stdio 模式，以及即时服务器、配置编辑和类型生成。

## 概述

**MCP 服务器管理** 是一个API集成领域的执行动作类技能。支持 6 种操作模式：列出, 添加, 移除, authorize, call, 状态查询。通过 4 个可配置参数实现灵活控制。

## 功能特性

- **list** — 列出
- **add** — 添加
- **remove** — 移除
- **authorize** — authorize
- **call** — call
- **status** — 状态查询

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | MCP 操作 可选值: `list, add, remove, authorize, call, status` |
| `server` | string | 否 | MCP 服务器名称或 URL |
| `tool` | string | 否 | 工具名称（call 时使用） |
| `params` | object | 否 | 工具调用参数 |
| `mode` | string | 否 | 连接模式 可选值: `http`, `stdio` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 列出

```json
{
  "action": "list",
  "server": "示例值",
  "tool": "示例值"
}
```

### 示例 2: 添加

```json
{
  "action": "add"
}
```

### 示例 3: 移除

```json
{
  "action": "remove"
}
```

### 示例 4: authorize

```json
{
  "action": "authorize"
}
```

## 适用场景

- 第三方服务集成或 API 对接时
- 数据同步或跨平台操作时
- 服务编排或接口调试时

## 注意事项

- 技能标识: `mcporter`
- 分类: 执行动作类 / API集成
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
