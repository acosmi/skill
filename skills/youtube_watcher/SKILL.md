---
name: youtube-watcher
description: "YouTube 视频分析：读取视频字幕做摘要、内容问答或信息提取，需视频有字幕。当需要总结或追问 YouTube 视频内容时触发。"
when_to_use: "用户给出 YouTube 链接想要摘要、问答或提取信息时"
argument-hint: "[url] (可选 task/question/topic)"
version: "1.0.0"
---

# YouTube 视频分析

基于视频字幕完成摘要、问答与定向信息提取。

## 何时使用

- 总结一条 YouTube 视频要点
- 就视频内容做问答
- 从视频中提取特定主题信息

## 能力

- `summarize` 摘要 · `qa` 问答 · `extract` 提取

## 工作流

1. 提供 `url`。
2. `qa` 带 `question`；`extract` 带 `topic`。

## 常见陷阱

- 视频无字幕则无法分析；优先选有字幕的视频。
- 超长视频建议先 summarize 再 qa。

## 输出

- 摘要、问答回复或提取到的信息。
