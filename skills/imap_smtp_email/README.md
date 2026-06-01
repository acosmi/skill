# IMAP/SMTP 通用邮件

通过 IMAP/SMTP 协议读取和发送邮件，支持检查新邮件、搜索邮箱、标记已读/未读和发送附件，兼容所有主流邮件服务。

## 概述

**IMAP/SMTP 通用邮件** 是一个调研分析领域的执行动作类技能。通过 4 个可配置参数实现灵活控制。

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `query` | string | 是 | 搜索或研究查询 |
| `source` | string | 否 | 数据来源或目标 URL |
| `depth` | string | 否 | 研究深度 可选值: `quick`, `standard`, `deep` |
| `format` | string | 否 | 输出格式 可选值: `summary`, `detailed`, `bullet` |

## 输出格式

返回 JSON 对象，包含以下字段：

| 字段 | 类型 | 说明 |
|------|------|------|
| `success` | boolean | 操作是否成功 |
| `data` | object | 返回数据 |
| `message` | string | 结果描述 |

## 使用示例


```json
{
  "query": "示例搜索或研究查询",
  "source": "示例数据来源或目标 URL",
  "depth": "quick",
  "format": "summary"
}
```

## 适用场景

- 需要搜索和整合多源信息时
- 学术研究或市场调研时
- 竞品分析或行业报告编写时

## 注意事项

- 技能标识: `imap_smtp_email`
- 分类: 执行动作类 / 调研分析
- 必填参数: `query`
- 请确保输入参数符合 JSON Schema 规范
- 超时或异常时请检查参数格式和网络连接
