# PDF 自然语言编辑

PDF 自然语言编辑 — 使用 nano-pdf CLI 通过自然语言指令编辑 PDF 文件，无需学习复杂工具，直接用文字描述操作需求。

## 概述

**PDF 自然语言编辑** 是一个效率工具领域的执行动作类技能。支持 6 种操作模式：teach, quiz, explain, practice, assess, 创建course。通过 5 个可配置参数实现灵活控制。

## 功能特性

- **teach** — teach
- **quiz** — quiz
- **explain** — explain
- **practice** — practice
- **assess** — assess
- **create_course** — 创建course

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | 教育操作 可选值: `teach, quiz, explain, practice, assess, create_course` |
| `topic` | string | 是 | 学习主题 |
| `level` | string | 否 | 难度级别 可选值: `beginner`, `intermediate`, `advanced` |
| `content` | string | 否 | 学习内容 |
| `questions` | integer | 否 | 题目数量（quiz 时使用） |
| `language` | string | 否 | 教学语言 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | - |
| `output_path` | string | 输出文件路径 |
| `pages` | integer | 结果 PDF 页数 |
| `message` | string | - |

## 使用示例

### 示例 1: teach

```json
{
  "action": "teach",
  "topic": "示例值",
  "level": "beginner",
  "content": "示例学习内容",
  "questions": 10,
  "language": "示例值"
}
```

### 示例 2: quiz

```json
{
  "action": "quiz",
  "level": "beginner",
  "content": "示例学习内容",
  "questions": 10
}
```

### 示例 3: explain

```json
{
  "action": "explain",
  "level": "beginner",
  "content": "示例学习内容",
  "questions": 10
}
```

### 示例 4: practice

```json
{
  "action": "practice",
  "level": "beginner",
  "content": "示例学习内容",
  "questions": 10
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `nano_pdf`
- 分类: 执行动作类 / 效率工具
- 必填参数: `action`, `topic`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
