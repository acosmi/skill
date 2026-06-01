---
name: trello
description: "Trello 看板：经 REST API 管理看板/列表/卡片/成员/标签，覆盖任务完整生命周期。当需要管理 Trello 看板或卡片时触发。"
when_to_use: "需要在 Trello 创建/移动卡片、管理看板任务时"
argument-hint: "[action] (可选 board_id/list_id/card_id/name)"
version: "1.0.0"
---

# Trello 看板

用 Trello API 管理项目任务全生命周期。

## 何时使用

- 列出看板与卡片
- 创建、移动卡片
- 管理成员与标签

## 能力

- `list_boards` · `list_cards` · `create_card` · `move_card` · `add_member` 等

## 工作流

1. 选 `action`，按需带 `board_id`/`list_id`/`card_id`。
2. 创建卡片带 `name`/`description`。

## 常见陷阱

- move_card 需正确的目标 list_id。
- create 前确认目标看板/列表存在。

## 输出

- 看板/卡片列表或操作结果。
