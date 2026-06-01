# Trello 看板

Trello 看板 — 通过 Trello REST API 管理看板、列表、卡片、成员和标签，实现项目任务的完整生命周期管理。

## 概述

**Trello 看板** 是一个API集成领域的执行动作类技能。支持 8 种操作模式：列出boards, 列出cards, 创建card, movecard, 添加member, 添加评论。通过 7 个可配置参数实现灵活控制。

## 功能特性

- **list_boards** — 列出boards
- **list_cards** — 列出cards
- **create_card** — 创建card
- **move_card** — movecard
- **add_member** — 添加member
- **add_comment** — 添加评论
- **add_label** — 添加label
- **archive** — 归档

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | Trello 操作 可选值: `list_boards, list_cards, create_card, move_card, add_member, add_comment, add_label, archive` |
| `board_id` | string | 否 | 看板 ID |
| `list_id` | string | 否 | 列表 ID |
| `card_id` | string | 否 | 卡片 ID |
| `name` | string | 否 | 名称（创建时使用） |
| `description` | string | 否 | - |
| `member` | string | 否 | 成员 ID |
| `label` | string | 否 | 标签颜色 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 列出boards

```json
{
  "action": "list_boards",
  "board_id": "item-001",
  "list_id": "item-001",
  "card_id": "item-001",
  "name": "示例name",
  "description": "示例值",
  "member": "示例值",
  "label": "示例值"
}
```

### 示例 2: 列出cards

```json
{
  "action": "list_cards",
  "board_id": "item-001",
  "list_id": "item-001",
  "card_id": "item-001",
  "name": "示例name"
}
```

### 示例 3: 创建card

```json
{
  "action": "create_card",
  "board_id": "item-001",
  "list_id": "item-001",
  "card_id": "item-001",
  "name": "示例name"
}
```

### 示例 4: movecard

```json
{
  "action": "move_card",
  "board_id": "item-001",
  "list_id": "item-001",
  "card_id": "item-001",
  "name": "示例name"
}
```

## 适用场景

- 第三方服务集成或 API 对接时
- 数据同步或跨平台操作时
- 服务编排或接口调试时

## 注意事项

- 技能标识: `trello`
- 分类: 执行动作类 / API集成
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
