---
name: api-gateway
description: "API 网关：托管 OAuth 接入 100+ 主流 API（Google/Microsoft/GitHub/Notion/Slack 等），支持增删改查/搜索/发送/Webhook。当需要调第三方 SaaS API 时触发。"
when_to_use: "需要调用某个第三方 SaaS 服务的 API 而不想自己处理 OAuth 时"
argument-hint: "[action] [resource] (可选 id/data/query/params)"
version: "1.0.0"
---

# API 网关

用统一接口与托管 OAuth 接入上百个主流服务。

## 何时使用

- 对某服务资源做列出/读取/创建/更新/删除
- 跨服务搜索、发送、注册 Webhook

## 能力

- `list` · `get` · `create` · `update` · `delete` · `search` · `send` · `webhook`

## 工作流

1. 指定 `resource`（目标服务/资源）与 `action`。
2. 写操作带 `data`，定位带 `id`，查询带 `query`/`params`。

## 常见陷阱

- delete/send 等写操作不可逆，先确认目标 resource 与 id。
- 各服务字段不同，按其 API 规范填 data。

## 输出

- 操作结果与返回数据。
