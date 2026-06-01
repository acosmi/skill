# Outlook 邮件日历
> Outlook & Microsoft Graph

通过 Microsoft Graph 连接 Outlook，使用预提供的访问令牌管理邮件、日历、联系人和文件夹操作，适合企业用户。

## 概述

**Outlook 邮件日历** 是一个API集成领域的执行动作类技能。支持 7 种操作模式：列出mail, 读取mail, 发送mail, 列出events, 创建event, 列出contacts。通过 7 个可配置参数实现灵活控制。

## 功能特性

- **list_mail** — 列出mail
- **read_mail** — 读取mail
- **send_mail** — 发送mail
- **list_events** — 列出events
- **create_event** — 创建event
- **list_contacts** — 列出contacts
- **list_folders** — 列出folders

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 操作类型 可选值: `list_mail, read_mail, send_mail, list_events, create_event, list_contacts, list_folders` |
| `query` | string | 否 | 搜索或过滤条件 |
| `id` | string | 否 | 邮件/事件 ID |
| `to` | string | 否 | 收件人 |
| `subject` | string | 否 | - |
| `body` | string | 否 | - |
| `start` | string | 否 | 事件开始时间 ISO 格式 |
| `end` | string | 否 | 事件结束时间 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 列出mail

```json
{
  "action": "list_mail",
  "query": "Outlook 邮件日历相关查询",
  "id": "item-001",
  "to": "示例值",
  "subject": "示例值",
  "body": "示例值",
  "start": "示例值",
  "end": "示例值"
}
```

### 示例 2: 读取mail

```json
{
  "action": "read_mail",
  "query": "Outlook 邮件日历相关查询",
  "id": "item-001"
}
```

### 示例 3: 发送mail

```json
{
  "action": "send_mail",
  "query": "Outlook 邮件日历相关查询",
  "id": "item-001"
}
```

### 示例 4: 列出events

```json
{
  "action": "list_events",
  "query": "Outlook 邮件日历相关查询",
  "id": "item-001"
}
```

## 适用场景

- 第三方服务集成或 API 对接时
- 数据同步或跨平台操作时
- 服务编排或接口调试时

## 注意事项

- 技能标识: `outlook_graph`
- 分类: 执行动作类 / API集成
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
