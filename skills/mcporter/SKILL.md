---
name: mcporter
description: "MCP 服务器管理：用 mcporter CLI 列出/添加/授权/调用 MCP 服务器与工具，支持 HTTP/stdio 模式。当需要管理或调用 MCP 服务器时触发。"
when_to_use: "需要查看、配置、授权或调用 MCP 服务器及其工具时"
argument-hint: "[action] (可选 server/tool/params/mode)"
version: "1.0.0"
---

# MCP 服务器管理

通过 mcporter 统一管理与调用 MCP 服务器。

## 何时使用

- 列出已配置的 MCP 服务器与工具
- 添加/移除服务器、完成 OAuth 授权
- 直接调用某服务器的工具

## 能力

- `list` · `add` · `remove` · `authorize` · `call` · `status`

## 工作流

1. 选 `action`；定位带 `server`/`tool`。
2. `call` 带 `params`；`mode` 选 http/stdio。

## 常见陷阱

- call 前先 authorize 完成鉴权；stdio 服务器需本地可执行。
- remove 影响依赖该服务器的技能。

## 输出

- 服务器/工具列表、调用结果或状态。
