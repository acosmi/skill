---
name: self-improving-agent
description: "自我进化智能体：记录错误/用户纠正/更优做法/主动反思，沉淀经验并跨会话复用。当操作失败、被纠正或发现更好方式时触发。"
when_to_use: "命令失败、用户纠正你、发现更优做法、或需要主动复盘时"
argument-hint: "[event_type] [context] [lesson]"
version: "1.0.0"
---

# 自我进化智能体

记录学习事件并提炼可复用的经验教训，支持跨会话学习传递。

## 何时使用

- 命令或操作意外失败（error）
- 用户纠正了你的做法（correction）
- 发现了更优的方式（discovery）
- 需要主动反思总结（reflection）

## 工作流

1. 判定 `event_type`：error / correction / discovery / reflection。
2. 记录 `context`（触发情境，含操作与环境）。
3. 提炼 `lesson`（一条可执行的经验教训）。
4. 可选补充 `action_taken`（已采取/建议的改进）与 `severity`（low/medium/high）。
5. 沉淀为带 `lesson_id` 的记录，后续同类任务前先检索复用。

## 参数

- `event_type`、`context`、`lesson`（必填）。
- `action_taken`、`severity`（可选）。

## 常见陷阱

- lesson 要具体可执行（“X 情况下应先 Y”），不要写空泛感想。
- severity 影响后续优先级，失败类不要一律标 low。

## 输出

- `lesson_id` 记录标识、`summary` 摘要、`improvements` 改进项、`confidence` 置信度。
