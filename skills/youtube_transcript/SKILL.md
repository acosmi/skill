---
name: youtube-transcript
description: "YouTube 字幕提取：通过 yt-dlp 从视频 URL 提取字幕文本，无需音频处理，输出 text/srt/json，可指定语言。当需要 YouTube 文字稿时触发。"
when_to_use: "用户给出 YouTube 链接想要字幕/文字稿时"
argument-hint: "[url] (可选 language/format)"
version: "1.0.0"
---

# YouTube 字幕提取

直接从 YouTube URL 拉取字幕，快速获取视频文字版。

## 何时使用

- 获取视频字幕/文字稿用于摘要或检索
- 导出 srt 字幕文件

## 工作流

1. 提供 `url`。
2. 可选 `language` 指定字幕语言。
3. 可选 `format`：text / srt / json。

## 常见陷阱

- 视频无字幕且无自动字幕时无法提取。
- 多语言视频指定 language 避免拿错轨。

## 输出

- 字幕文本或字幕文件（按 format）。
