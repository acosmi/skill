---
name: desktop-control
description: "桌面自动化控制：鼠标/键盘/热键/截图/图像匹配/窗口管理，内置故障安全中止与边界检查。当需要自动化操作本机桌面应用时触发。"
when_to_use: "需要程序化控制本机桌面（点击、输入、截图、找图）时"
argument-hint: "[action] (按操作带 x/y/text/image/window)"
version: "1.0.0"
---

# 桌面自动化控制

高级桌面 GUI 自动化，带安全保护。

## 何时使用

- 移动/点击鼠标、输入文本与热键
- 截图与图像匹配定位元素
- 查找与管理窗口

## 能力

- `click` · `type` · `hotkey` · `screenshot` · `find_image` · `move_mouse` · `scroll` 等

## 工作流

1. 选 `action`；坐标类带 `x`/`y`；输入带 `text`；找图带 `image`。
2. 操作窗口带 `window`，区域截图带 `region`。

## 常见陷阱

- 误操作会作用到真实桌面，先用 screenshot/find_image 定位再动作。
- 触发故障安全（如鼠标移到角落）会中止，属保护机制。

## 输出

- 操作结果、截图或匹配到的坐标/元素。
