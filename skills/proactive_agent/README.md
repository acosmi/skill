# 主动型智能体

将 AI 从被动任务执行者转变为能预判需求、持续改进的主动伙伴。支持 WAL 协议、工作缓冲区和自主定时任务，实现真正的主动式 AI 协作。

## 概述

**主动型智能体** 是一个自动化领域的执行动作类技能。支持 4 种操作模式：anticipate, 定时任务, 工作缓冲, 自主反思。通过 4 个可配置参数实现灵活控制。

## 功能特性

- **anticipate** — anticipate
- **schedule** — 定时任务
- **buffer** — 工作缓冲
- **reflect** — 自主反思

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `mode` | string | 是 | 主动模式：anticipate=需求预判, schedule=定时任务, buffer=工作缓冲, reflect=自主反思 可选值: `anticipate, schedule, buffer, reflect` |
| `task` | string | 否 | 任务描述或定时任务内容 |
| `schedule` | string | 否 | cron 表达式或时间间隔（schedule 模式时使用） |
| `context` | string | 否 | 当前上下文信息，用于需求预判 |
| `priority` | string | 否 | 任务优先级 可选值: `low`, `medium`, `high`, `urgent` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `action_taken` | string | 已执行的主动行为 |
| `scheduled` | boolean | 是否已安排定时任务 |
| `anticipations` | array | 预判的用户需求列表 |
| `next_check` | string | 下次主动检查时间 |

## 使用示例

### 示例 1: anticipate

```json
{
  "action": "anticipate",
  "task": "示例值",
  "schedule": "示例值",
  "context": "示例当前上下文信息，用于需求预判",
  "priority": "low"
}
```

### 示例 2: 定时任务

```json
{
  "action": "schedule",
  "context": "示例当前上下文信息，用于需求预判",
  "priority": "low"
}
```

### 示例 3: 工作缓冲

```json
{
  "action": "buffer",
  "context": "示例当前上下文信息，用于需求预判",
  "priority": "low"
}
```

### 示例 4: 自主反思

```json
{
  "action": "reflect",
  "context": "示例当前上下文信息，用于需求预判",
  "priority": "low"
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `proactive_agent`
- 分类: 执行动作类 / 自动化
- 必填参数: `mode`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
