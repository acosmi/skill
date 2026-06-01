---
name: youtube-api
description: "YouTube API：经托管 OAuth 集成 YouTube Data API，搜索视频、管理播放列表、访问频道数据、与评论交互。当需要管理 YouTube 内容或播放列表时触发。"
when_to_use: "需要管理 YouTube 播放列表、频道或与评论交互时"
argument-hint: "[action] (可选 query/video_id/playlist_id/channel_id)"
version: "1.0.0"
---

# YouTube API

通过 YouTube Data API 做内容运营自动化。

## 何时使用

- 搜索视频、获取视频信息
- 管理播放列表（列出/添加）
- 访问频道数据、与评论交互

## 能力

- `search` · `video_info` · `playlist_list` · `playlist_add` · `channel_info` 等

## 工作流

1. 选 `action`；按操作带 `video_id`/`playlist_id`/`channel_id`。
2. 用 `max_results` 控制数量。

## 常见陷阱

- playlist_add 会改动账号数据，确认目标播放列表。
- Data API 配额有限。

## 输出

- 视频/播放列表/频道数据或操作结果。
