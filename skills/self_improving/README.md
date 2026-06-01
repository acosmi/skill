---
name: self-improving
description: >
  CrabClaw 桌面智能体的主动自进化引擎。通过自我反思、自我批评、学习沉淀和记忆整理四大闭环，
  让智能体在每次任务执行后主动评估质量、捕捉错误模式、永久固化经验，实现真正的自主进化。
  深度集成 UHMS 高维记忆系统和多智能体 Fleet 治理框架。
version: 2.0.0
author: Acosmi
keywords: [self-evolve, reflection, critique, learning, memory, CrabClaw, UHMS, meta-skill]
---

# 主动自进化智能体

> 生物进化的核心机制：变异、选择、保留。Self-Improving 将同样的机制应用到 CrabClaw 桌面智能体——不断发现可改进的角度，用实验找到更好的方案，然后永久固化到记忆系统。

## 概述

**主动自进化智能体**是 CrabClaw 桌面智能体生态的核心 meta-skill。它不直接解决业务问题，而是让智能体自身变强。通过 5 种操作模式（反思、批评、学习、整理、回忆），智能体在每次任务执行后主动评估自身工作质量，捕捉错误并永久改进，实现真正的自主进化。

### 核心进化闭环

reflect(自我反思) -> critique(自我批评) -> learn(学习沉淀) -> organize(记忆整理) -> recall(经验回忆) -> 回到 reflect

## 与 CrabClaw 桌面智能体的深度集成

### 1. UHMS 高维记忆系统

Self-Improving 通过 CrabClaw 的 UHMS（Universal High-Dimensional Memory Storage）实现长期记忆持久化：

- **日志记忆**: 每次反思/学习结果自动写入 `memory/YYYY-MM-DD.md` 日志
- **策略记忆**: 高价值洞察提炼后固化到 `MEMORY.md` 长期记忆
- **向量检索**: 基于 BM25 + 语义混合搜索（支持 OpenAI/Gemini/Voyage 向量化），recall 操作可精准检索历史经验
- **知识图谱**: 将学习到的概念/实体/事件构建为加权关系图，支持跨领域关联推理

### 2. 引导文件协同

CrabClaw 运行时会注入 5 个引导文件到智能体系统提示词中：

| 文件 | 作用 | Self-Improving 如何利用 |
|------|------|------------------------|
| AGENTS.md | 操作指令 | reflect 分析执行指令的合理性 |
| SOUL.md | 人格与边界 | critique 检查是否偏离核心价值观 |
| TOOLS.md | 工具使用指南 | learn 沉淀工具组合的最佳实践 |
| USER.md | 用户画像 | organize 按用户偏好重组记忆 |
| IDENTITY.md | 身份与风格 | recall 回忆与当前身份一致的经验 |

### 3. 多智能体 Fleet 治理

在 CrabClaw 的六层治理框架中，Self-Improving 可以：

- **L1 能力树**: 评估当前工具能力是否匹配任务需求
- **L2 蓝图**: 通过 agent_blueprint_suggest 分析并改进智能体蓝图
- **L4 编排**: 反思 Pipeline/Swarm 编排策略的效率
- **L5 舰队管理**: 监控 BudgetTracker 消耗，优化资源分配
- **L6 治理**: 评估 Intent 路由和审批决策的准确性

## 五大操作模式详解

### reflect — 自我反思

对刚完成的任务进行全面复盘，评估执行质量、发现改进空间。

**触发时机**: 每次重要任务完成后自动触发，或用户主动要求反思。

**反思维度**:
- 目标达成度（是否完全满足用户需求）
- 执行效率（耗时、步骤数、工具调用次数）
- 方案质量（是否有更优的替代方案）
- 错误检测（是否引入新问题或副作用）

**使用示例**:

```json
{
  "action": "reflect",
  "content": "刚完成了用户的代码重构请求：将 10 个 React Class Component 迁移到 Hooks",
  "task_result": "已完成迁移，但 3 个组件的 useEffect 依赖数组不够精确，可能导致不必要的重渲染"
}
```

**输出示例**:

```json
{
  "insight": "Class->Hooks 迁移时，应优先分析 componentDidMount/Update 的依赖关系，再映射到 useEffect。发现规律：含 this.setState 回调的组件需特别注意闭包陷阱。",
  "score": 72,
  "memories_updated": 2,
  "improvements": [
    "建立 Class->Hooks 迁移检查清单",
    "useEffect 依赖应使用 ESLint exhaustive-deps 规则预检",
    "含 timer/subscription 的组件应优先使用 useRef 而非 useState"
  ]
}
```

### critique — 自我批评

对输出结果进行严格的质量审查，主动发现盲点和不足。

**与 reflect 的区别**: reflect 是全面复盘（诊断），critique 是深度挑错（压力测试）。

**使用示例**:

```json
{
  "action": "critique",
  "content": "审查刚生成的 API 设计方案：用户管理模块 RESTful 端点设计",
  "task_result": "设计了 8 个端点：GET/POST/PUT/DELETE users, GET/PUT users/:id/profile, POST users/:id/avatar"
}
```

**输出示例**:

```json
{
  "insight": "API 设计缺少：1) 批量操作端点 2) 分页参数规范 3) 错误码标准 4) 版本策略。avatar 端点应支持 multipart/form-data 而非 JSON。",
  "score": 58,
  "memories_updated": 1,
  "improvements": [
    "API 设计必须包含分页、排序、过滤三要素",
    "文件上传端点独立于 CRUD 体系",
    "每个模块应定义错误码范围（如 user: 1001-1099）"
  ]
}
```

### learn — 学习沉淀

将有价值的发现、技巧、模式固化为持久知识，写入 UHMS 记忆系统。

**学习分类体系**:
- `pattern` — 代码/设计模式（可复用的最佳实践）
- `pitfall` — 陷阱与坑（避免重复踩坑）
- `preference` — 用户偏好（个性化服务）
- `domain` — 领域知识（业务理解）
- `tool` — 工具技巧（工具链优化）

**使用示例**:

```json
{
  "action": "learn",
  "content": "发现 PostgreSQL 的 JSONB GIN 索引对 tags 数组字段查询性能提升 50x，但对单值查询无明显帮助",
  "category": "pattern"
}
```

**输出示例**:

```json
{
  "insight": "已沉淀为长期记忆：PostgreSQL 性能优化模式 -- JSONB GIN 索引适用场景为数组包含查询(@>)和存在性查询(?)，不适用于等值比较。",
  "score": 95,
  "memories_updated": 1,
  "improvements": [
    "数据库索引选型应根据查询模式决定，非字段类型"
  ]
}
```

### organize — 记忆整理

定期整理和压缩记忆库，合并相似条目，删除过时信息，维护知识图谱健康度。

**整理策略**:
- **去重合并**: 将多次学到的相似经验合并为一条高质量记忆
- **时效清理**: 标记过时的技术栈/版本相关记忆
- **关联增强**: 在知识图谱中建立跨领域关联（如 React Hooks 与闭包与内存泄漏的关联）
- **优先级排序**: 按使用频率和价值评分重排记忆

**使用示例**:

```json
{
  "action": "organize",
  "content": "整理过去一周的学习记忆，合并 React 相关的 5 条经验为最佳实践清单"
}
```

### recall — 经验回忆

基于当前任务上下文，从 UHMS 记忆系统中检索相关历史经验，辅助决策。

**检索策略**: BM25 关键词匹配 + 语义向量相似度混合排序，支持跨会话、跨日期检索。

**使用示例**:

```json
{
  "action": "recall",
  "content": "即将进行数据库迁移，需要回忆之前的迁移经验",
  "query": "数据库迁移 DDL 注意事项 PostgreSQL"
}
```

**输出示例**:

```json
{
  "insight": "检索到 3 条相关经验：1) ALTER TABLE ADD COLUMN 带 DEFAULT 值在 PG12+ 不锁表 2) 迁移脚本必须幂等（IF NOT EXISTS）3) 大表加索引应使用 CONCURRENTLY",
  "score": 88,
  "memories_updated": 0,
  "improvements": []
}
```

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| action | string | 是 | 操作模式：reflect(自我反思), critique(自我批评), learn(学习沉淀), organize(记忆整理), recall(经验回忆) |
| content | string | 是 | 反思/学习/批评的具体内容描述，越详细越好 |
| task_result | string | 否 | 需要评估的任务结果（reflect/critique 时建议提供） |
| query | string | 否 | 经验检索查询关键词（recall 时必须提供） |
| category | string | 否 | 学习分类标签：pattern/pitfall/preference/domain/tool（learn 时建议提供） |

## 输出格式

| 字段 | 类型 | 说明 |
|------|------|------|
| insight | string | 生成的洞察、改进建议或检索到的经验总结 |
| score | number | 质量评分 0-100（reflect/critique 为任务质量分，learn 为知识价值分，recall 为匹配相关度） |
| memories_updated | integer | 本次操作写入/更新的 UHMS 记忆条数 |
| improvements | string[] | 具体可执行的改进行动清单 |

## 进化策略与最佳实践

### 推荐进化流程

任务完成后: reflect(复盘) -> critique(挑错) -> learn(沉淀) -> organize(整理)
新任务开始前: recall(回忆相关经验) -> 执行任务 -> 回到上述闭环

### CrabClaw 工作流集成

在 CrabClaw 的 DAG 工作流引擎中，可将 Self-Improving 嵌入为后处理节点：

```yaml
nodes:
  - id: execute_task
    type: ACTION
    skill: target_skill
  - id: auto_reflect
    type: ACTION
    skill: self_improving
    input_map:
      action: reflect
      content: "任务执行结果回顾"
      task_result: "{{execute_task.output}}"
  - id: auto_learn
    type: ACTION
    skill: self_improving
    input_map:
      action: learn
      content: "{{auto_reflect.insight}}"
      category: pattern
edges:
  - from: execute_task
    to: auto_reflect
  - from: auto_reflect
    to: auto_learn
```

### 定期维护建议

| 频率 | 操作 | 说明 |
|------|------|------|
| 每次任务后 | reflect | 保持持续改进节奏 |
| 每天 | organize | 防止记忆碎片化 |
| 每周 | critique + recall | 深度审视本周决策质量 |
| 每月 | 全量 organize | 清理过时记忆，优化知识图谱 |

## 与其他技能的协同

| 技能 | 协同方式 |
|------|----------|
| self_evolve | Self-Improving 进行诊断发现短板，Self-Evolve 对短板寻找解法并跑实验验证 |
| self_evolve_agent | Self-Improving 提供进化方向，Agent 版本执行实际的蓝图修改 |
| agent_blueprint_suggest | recall 历史经验辅助蓝图推荐，learn 沉淀蓝图效果反馈 |
| memory_search | 底层记忆检索能力，recall 操作的核心依赖 |

## 安全与边界

- **只读引导文件**: Self-Improving 只分析 AGENTS.md/SOUL.md 等引导文件，不直接修改
- **记忆隔离**: 每个租户的记忆独立存储，不会跨租户泄露
- **评分透明**: 所有 score 评分附带评分维度说明，可追溯
- **人工覆盖**: 用户可随时修正 learn 沉淀的记忆，优先级高于自动学习

## 技术规格

- **技能标识**: self_improving
- **分类**: ACTION / PRODUCTIVITY
- **超时**: 30 秒
- **重试**: 失败自动重试 1 次，间隔 1 秒
- **依赖**: UHMS 记忆系统（CrabClaw 内置）
- **兼容**: CrabClaw Desktop v2.0+，Nexus V4 后端
