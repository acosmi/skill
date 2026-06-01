---
name: proactive-agent
description: "主动型智能体：预判需求、安排定时任务、缓冲工作、自主反思，从被动执行转为主动协作。当需要需求预判或周期性主动执行时触发。"
when_to_use: "希望智能体主动预判、定时执行或周期复盘，而非被动等待指令时"
argument-hint: "[mode] (schedule 模式需 schedule 表达式)"
version: "1.0.0"
---

# 主动型智能体

将 AI 从被动执行者转变为能预判与持续改进的主动伙伴。

## 何时使用

- 预判用户接下来可能的需求（anticipate）
- 安排定时/周期任务（schedule）
- 缓冲并批处理工作（buffer）
- 周期性自主反思复盘（reflect）

## 工作流

1. 选 `mode`：anticipate / schedule / buffer / reflect。
2. 提供 `task`（任务内容）与 `context`（当前情境，用于预判）。
3. schedule 模式补 `schedule`（cron 表达式或间隔）。
4. 可选设 `priority`：low / medium / high / urgent。

## 常见陷阱

- schedule 模式必须给出合法 cron/间隔，否则不会真正排期。
- 主动行为应有节制，urgent 仅用于真正紧急项，避免打扰。

## 输出

- `action_taken` 已执行行为、`scheduled` 是否已排期、`anticipations` 预判需求、`next_check` 下次检查时间。
