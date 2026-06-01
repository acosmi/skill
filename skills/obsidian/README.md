# Obsidian 笔记

操作 Obsidian 知识库（纯 Markdown 笔记），支持通过 obsidian-cli 进行笔记的创建、搜索、链接和自动化管理。

## 概述

**Obsidian 笔记** 是一个效率工具领域的执行动作类技能。支持 8 种操作模式：搜索, 创建, 读取, 更新, 删除, link。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **search** — 搜索
- **create** — 创建
- **read** — 读取
- **update** — 更新
- **delete** — 删除
- **link** — link
- **list_tags** — 列出tags
- **backlinks** — backlinks

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 笔记操作类型 可选值: `search, create, read, update, delete, link, list_tags, backlinks` |
| `vault` | string | 否 | 知识库路径 |
| `title` | string | 否 | 笔记标题 |
| `content` | string | 否 | 笔记内容（Markdown 格式） |
| `query` | string | 否 | 搜索关键词 |
| `tags` | array | 否 | 笔记标签 |
| `link_to` | string | 否 | 链接目标笔记标题（link 操作时使用） |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `notes` | array | 笔记列表 |
| `content` | string | 单篇笔记内容 |
| `backlinks` | array | - |

## 使用示例

### 示例 1: 搜索

```json
{
  "action": "search",
  "vault": "示例值",
  "title": "示例title",
  "content": "示例笔记内容（Markdown 格式）",
  "query": "Obsidian 笔记相关查询",
  "tags": [
    "item1",
    "item2"
  ],
  "link_to": "示例值"
}
```

### 示例 2: 创建

```json
{
  "action": "create",
  "title": "示例title",
  "content": "示例笔记内容（Markdown 格式）",
  "query": "Obsidian 笔记相关查询",
  "tags": [
    "item1",
    "item2"
  ]
}
```

### 示例 3: 读取

```json
{
  "action": "read",
  "title": "示例title",
  "content": "示例笔记内容（Markdown 格式）",
  "query": "Obsidian 笔记相关查询",
  "tags": [
    "item1",
    "item2"
  ]
}
```

### 示例 4: 更新

```json
{
  "action": "update",
  "title": "示例title",
  "content": "示例笔记内容（Markdown 格式）",
  "query": "Obsidian 笔记相关查询",
  "tags": [
    "item1",
    "item2"
  ]
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `obsidian`
- 分类: 执行动作类 / 效率工具
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
