# Claude Code Skills

本目录收录了个人开发的 Claude Code Skills，每个 skill 都有独立的子文件夹，包含详细文档和可直接使用的 SKILL.md 文件。

## 什么是 Skill？

Skill 是 Claude Code 的扩展机制，通过 Markdown 文件定义专门的指令集和工作流程。当用户输入匹配的触发词时，Claude 会自动加载对应的 skill，以特定角色和流程完成任务。

每个 skill 本质上是一段注入到 Claude 系统提示中的专业指令，让通用模型在特定领域表现得像专家。

## Skill 列表

| Skill | 分类 | 简介 |
|-------|------|------|
| [chinese-natural-writing](./chinese-natural-writing/) | 📝 内容写作 | 撰写没有"AI 味"的中文文章，七大原则系统化去机械化 |
| [universal-teacher](./universal-teacher/) | 🎓 技术学习 | 深入解释代码、架构、算法原理，结构化四步教学法 |
| [virtual-think-tank](./virtual-think-tank/) | 🧠 决策分析 | 模拟多专家辩论会，揭示盲点、权衡和不同视角 |

## 目录结构

```
skill/
├── README.md                         # 本文件
├── chinese-natural-writing/
│   ├── README.md                     # Skill 详细介绍
│   └── SKILL.md                      # Skill 定义文件（可直接使用）
├── universal-teacher/
│   ├── README.md
│   └── SKILL.md
└── virtual-think-tank/
    ├── README.md
    ├── SKILL.md
    └── references/
        ├── panelist-spec.md
        ├── debate-format.md
        └── summary-template.md
```

## 安装使用

将任意 skill 的整个文件夹复制到 `~/.claude/skills/<skill-name>/` 下即可：

```bash
# 示例：安装 chinese-natural-writing
cp -r skill/chinese-natural-writing ~/.claude/skills/
```

Claude Code 启动时会自动扫描 `~/.claude/skills/` 目录并加载所有 skill。

## Skill 设计原则

这些 skill 遵循以下设计理念：

1. **触发精准**：每个 skill 的 description 包含清晰的触发词和使用场景，避免误触发
2. **角色明确**：skill 定义了清晰的角色边界和行为准则，而非模糊的建议
3. **流程结构化**：每个 skill 有明确的工作步骤，确保输出质量稳定
4. **原则驱动**：不仅告诉模型"做什么"，更解释"为什么"，帮助模型在边界情况做出正确判断
5. **自包含**：每个 skill 是独立的文件夹，复制即用，无外部依赖

## 贡献与反馈

如果你使用了这些 skill 并有问题或改进建议，欢迎提 Issue 或 PR。

## 许可

MIT License
