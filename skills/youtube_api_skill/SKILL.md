---
name: youtube-api-skill
description: "YouTube 搜索：经托管 OAuth 调用 YouTube Data API，搜索视频、获取视频/频道信息与评论。当需要在 YouTube 搜视频或查频道/评论时触发。"
when_to_use: "需要在 YouTube 搜索视频或查询视频/频道/评论时"
argument-hint: "[action] (可选 query/video_id/channel_id/max_results)"
version: "1.0.0"
---

# YouTube 搜索

通过 YouTube Data API 检索视频与元数据。

## 何时使用

- 按关键词搜索视频
- 获取视频详情与评论
- 查询频道信息

## 能力

- `search` · `video_info` · `channel_info` · `comments`

## 工作流

1. 选 `action`；搜索带 `query`，定位带 `video_id`/`channel_id`。
2. 用 `max_results` 控制数量。

## 常见陷阱

- Data API 有配额上限，避免高频大批量请求。
- video_id/channel_id 需为合法 ID。

## 输出

- 视频搜索结果、视频/频道详情或评论列表。
