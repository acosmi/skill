# 自动化工作流设计

设计和实施自动化工作流以节省时间、扩展业务。涵盖自动化机会识别、工作流设计、工具选型（Zapier、Make、n8n）、测试和维护全流程。

## 概述

**自动化工作流设计** 是一个自动化领域的执行动作类技能。支持 6 种操作模式：创建, 编辑, preview, 导出, 分析, 生成。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **create** — 创建
- **edit** — 编辑
- **preview** — preview
- **export** — 导出
- **analyze** — 分析
- **generate** — 生成

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 设计操作 可选值: `create, edit, preview, export, analyze, generate` |
| `component` | string | 否 | 组件/页面类型 |
| `description` | string | 是 | 设计需求描述 |
| `style` | string | 否 | 设计风格 |
| `framework` | string | 否 | 技术框架 |
| `responsive` | boolean | 否 | 是否响应式 |
| `output` | string | 否 | 输出路径 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 创建

```json
{
  "action": "create",
  "component": "示例值",
  "description": "示例值",
  "style": "示例值",
  "framework": "示例值",
  "responsive": true,
  "output": "示例值"
}
```

### 示例 2: 编辑

```json
{
  "action": "edit",
  "responsive": true
}
```

### 示例 3: preview

```json
{
  "action": "preview",
  "responsive": true
}
```

### 示例 4: 导出

```json
{
  "action": "export",
  "responsive": true
}
```

## 适用场景

- 重复性工作流需要自动化时
- 定时任务或触发器配置时
- 跨系统集成或数据同步时

## 注意事项

- 技能标识: `automation_workflows`
- 分类: 执行动作类 / 自动化
- 必填参数: `action`, `description`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
