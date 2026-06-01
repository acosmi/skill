# 自然语言浏览器自动化

自然语言浏览器自动化 — 通过自然语言 CLI 命令自动化浏览器操作，支持网站浏览、网页数据提取、截图和表单交互，无需编写代码。

## 概述

**自然语言浏览器自动化** 是一个调研分析领域的执行动作类技能。支持 7 种操作模式：运行, 构建, 测试, lint, 格式化, 分析。通过 4 个可配置参数实现灵活控制。

## 功能特性

- **run** — 运行
- **build** — 构建
- **test** — 测试
- **lint** — lint
- **format** — 格式化
- **analyze** — 分析
- **generate** — 生成

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 开发工具操作 可选值: `run, build, test, lint, format, analyze, generate` |
| `input` | string | 否 | 输入代码、文件或项目路径 |
| `language` | string | 否 | 编程语言 |
| `config` | object | 否 | 工具配置 |
| `output_format` | string | 否 | 输出格式 可选值: `json`, `text`, `diff` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 运行

```json
{
  "action": "run",
  "input": "示例值",
  "language": "示例值",
  "output_format": "json"
}
```

### 示例 2: 构建

```json
{
  "action": "build",
  "output_format": "json"
}
```

### 示例 3: 测试

```json
{
  "action": "test",
  "output_format": "json"
}
```

### 示例 4: lint

```json
{
  "action": "lint",
  "output_format": "json"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `browser_automation`
- 分类: 执行动作类 / 调研分析
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
