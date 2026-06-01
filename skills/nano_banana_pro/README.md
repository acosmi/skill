# AI 图片生成与编辑

使用 Nano Banana Pro（Gemini 3 Pro 图像模型）生成和编辑图片，支持文本生成图片和图片编辑，分辨率可选 1K/2K/4K，支持 --input-image 参数。

## 概述

**AI 图片生成与编辑** 是一个多媒体处理领域的执行动作类技能。支持 2 种操作模式：生成, 图片编辑。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **generate** — 生成
- **edit** — 图片编辑

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 操作类型：generate=文本生图, edit=图片编辑 可选值: `generate, edit` |
| `prompt` | string | 是 | 图片生成/编辑的文字描述 |
| `input_image` | string | 否 | 输入图片路径（edit 操作时必填） |
| `resolution` | string | 否 | 输出分辨率，默认 1k 可选值: `1k`, `2k`, `4k` |
| `output` | string | 否 | 输出文件路径 |
| `style` | string | 否 | 风格提示词（如 photorealistic, anime, watercolor） |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `image_path` | string | 生成的图片文件路径 |
| `resolution` | string | 实际输出分辨率 |
| `seed` | integer | 使用的随机种子（可复现） |

## 使用示例

### 示例 1: 生成

```json
{
  "action": "generate",
  "prompt": "示例值",
  "input_image": "示例值",
  "resolution": "1k",
  "output": "示例值",
  "style": "示例值"
}
```

### 示例 2: 图片编辑

```json
{
  "action": "edit",
  "resolution": "1k"
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `nano_banana_pro`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `prompt`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
