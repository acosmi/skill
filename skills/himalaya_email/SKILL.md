---
name: himalaya-email
description: "Himalaya 邮件 CLI：经 IMAP/SMTP 列出/读/撰写/回复/转发/搜索/移动/标记邮件，支持多账号与 MIME 附件。当需要命令行收发管理邮件时触发。"
when_to_use: "需要用命令行管理多账号邮件、含附件收发时"
argument-hint: "[action] (可选 account/folder/id/to/subject/body/query)"
version: "1.0.0"
---

# Himalaya 邮件 CLI

功能完整的终端邮件客户端，支持多账号与附件。

## 何时使用

- 列出、阅读、撰写邮件
- 回复、转发、搜索邮件
- 移动、标记、整理邮件

## 能力

- `list` · `read` · `compose` · `reply` · `forward` · `search` · `move` · `flag`

## 工作流

1. 选 `action`，多账号时指定 `account`、`folder`。
2. 撰写带 `to`/`subject`/`body`；定位带 `id`；搜索带 `query`。

## 常见陷阱

- compose/reply 不可撤销；多账号下先确认 account。
- move/flag 的 id 需有效。

## 输出

- 邮件列表、正文或操作结果。
