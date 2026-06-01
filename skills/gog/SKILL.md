---
name: gog
description: "Google Workspace 套件：统一操作 Gmail/日历/云端硬盘/联系人/表格/文档，支持列出/查看/创建/更新/删除/搜索/发送。当处理 Google 办公服务时触发。"
when_to_use: "需要在 Gmail、Calendar、Drive、Contacts、Sheets、Docs 上执行操作时"
argument-hint: "[service] [action] (可选 query / id / data)"
version: "1.0.0"
---

# Google Workspace 套件

一个 CLI 统一覆盖 Google 全套办公服务。

## 何时使用

- 收发/搜索 Gmail 邮件
- 管理日历事件、Drive 文件、联系人
- 读写 Sheets 表格与 Docs 文档

## 工作流

1. 选择 `service`：gmail / calendar / drive / contacts / sheets / docs。
2. 选择 `action`：list / get / create / update / delete / search / send。
3. 按操作补 `query`（搜索）、`id`（定位资源）或 `data`（创建/更新内容）。
4. 校验结果 `success` 与返回 `data`。

## 参数

- `service`、`action`（必填）。
- `query`、`id`、`data`（按操作可选）。

## 常见陷阱

- delete/update 必须带正确 `id`，先用 list/search 确认目标再操作。
- send（发邮件）是不可撤销动作，发送前与用户确认收件人与正文。

## 输出

- `success` 是否成功、`data` 数据、`count` 数量、`message` 结果描述。
