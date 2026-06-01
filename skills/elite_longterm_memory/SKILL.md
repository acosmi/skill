---
name: elite-longterm-memory
description: "精英长期记忆系统：WAL+向量搜索+git-notes+云备份，支持存储/召回/搜索/同步/备份/清理，永不丢上下文。当需要长期记忆存取或备份时触发。"
when_to_use: "需要把重要上下文长期保存、跨会话/工具召回或备份时"
argument-hint: "[action] (可选 content/query/tags/importance/ttl)"
version: "1.0.0"
---

# 精英长期记忆系统

为智能体提供可同步、可备份的终极长期记忆。

## 何时使用

- 持久化存储重要上下文与结论
- 跨会话语义召回与搜索
- 同步/备份记忆、清理过期项

## 能力

- `store` · `recall` · `search` · `sync` · `backup` · `prune`

## 工作流

1. `store` 带 `content`，标 `importance`(low/medium/high/critical) 与可选 `ttl`。
2. `recall`/`search` 带 `query`，可按 `tags` 过滤。

## 常见陷阱

- critical 记忆勿设短 ttl 以免被清理。
- prune 不可逆，先 backup。

## 输出

- 存储确认、召回条目或同步/备份状态。
