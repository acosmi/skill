# Google Workspace 套件

Google Workspace 全套 CLI，涵盖 Gmail、日历、云端硬盘、联系人、表格和文档，一个工具搞定所有 Google 服务。

## 概述

**Google Workspace 套件** 是一个调研分析领域的执行动作类技能。支持 7 种操作模式：列出, 获取, 创建, 更新, 删除, 搜索。通过 4 个可配置参数实现灵活控制。

## 功能特性

- **list** — 列出
- **get** — 获取
- **create** — 创建
- **update** — 更新
- **delete** — 删除
- **search** — 搜索
- **send** — 发送

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 操作类型 可选值: `list, get, create, update, delete, search, send` |
| `service` | string | 是 | Google 服务类型 可选值: `gmail`, `calendar`, `drive`, `contacts`, `sheets`, `docs` |
| `query` | string | 否 | 搜索关键词或过滤条件 |
| `id` | string | 否 | 资源 ID（get/update/delete 时使用） |
| `data` | object | 否 | 创建或更新的数据内容 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回的数据内容 |
| `count` | integer | 结果数量（列表操作时） |
| `message` | string | 操作结果描述 |

## 使用示例

### 示例 1: 列出

```json
{
  "action": "list",
  "service": "gmail",
  "query": "Google Workspace 套件相关查询",
  "id": "item-001"
}
```

### 示例 2: 获取

```json
{
  "action": "get",
  "service": "gmail",
  "query": "Google Workspace 套件相关查询",
  "id": "item-001"
}
```

### 示例 3: 创建

```json
{
  "action": "create",
  "service": "gmail",
  "query": "Google Workspace 套件相关查询",
  "id": "item-001"
}
```

### 示例 4: 更新

```json
{
  "action": "update",
  "service": "gmail",
  "query": "Google Workspace 套件相关查询",
  "id": "item-001"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `gog`
- 分类: 执行动作类 / 调研分析
- 必填参数: `service`, `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
