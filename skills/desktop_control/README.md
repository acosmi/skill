# 桌面自动化控制

高级桌面自动化，支持鼠标控制、键盘输入、热键、屏幕捕获、图像匹配和窗口管理，内置安全保护（故障安全中止、边界检查）。

## 概述

**桌面自动化控制** 是一个多媒体处理领域的执行动作类技能。支持 10 种操作模式：click, type, hotkey, screenshot, 查找image, movemouse。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **click** — click
- **type** — type
- **hotkey** — hotkey
- **screenshot** — screenshot
- **find_image** — 查找image
- **move_mouse** — movemouse
- **scroll** — scroll
- **window_list** — window列出
- **window_focus** — windowfocus
- **window_resize** — window调整大小

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 桌面操作 可选值: `click, type, hotkey, screenshot, find_image, move_mouse, scroll, window_list, window_focus, window_resize` |
| `x` | integer | 否 | X 坐标 |
| `y` | integer | 否 | Y 坐标 |
| `text` | string | 否 | 输入文本或热键组合 |
| `image` | string | 否 | 要查找的图像路径（find_image 时使用） |
| `window` | string | 否 | 窗口标题（window_focus 时使用） |
| `region` | object | 否 | 截图区域 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: click

```json
{
  "action": "click",
  "x": 10,
  "y": 10,
  "text": "示例输入文本或热键组合",
  "image": "示例值",
  "window": "示例值"
}
```

### 示例 2: type

```json
{
  "action": "type",
  "x": 10,
  "y": 10,
  "text": "示例输入文本或热键组合"
}
```

### 示例 3: hotkey

```json
{
  "action": "hotkey",
  "x": 10,
  "y": 10,
  "text": "示例输入文本或热键组合"
}
```

### 示例 4: screenshot

```json
{
  "action": "screenshot",
  "x": 10,
  "y": 10,
  "text": "示例输入文本或热键组合"
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `desktop_control`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
