---
name: video-frames
description: "视频帧提取：用 ffmpeg 按时间戳提取指定帧或短片段，精确定位，输出 png/jpg/gif。当需要从视频抽帧或截取片段时触发。"
when_to_use: "用户想从视频中取某一帧、生成缩略图或截取短片段时"
argument-hint: "[input] [timestamp] (可选 duration/fps/format)"
version: "1.0.0"
---

# 视频帧提取

基于 ffmpeg 精确提取视频帧与片段。

## 何时使用

- 提取指定时间戳的单帧
- 生成缩略图
- 截取短片段或转 gif

## 工作流

1. 提供 `input`（视频）与 `timestamp`（如 00:01:23）。
2. 可选 `duration` 截片段、`fps`、`format`(png/jpg/gif)。

## 常见陷阱

- timestamp 超出时长会失败；先确认视频长度。
- gif 输出体积大，控制 duration 与 fps。

## 输出

- 提取的帧图片或片段文件。
