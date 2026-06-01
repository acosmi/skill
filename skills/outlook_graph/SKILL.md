---
name: outlook-graph
description: "Outlook & Microsoft Graph：经 Graph 用预置令牌管理 Outlook 邮件/日历/联系人/文件夹（列表/读/发/建事件）。当需要操作 Outlook/M365 时触发。"
when_to_use: "需要读写企业 Outlook 邮件、日历或联系人时"
argument-hint: "[action] (按操作带 id/to/subject/body/start/end)"
version: "1.0.0"
---

# Outlook & Microsoft Graph

通过 Microsoft Graph 自动化 Outlook 与 M365 操作。

## 何时使用

- 列出/读取/发送邮件
- 列出/创建日历事件
- 管理联系人与文件夹

## 能力

- `list_mail` · `read_mail` · `send_mail` · `list_events` · `create_event` 等

## 工作流

1. 选 `action`；读/定位带 `id`，搜索带 `query`。
2. 发信带 `to`/`subject`/`body`；建事件带 `start`/`end`。

## 常见陷阱

- send_mail/create_event 不可撤销，发送前确认收件人与时间。
- 令牌过期会全失败，先确认鉴权有效。

## 输出

- 邮件/事件/联系人数据或操作结果。
