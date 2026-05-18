# 自我进化智能体

记录学习、错误和修正以实现持续改进。适用场景：（1）命令或操作意外失败时；（2）用户纠正操作时；（3）发现更好方式时。支持 CrabClaw 集成与跨会话学习传递。

## 概述

**自我进化智能体** 是一个教育学习领域的执行动作类技能。通过 5 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `event_type` | string | 是 | 学习事件类型：error=操作失败, correction=用户纠正, discovery=发现更优方式, reflection=主动反思 可选值: `error`, `correction`, `discovery`, `reflection` |
| `context` | string | 是 | 触发学习的上下文描述，包含操作内容和环境信息 |
| `lesson` | string | 是 | 从事件中提取的经验教训 |
| `action_taken` | string | 否 | 已采取或建议的改进措施 |
| `severity` | string | 否 | 事件严重程度 可选值: `low`, `medium`, `high` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `lesson_id` | string | 学习记录唯一标识 |
| `summary` | string | 学习成果摘要 |
| `improvements` | array | 具体改进列表 |
| `confidence` | number | 改进置信度 0-1 |

## 使用示例


```json
{
  "event_type": "error",
  "context": "示例触发学习的上下文描述，包含操作",
  "lesson": "示例从事件中提取的经验教训",
  "action_taken": "示例已采取或建议的改进措施",
  "severity": "low"
}
```

## 适用场景

- 教学内容准备或课程设计时
- 学习辅导或知识问答时
- 考试准备或练习生成时

## 注意事项

- 技能标识: `self_improving_agent`
- 分类: 执行动作类 / 教育学习
- 必填参数: `event_type`, `context`, `lesson`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
