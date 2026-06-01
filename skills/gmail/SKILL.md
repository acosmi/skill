---
name: gmail
description: "Gmail：经托管 OAuth 集成 Gmail API，读取/发送/管理邮件、线程、标签与草稿。当需要在 Gmail 收发或管理邮件时触发。"
when_to_use: "需要在 Gmail 读写邮件、管理标签或草稿时"
argument-hint: "[action] (按操作带 id/to/subject/body/label)"
version: "1.0.0"
---

# Gmail

完整的 Gmail 自动化，托管 OAuth 免手动鉴权。

## 何时使用

- 列出/读取/搜索邮件与线程
- 发送、回复、转发邮件
- 管理标签、草稿与垃圾箱

## 能力

- `list` · `read` · `send` · `reply` · `forward` · `search` · `label` · `draft` · `trash`

## 工作流

1. 选 `action`，搜索带 `query`，定位带 `id`。
2. 发信带 `to`/`subject`/`body`，可加 `cc`、`label`。

## 常见陷阱

- send/trash 不可撤销，发送前确认收件人。
- label 名需已存在或先创建。

## 输出

- 邮件列表、正文或操作结果。
