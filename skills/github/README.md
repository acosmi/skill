# GitHub 工具
> GitHub

使用 gh CLI 与 GitHub 交互，支持 issue 管理、PR 操作、CI/CD 运行查看和高级 API 查询，提升开发效率。

## 概述

**GitHub 工具** 是一个效率工具领域的执行动作类技能。支持 11 种操作模式：issue列出, issue创建, issueview, pr列出, pr创建, pr审查。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **issue_list** — issue列出
- **issue_create** — issue创建
- **issue_view** — issueview
- **pr_list** — pr列出
- **pr_create** — pr创建
- **pr_review** — pr审查
- **pr_merge** — pr合并
- **repo_clone** — repoclone
- **run_list** — 运行列出
- **run_view** — 运行view
- **api** — api

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | GitHub 操作类型 可选值: `issue_list, issue_create, issue_view, pr_list, pr_create, pr_review, pr_merge, repo_clone, run_list, run_view, api` |
| `repo` | string | 否 | 仓库名称（owner/repo 格式） |
| `query` | string | 否 | 搜索或过滤条件 |
| `number` | integer | 否 | Issue 或 PR 编号 |
| `title` | string | 否 | 标题（创建时使用） |
| `body` | string | 否 | 正文内容（创建时使用） |
| `labels` | array | 否 | 标签列表 |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据（Issue/PR/Run 详情） |
| `items` | array | 列表结果 |
| `total` | integer | 总数量 |
| `url` | string | 相关链接 |

## 使用示例

### 示例 1: issue列出

```json
{
  "action": "issue_list",
  "repo": "示例值",
  "query": "GitHub 工具相关查询",
  "number": 10,
  "title": "示例title",
  "body": "示例值",
  "labels": [
    "item1",
    "item2"
  ]
}
```

### 示例 2: issue创建

```json
{
  "action": "issue_create",
  "query": "GitHub 工具相关查询",
  "number": 10,
  "title": "示例title",
  "labels": [
    "item1",
    "item2"
  ]
}
```

### 示例 3: issueview

```json
{
  "action": "issue_view",
  "query": "GitHub 工具相关查询",
  "number": 10,
  "title": "示例title",
  "labels": [
    "item1",
    "item2"
  ]
}
```

### 示例 4: pr列出

```json
{
  "action": "pr_list",
  "query": "GitHub 工具相关查询",
  "number": 10,
  "title": "示例title",
  "labels": [
    "item1",
    "item2"
  ]
}
```

## 适用场景

- 任务管理或待办事项整理时
- 笔记整理或知识库维护时
- 文件格式转换或工具集成时

## 注意事项

- 技能标识: `github`
- 分类: 执行动作类 / 效率工具
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
