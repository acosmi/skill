# Sonos 音响控制

Sonos 音响控制 — 控制 Sonos 智能音响系统，支持设备发现、状态查询、播放控制、音量调节和多房间分组，打造智能家居音频体验。

## 概述

**Sonos 音响控制** 是一个多媒体处理领域的执行动作类技能。支持 11 种操作模式：discover, 状态查询, 播放, 暂停, 停止, next。通过 3 个可配置参数实现灵活控制。

## 功能特性

- **discover** — discover
- **status** — 状态查询
- **play** — 播放
- **pause** — 暂停
- **stop** — 停止
- **next** — next
- **previous** — previous
- **volume** — volume
- **group** — 分组
- **ungroup** — ungroup
- **favorite** — favorite

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 音响控制操作 可选值: `discover, status, play, pause, stop, next, previous, volume, group, ungroup, favorite` |
| `speaker` | string | 否 | 音响设备名称或 ID |
| `value` | string | 否 | 操作参数（音量值 0-100、播放 URI 等） |
| `group_members` | array | 否 | 分组成员列表（group 操作时使用） |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `speakers` | array | 发现的音响列表 |
| `status` | object | 当前播放状态 |
| `message` | string | - |

## 使用示例

### 示例 1: discover

```json
{
  "action": "discover",
  "speaker": "示例值",
  "value": "示例值",
  "group_members": [
    "item1",
    "item2"
  ]
}
```

### 示例 2: 状态查询

```json
{
  "action": "status",
  "group_members": [
    "item1",
    "item2"
  ]
}
```

### 示例 3: 播放

```json
{
  "action": "play",
  "group_members": [
    "item1",
    "item2"
  ]
}
```

### 示例 4: 暂停

```json
{
  "action": "pause",
  "group_members": [
    "item1",
    "item2"
  ]
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `sonoscli`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
