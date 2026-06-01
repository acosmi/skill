---
name: auto-updater
description: "技能自动更新：定时检查并更新已安装技能，支持单个/全部/定时/状态，完成推送摘要。当需要保持技能库最新或配置自动更新时触发。"
when_to_use: "想保持技能库最新，或配置每日自动更新时"
argument-hint: "[action] (可选 skill_key/cron/notify)"
version: "1.0.0"
---

# 技能自动更新

通过定时任务自动维护技能库版本。

## 何时使用

- 检查有无可用更新
- 更新全部或指定技能
- 配置定时自动更新计划

## 能力

- `check` · `update_all` · `update_one` · `schedule` · `status`

## 工作流

1. 选 `action`；更新单个带 `skill_key`。
2. `schedule` 带 `cron` 表达式；`notify=true` 完成后通知。

## 常见陷阱

- update_all 可能引入破坏性变更，重要环境先 check 再逐个更新。
- cron 表达式非法不会真正排期。

## 输出

- 更新结果摘要与各技能版本状态。
