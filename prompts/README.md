# Prompt 模板库

本目录收录了可复用的 AI Prompt 模板（角色定义）。与 `skill/` 不同，这些模板**不是** Claude Code Skill（没有触发机制和 YAML frontmatter），而是精心设计的角色提示词，可以直接复制到任何 LLM 对话中使用。

## 什么是 Prompt 模板？

Prompt 模板是一段经过精心设计的角色定义和指令集，通过定义 AI 的角色、工作流程和输出标准，让通用模型在特定任务上表现出专家级行为。

与 skill 的区别：

| 特性 | Skill | Prompt 模板 |
|------|-------|-------------|
| 触发方式 | 自动（匹配关键词） | 手动（复制粘贴） |
| 平台限制 | 仅 Claude Code | 任何 LLM |
| 复杂度 | 可引用外部文件 | 单文件自包含 |
| 安装方式 | 放入 `~/.claude/skills/` | 直接复制文本 |

## Prompt 列表

| Prompt | 分类 | 简介 |
|--------|------|------|
| [Concept Demystifier](./Concept%20Demystifier/) | 🎓 教学学习 | 打破学术"黑话"，用大白话将复杂概念直观化 |
| [Prompt Engineer](./Prompt%20Engineer/) | 🛠️ 元工具 | 将模糊需求转化为结构化 Prompt 的三阶段工程化流程 |

## 目录结构

```
prompts/
├── README.md
├── Concept Demystifier/
│   ├── README.md
│   └── 概念祛魅师 (Concept Demystifier).md
└── Prompt Engineer/
    ├── README.md
    └── 提示词工程师（Prompt Engineer）.md
```

## 使用方式

### 方式一：直接使用

打开 Prompt 文件，全选复制，粘贴到 Claude/ChatGPT/其他 LLM 对话开头即可。

### 方式二：改造为 Skill

如果你希望它像 skill 一样自动触发，可以在文件头部添加 YAML frontmatter：

```yaml
---
name: my-skill-name
description: 触发条件和场景描述
---
```

然后放入 `~/.claude/skills/` 目录。

## 设计理念

这些 Prompt 遵循以下设计原则：

1. **角色先行**：先定义"你是谁"，再定义"你做什么"——角色比指令更能约束模型行为
2. **流程门控**：关键阶段设置"必须用户确认"的门控，确保方向不跑偏
3. **输出可复制**：最终产物放在代码块中，用户一键复制即用
4. **批判优于执行**：先质疑需求的合理性，再开始干活
