# 技能自动更新

技能自动更新 — 通过定时任务每日自动检查并更新所有已安装的技能，运行完成后向用户发送更新摘要，保持技能库始终最新。

## 概述

**技能自动更新** 是一个自动化领域的执行动作类技能。支持 5 种操作模式：检查, 全部更新, 更新单个, 设置定时, 查看状态。通过 3 个可配置参数实现灵活控制。

## 功能特性

- **check** — 检查
- **update_all** — 全部更新
- **update_one** — 更新单个
- **schedule** — 设置定时
- **status** — 查看状态

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 操作类型：check=检查更新, update_all=全部更新, update_one=更新单个, schedule=设置定时, status=查看状态 可选值: `check, update_all, update_one, schedule, status` |
| `skill_key` | string | 否 | 指定技能 key（update_one 时使用） |
| `cron` | string | 否 | 定时任务 cron 表达式（schedule 时使用），默认每天 3:00 |
| `notify` | boolean | 否 | 更新后是否发送通知，默认 true |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `updated` | array | 已更新的技能列表 |
| `skipped` | integer | - |
| `failed` | integer | - |
| `next_check` | string | 下次检查时间 |

## 使用示例

### 示例 1: 检查

```json
{
  "action": "check",
  "skill_key": "示例值",
  "cron": "示例值",
  "notify": true
}
```

### 示例 2: 全部更新

```json
{
  "action": "update_all",
  "notify": true
}
```

### 示例 3: 更新单个

```json
{
  "action": "update_one",
  "notify": true
}
```

### 示例 4: 设置定时

```json
{
  "action": "schedule",
  "notify": true
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `auto_updater`
- 分类: 执行动作类 / 自动化
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
