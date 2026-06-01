---
name: notion
description: "Notion：通过 API 创建/更新/搜索页面、查询/创建数据库、管理内容块。当需要操作 Notion 页面或数据库时触发。"
when_to_use: "需要在 Notion 中读写页面、数据库或内容块时"
argument-hint: "[action] (按操作带 page_id/database_id/title/content)"
version: "1.0.0"
---

# Notion

通过 Notion API 实现全面的工作区自动化。

## 何时使用

- 搜索、读取、创建、更新 Notion 页面
- 查询与创建数据库、追加内容块

## 能力

- `search` · `get_page` · `create_page` · `update_page` · `query_database` · `create_database` 等

## 工作流

1. 选 `action`。
2. 创建页面带 `parent_id`+`title`+`content`；更新带 `page_id`。
3. 数据库操作带 `database_id` 与 `filter`。

## 常见陷阱

- create_page 必须有合法 parent_id（数据库或页面）。
- update 前确认 page_id，避免改错页面。

## 输出

- 操作结果、页面/数据库对象或查询命中列表。
