# Slack 集成
> Slack

通过工具控制 Slack，支持发送消息、添加表情回应、置顶/取消置顶消息，适用于频道和私信场景的完整 Slack 自动化。

## 概述

**Slack 集成** 是一个自动化领域的执行动作类技能。支持 7 种操作模式：发送, react, pin, unpin, 列出channels, history。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **send** — 发送
- **react** — react
- **pin** — pin
- **unpin** — unpin
- **list_channels** — 列出channels
- **history** — history
- **upload** — 上传

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | Slack 操作 可选值: `send, react, pin, unpin, list_channels, history, upload` |
| `channel` | string | 否 | 频道名或 ID |
| `message` | string | 否 | 消息内容 |
| `emoji` | string | 否 | 表情符号名称（react 时使用） |
| `thread_ts` | string | 否 | 线程时间戳（回复消息时使用） |
| `file` | string | 否 | 上传文件路径 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 发送

```json
{
  "action": "send",
  "channel": "示例值",
  "message": "示例消息内容",
  "emoji": "示例值",
  "thread_ts": "示例值",
  "file": "/path/to/file.txt"
}
```

### 示例 2: react

```json
{
  "action": "react",
  "message": "示例消息内容",
  "file": "/path/to/file.txt"
}
```

### 示例 3: pin

```json
{
  "action": "pin",
  "message": "示例消息内容",
  "file": "/path/to/file.txt"
}
```

### 示例 4: unpin

```json
{
  "action": "unpin",
  "message": "示例消息内容",
  "file": "/path/to/file.txt"
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `slack`
- 分类: 执行动作类 / 自动化
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
