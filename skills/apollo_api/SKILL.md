---
name: apollo-api
description: "Apollo.io API:搜索人脉与组织、补全联系人资料、管理销售管道。当需要查找潜客、丰富联系信息或对接销售流程时触发。"
when_to_use: "需要通过 Apollo.io 搜索人脉/组织、补全联系人或管理销售管道时"
argument-hint: "[action: read|send|search|list] (可选 query/url)"
version: "1.0.0"
---

# Apollo.io 销售情报

通过托管 OAuth 鉴权访问 Apollo.io API,搜索人脉与组织、补全联系人资料并管理销售管道。

## 何时使用

- 需要按关键词搜索潜在客户或目标公司
- 需要补全某个联系人的邮箱、职位等资料
- 需要列出或读取销售管道中的记录
- 与销售外联/CRM 流程对接

## 能力

- `search`:按 query 搜索人脉与组织
- `read`:读取指定联系人或组织详情
- `list`:列出管道中的记录
- `send`:向 Apollo 提交写入/外联请求

## 工作流

1. 准备 query(搜索关键词)或目标 url,确保 MATON_API_KEY 已配置。
2. 选择 action(search/read/list/send)。
3. 执行并解析返回的人脉/组织数据。

## 常见陷阱

- 必须配置 MATON_API_KEY 才能完成托管 OAuth 鉴权。
- query 为必填参数,缺失会导致请求失败。
- send 会写入远端数据,执行前确认内容无误。

## 输出

- 返回匹配的人脉/组织记录或写入操作的结果状态。
