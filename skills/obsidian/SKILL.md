---
name: obsidian
description: "Obsidian 笔记：通过 obsidian-cli 操作 Markdown 知识库——创建/读/改/删、搜索、双链、标签、反链。当需要管理 Obsidian 笔记时触发。"
when_to_use: "需要在 Obsidian 知识库中读写笔记、建立链接或检索时"
argument-hint: "[action] (可选 vault/title/content/query/tags)"
version: "1.0.0"
---

# Obsidian 笔记

操作纯 Markdown 的 Obsidian 知识库，支持双链与标签。

## 何时使用

- 创建、读取、更新、删除笔记
- 搜索笔记、列标签、查反链
- 在笔记间建立双向链接

## 能力

- `search` · `create` · `read` · `update` · `delete` · `link` · `list_tags` · `backlinks`

## 工作流

1. 选 `action`，多库时指定 `vault`。
2. 写入带 `title`+`content`；`link` 带 `link_to`；搜索带 `query`/`tags`。

## 常见陷阱

- delete 不可逆，删除前确认 title 命中唯一笔记。
- link_to 目标不存在会产生空链。

## 输出

- 操作结果、笔记内容、搜索命中或标签/反链列表。
