---
name: sonoscli
description: "Sonos 音响控制：发现设备、查询状态、播放/暂停/切歌、调音量、多房间分组。当需要控制 Sonos 音响时触发。"
when_to_use: "需要控制 Sonos 智能音响的播放、音量或分组时"
argument-hint: "[action] (可选 speaker / value / group_members)"
version: "1.0.0"
---

# Sonos 音响控制

控制 Sonos 智能音响系统，覆盖发现、播放与分组。

## 何时使用

- 发现局域网内的 Sonos 设备
- 播放/暂停/停止、切换上一首下一首
- 调节音量、组建多房间同步播放

## 能力

- `discover` 发现 · `status` 状态 · `play`/`pause`/`stop` · `next`/`previous` · `volume` 音量 · `group`/`ungroup` 分组

## 工作流

1. 先 `discover` 获取 `speaker` 标识。
2. 用 `action` 指定操作，音量类带 `value`，分组类带 `group_members`。

## 常见陷阱

- volume 的 value 一般 0-100，越界会被钳制或拒绝。
- 分组操作需所有成员在同一网络且可达。

## 输出

- 操作结果与设备/播放状态。
