# Gmail 邮件管理
> Gmail

通过托管 OAuth 集成 Gmail API，完整支持读取、发送和管理邮件、会话线程、标签和草稿，实现 Gmail 自动化操作。

## 概述

**Gmail 邮件管理** 是一个自动化领域的执行动作类技能。支持 9 种操作模式：列出, 读取, 发送, 回复, 转发, 搜索。通过 8 个可配置参数实现灵活控制。

## 功能特性

- **list** — 列出
- **read** — 读取
- **send** — 发送
- **reply** — 回复
- **forward** — 转发
- **search** — 搜索
- **label** — label
- **draft** — draft
- **trash** — trash

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | Gmail 操作 可选值: `list, read, send, reply, forward, search, label, draft, trash` |
| `query` | string | 否 | 搜索条件（Gmail 搜索语法） |
| `id` | string | 否 | 邮件 ID |
| `to` | string | 否 | 收件人 |
| `cc` | string | 否 | 抄送 |
| `subject` | string | 否 | 邮件主题 |
| `body` | string | 否 | 邮件正文（HTML 或纯文本） |
| `label` | string | 否 | 标签名 |
| `max_results` | integer | 否 | 列表最大数量，默认 20 |

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
  "query": "Gmail 邮件管理相关查询",
  "id": "item-001",
  "to": "示例值",
  "cc": "示例值",
  "subject": "示例值",
  "body": "示例值",
  "label": "示例值",
  "max_results": 10
}
```

### 示例 2: 读取

```json
{
  "action": "read",
  "query": "Gmail 邮件管理相关查询",
  "id": "item-001",
  "max_results": 10
}
```

### 示例 3: 发送

```json
{
  "action": "send",
  "query": "Gmail 邮件管理相关查询",
  "id": "item-001",
  "max_results": 10
}
```

### 示例 4: 回复

```json
{
  "action": "reply",
  "query": "Gmail 邮件管理相关查询",
  "id": "item-001",
  "max_results": 10
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `gmail`
- 分类: 执行动作类 / 自动化
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
