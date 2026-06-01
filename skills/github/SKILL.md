---
name: github
description: "GitHub：用 gh CLI 管理 issue、PR（创建/审查/合并）、查看 CI/CD 运行、克隆仓库与 API 查询。当需要在 GitHub 上协作开发时触发。"
when_to_use: "需要操作 GitHub 的 issue、PR、CI 运行或仓库时"
argument-hint: "[action] (可选 repo / number / title / body / labels)"
version: "1.0.0"
---

# GitHub

通过 gh CLI 与 GitHub 交互，提升开发协作效率。

## 何时使用

- 列出/创建/查看 issue
- 列出/创建/审查/合并 PR
- 查看 CI/CD 运行、克隆仓库、调用 GitHub API

## 能力（action）

- issue：`issue_list` / `issue_create` / `issue_view`
- PR：`pr_list` / `pr_create` / `pr_review` / `pr_merge`
- 其他：`repo_clone` / `run_list` / `run_view` / `api`

## 工作流

1. 选 `action`，带上 `repo`（owner/repo 格式）。
2. 创建类操作补 `title` / `body` / `labels`；定位类补 `number`。
3. 合并/审查前先 `pr_view`/`pr_list` 确认目标 PR 状态。

## 常见陷阱

- `pr_merge` 不可逆，合并前确认分支、CI 通过与审查意见。
- repo 用 `owner/repo` 全名，省略会作用到错误仓库。

## 输出

- `success`、`data`（详情）、`items`（列表）、`total`、`url`。
