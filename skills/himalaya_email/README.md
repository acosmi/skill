# Himalaya 邮件 CLI

通过 IMAP/SMTP 协议管理邮件的命令行工具，支持列出、读取、撰写、回复、转发、搜索和整理邮件，支持多账号和 MIME 附件。

## 概述

**Himalaya 邮件 CLI** 是一个调研分析领域的执行动作类技能。支持 8 种操作模式：列出, 读取, 撰写, 回复, 转发, 搜索。通过 7 个可配置参数实现灵活控制。

## 功能特性

- **list** — 列出
- **read** — 读取
- **compose** — 撰写
- **reply** — 回复
- **forward** — 转发
- **search** — 搜索
- **move** — move
- **flag** — flag

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 邮件操作 可选值: `list, read, compose, reply, forward, search, move, flag` |
| `account` | string | 否 | 邮件账号标识 |
| `folder` | string | 否 | 邮箱文件夹（INBOX/Sent/Drafts 等） |
| `id` | string | 否 | 邮件 ID |
| `to` | string | 否 | - |
| `subject` | string | 否 | - |
| `body` | string | 否 | - |
| `query` | string | 否 | 搜索关键词 |

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
  "account": "示例值",
  "folder": "示例值",
  "id": "item-001",
  "to": "示例值",
  "subject": "示例值",
  "body": "示例值",
  "query": "Himalaya 邮件 CLI相关查询"
}
```

### 示例 2: 读取

```json
{
  "action": "read",
  "id": "item-001",
  "query": "Himalaya 邮件 CLI相关查询"
}
```

### 示例 3: 撰写

```json
{
  "action": "compose",
  "id": "item-001",
  "query": "Himalaya 邮件 CLI相关查询"
}
```

### 示例 4: 回复

```json
{
  "action": "reply",
  "id": "item-001",
  "query": "Himalaya 邮件 CLI相关查询"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `himalaya_email`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
