# YouTube API

通过托管 OAuth 集成 YouTube Data API，支持搜索视频、管理播放列表、访问频道数据和与评论交互，实现 YouTube 内容运营自动化。

## 概述

**YouTube API** 是一个多媒体处理领域的执行动作类技能。支持 7 种操作模式：搜索, video详情查看, playlist列出, playlist添加, channel详情查看, comments。通过 6 个可配置参数实现灵活控制。

## 功能特性

- **search** — 搜索
- **video_info** — video详情查看
- **playlist_list** — playlist列出
- **playlist_add** — playlist添加
- **channel_info** — channel详情查看
- **comments** — comments
- **captions** — captions

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `action` | string | 是 | YouTube 操作 可选值: `search, video_info, playlist_list, playlist_add, channel_info, comments, captions` |
| `query` | string | 否 | 搜索关键词 |
| `video_id` | string | 否 | 视频 ID |
| `playlist_id` | string | 否 | 播放列表 ID |
| `channel_id` | string | 否 | 频道 ID |
| `max_results` | integer | 否 | 最大结果数，默认 10 |
| `order` | string | 否 | 排序方式 可选值: `relevance`, `date`, `viewCount`, `rating` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例

### 示例 1: 搜索

```json
{
  "action": "search",
  "query": "YouTube API相关查询",
  "video_id": "item-001",
  "playlist_id": "item-001",
  "channel_id": "item-001",
  "max_results": 10,
  "order": "relevance"
}
```

### 示例 2: video详情查看

```json
{
  "action": "video_info",
  "query": "YouTube API相关查询",
  "video_id": "item-001",
  "playlist_id": "item-001",
  "channel_id": "item-001",
  "max_results": 10,
  "order": "relevance"
}
```

### 示例 3: playlist列出

```json
{
  "action": "playlist_list",
  "query": "YouTube API相关查询",
  "video_id": "item-001",
  "playlist_id": "item-001",
  "channel_id": "item-001",
  "max_results": 10,
  "order": "relevance"
}
```

### 示例 4: playlist添加

```json
{
  "action": "playlist_add",
  "query": "YouTube API相关查询",
  "video_id": "item-001",
  "playlist_id": "item-001",
  "channel_id": "item-001",
  "max_results": 10,
  "order": "relevance"
}
```

## 适用场景

- 图像、音频或视频处理时
- 多媒体内容创作或转换时
- 媒体资源管理或优化时

## 注意事项

- 技能标识: `youtube_api`
- 分类: 执行动作类 / 多媒体处理
- 必填参数: `action`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
