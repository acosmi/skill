---
name: find-skills
description: "当用户询问\"怎么做 X\"、\"有没有能做 X 的技能\"或希望扩展智能体能力时自动触发，通过 Skills CLI 搜索、推荐并安装开源技能生态中的可用技能包。"
---

# 技能发现与安装助手

## 何时使用

当用户出现以下意图时触发本技能：

- 询问"怎么做 X"或"能不能帮我 X"，且 X 可能已有现成技能覆盖
- 明确要求"找一个能做 X 的技能"或"有没有 X 相关的技能"
- 希望扩展智能体能力，搜索可用的工具、模板或工作流
- 提到某个领域（设计、测试、部署等）并希望获得专项辅助

## 执行前检查

- 确认运行环境已安装 Node.js 和 `npx`
- 确认网络可访问 https://skills.sh/ 及对应 GitHub 仓库

## 标准流程

### 1. 理解用户需求

明确三个要素：

1. **领域** — 例如 React、测试、部署、设计
2. **具体任务** — 例如写测试、优化性能、审查 PR
3. **是否属于常见场景** — 判断是否可能已有现成技能

### 2. 搜索技能

使用关键词执行搜索：

```bash
npx skills find [query]
```

示例：

| 用户问题 | 搜索命令 |
|---------|---------|
| "怎么让 React 应用更快？" | `npx skills find react performance` |
| "能帮我做 PR Review 吗？" | `npx skills find pr review` |
| "我需要生成 changelog" | `npx skills find changelog` |

### 3. 推荐结果

向用户展示搜索到的技能时，提供以下信息：

1. 技能名称及功能简述
2. 安装命令
3. 详情链接

示例回复：

```
找到一个相关技能："vercel-react-best-practices"，提供来自 Vercel 工程团队的
React / Next.js 性能优化指南。

安装命令：
npx skills add vercel-labs/agent-skills@vercel-react-best-pract
