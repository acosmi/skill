---
name: himalaya
description: "Himalaya 邮件：终端邮件客户端，经 IMAP/SMTP 列出/读/发/回复/转发/搜索/整理邮件。当需要在命令行收发或管理邮件时触发。"
when_to_use: "需要在终端收发、阅读或搜索邮件时"
argument-hint: "[action] (按操作带 id/to/subject/body/query)"
version: "1.0.0"
---

# Himalaya 邮件

用 Himalaya CLI 在终端完成全套邮件操作。

## 何时使用

- 列出与阅读邮件
- 发送、回复、转发邮件
- 搜索与标记/整理邮件

## 能力

- `list`/`check` 收件 · `read` 读取 · `send` 发送 · `reply`/`forward` 回复转发 · `search` 搜索 · `flag`/`move` 整理

## 工作流

1. 选 `action`，必要时指定 `folder`。
2. 读/回复/转发带 `id`；发信带 `to`/`subject`/`body`；搜索带 `query`。

## 常见陷阱

- send/reply 不可撤销，发送前确认收件人。
- reply/forward 的 id 要对应正确邮件。

## 输出

- 邮件列表、正文或发送/操作结果。
