# Notion 工作区
> Notion

Notion — 通过 Notion API 创建和管理页面、数据库和内容块，支持全面的 Notion 工作区自动化操作。

## 概述

**Notion 工作区** 是一个自动化领域的执行动作类技能。支持 8 种操作模式：搜索, 获取page, 创建page, 更新page, 查询database, 创建database。通过 7 个可配置参数实现灵活控制。

## 功能特性

- **search** — 搜索
- **get_page** — 获取page
- **create_page** — 创建page
- **update_page** — 更新page
- **query_database** — 查询database
- **create_database** — 创建database
- **add_block** — 添加block
- **get_blocks** — 获取blocks

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | Notion 操作类型 可选值: `search, get_page, create_page, update_page, query_database, create_database, add_block, get_blocks` |
| `query` | string | 否 | 搜索关键词（search 时使用） |
| `page_id` | string | 否 | 页面 ID |
| `database_id` | string | 否 | 数据库 ID |
| `parent_id` | string | 否 | 父页面/数据库 ID（创建时使用） |
| `title` | string | 否 | 页面标题 |
| `content` | string | 否 | 页面内容（Markdown 格式） |
| `filter` | object | 否 | 数据库查询过滤条件 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `data` | object | 页面/数据库/块的详细数据 |
| `results` | array | 搜索或查询结果列表 |
| `page_url` | string | 创建的页面 URL |

## 使用示例

### 示例 1: 搜索

```json
{
  "action": "search",
  "query": "Notion 工作区相关查询",
  "page_id": "item-001",
  "database_id": "item-001",
  "parent_id": "item-001",
  "title": "示例title",
  "content": "示例页面内容（Markdown 格式）"
}
```

### 示例 2: 获取page

```json
{
  "action": "get_page",
  "query": "Notion 工作区相关查询",
  "page_id": "item-001",
  "database_id": "item-001",
  "parent_id": "item-001",
  "title": "示例title",
  "content": "示例页面内容（Markdown 格式）"
}
```

### 示例 3: 创建page

```json
{
  "action": "create_page",
  "query": "Notion 工作区相关查询",
  "page_id": "item-001",
  "database_id": "item-001",
  "parent_id": "item-001",
  "title": "示例title",
  "content": "示例页面内容（Markdown 格式）"
}
```

### 示例 4: 更新page

```json
{
  "action": "update_page",
  "query": "Notion 工作区相关查询",
  "page_id": "item-001",
  "database_id": "item-001",
  "parent_id": "item-001",
  "title": "示例title",
  "content": "示例页面内容（Markdown 格式）"
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `notion`
- 分类: 执行动作类 / 自动化
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
