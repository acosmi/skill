---
name: slack
description: "Slack：发送消息、表情回应、置顶/取消置顶、列频道、读历史、上传文件，覆盖频道与私信。当需要在 Slack 收发消息或管理频道时触发。"
when_to_use: "需要在 Slack 发消息、通知团队或管理频道内容时"
argument-hint: "[action] (可选 channel/message/emoji/thread_ts/file)"
version: "1.0.0"
---

# Slack

完整的 Slack 自动化，覆盖消息与频道操作。

## 何时使用

- 发送消息与线程回复
- 加表情回应、置顶/取消置顶
- 列频道、读历史、上传文件

## 能力

- `send` · `react` · `pin` · `unpin` · `list_channels` · `history` · `upload`

## 工作流

1. 选 `action`，指定 `channel`。
2. 发消息带 `message`，线程带 `thread_ts`；回应带 `emoji`；上传带 `file`。

## 常见陷阱

- send 会真实发到频道，确认 channel 正确避免误发。
- history 量大时注意分页与限流。

## 输出

- 发送结果、频道/历史列表或操作回执。
