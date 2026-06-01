---
name: openai-whisper
description: "Whisper 语音转文字：本地离线转写，无需 API 密钥，多语言多格式，输出 text/srt/vtt/json，可翻译为英文。当需要音频转文字/字幕时触发。"
when_to_use: "用户有音频文件想转成文字或字幕时"
argument-hint: "[audio_file] (可选 language/model/output_format/translate)"
version: "1.0.0"
---

# Whisper 语音转文字

使用本地 Whisper CLI 离线完成语音转写，保护数据隐私。

## 何时使用

- 把语音/录音/音频转为文字
- 生成 srt/vtt 字幕文件
- 把非英文音频转写并翻译为英文

## 工作流

1. 提供 `audio_file`。
2. 可选 `language`（默认自动检测）。
3. 选 `model`：tiny/base/small/medium/large（越大越准越慢）。
4. 选 `output_format` 与 `translate`。

## 常见陷阱

- 大模型更准但慢且吃显存/内存，按时长权衡。
- 小语种或嘈杂音频建议用 medium 以上。

## 输出

- 转写文本或字幕文件（按 output_format）。
