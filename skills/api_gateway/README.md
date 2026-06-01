# API 网关（100+ 服务）

通过托管 OAuth 连接 100+ 个主流 API，涵盖 Google Workspace、Microsoft 365、GitHub、Notion、Slack、Airtable、HubSpot 等，一个技能接入所有服务。

## 概述

**API 网关（100+ 服务）** 是一个编程开发领域的执行动作类技能。支持 8 种操作模式：列出, 获取, 创建, 更新, 删除, 搜索。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **list** — 列出
- **get** — 获取
- **create** — 创建
- **update** — 更新
- **delete** — 删除
- **search** — 搜索
- **send** — 发送
- **webhook** — webhook

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | API 操作 可选值: `list, get, create, update, delete, search, send, webhook` |
| `resource` | string | 否 | 资源类型 |
| `id` | string | 否 | 资源 ID |
| `data` | object | 否 | 请求数据 |
| `query` | string | 否 | 搜索/过滤条件 |
| `params` | object | 否 | 附加参数 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `data` | object | API 返回数据 |
| `service` | string | - |
| `action` | string | - |
| `rate_limit` | object | - |

## 使用示例

### 示例 1: 列出

```json
{
  "action": "list",
  "resource": "示例值",
  "id": "item-001",
  "query": "API 网关（100+ 服务）相关查询"
}
```

### 示例 2: 获取

```json
{
  "action": "get",
  "id": "item-001",
  "query": "API 网关（100+ 服务）相关查询"
}
```

### 示例 3: 创建

```json
{
  "action": "create",
  "id": "item-001",
  "query": "API 网关（100+ 服务）相关查询"
}
```

### 示例 4: 更新

```json
{
  "action": "update",
  "id": "item-001",
  "query": "API 网关（100+ 服务）相关查询"
}
```

## 适用场景

- 日常编程开发中需要代码生成、审查或调试时
- 项目重构或代码质量优化时
- 学习新编程语言或框架时的辅助工具

## 注意事项

- 技能标识: `api_gateway`
- 分类: 执行动作类 / 编程开发
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
