---
name: imap-smtp-email
description: "IMAP/SMTP 通用邮件：经标准协议读取与发送邮件，支持查新邮件、搜索、标记已读/未读、发附件，兼容所有主流邮箱。当需要用通用协议收发邮件时触发。"
when_to_use: "需要用通用 IMAP/SMTP 协议收发任意邮箱的邮件时"
argument-hint: "[action] (可选 folder/id/to/subject/body/attachments/query)"
version: "1.0.0"
---

# IMAP/SMTP 通用邮件

兼容所有主流邮件服务的通用收发客户端。

## 何时使用

- 检查新邮件、读取正文
- 发送邮件（含附件）
- 搜索邮箱、标记已读/未读

## 能力

- `list`/`check` 收件 · `read` 读取 · `send` 发送 · `reply`/`forward` 回复转发 · `search` 搜索 · `flag`/`move` 整理

## 工作流

1. 选 `action`，必要时指定 `folder`。
2. 发信带 `to`/`subject`/`body`，附件用 `attachments`；读/标记带 `id`；搜索带 `query`。

## 常见陷阱

- send 不可撤销，确认收件人与附件路径有效。
- 不同邮箱的 IMAP/SMTP 配置不同，需正确凭据。

## 输出

- 邮件列表、正文或发送/标记结果。
