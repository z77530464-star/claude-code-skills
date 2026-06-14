# Claude Code Skills & Prompts

个人 Claude Code 扩展库，包含 Skills（自动触发）和 Prompts（手动使用）两类 AI 增强工具。

## 仓库结构

```
├── skill/                          # Claude Code Skills（自动触发）
│   ├── chinese-natural-writing/    # 中文自然写作，去 AI 味
│   ├── universal-teacher/          # 通用技术导师，深度讲解代码/架构/算法
│   ├── visualization-expert/       # 数据可视化专家，图表选择与设计
│   └── virtual-think-tank/         # 虚拟智囊团，多专家辩论辅助决策
│
└── prompts/                        # Prompt 模板（手动复制使用）
    ├── Concept Demystifier/        # 概念祛魅师，用人话讲透复杂概念
    └── Prompt Engineer/            # 提示词工程师，三阶段工程化流程
```

## 快速开始

### 安装 Skill（推荐）

```bash
# 复制任意 skill 到 Claude Code skills 目录
cp -r skill/<skill-name> ~/.claude/skills/
```

重启 Claude Code 后，skill 会自动加载并在匹配场景下触发。

### 使用 Prompt 模板

打开 `prompts/` 下任意模板文件，全选复制，粘贴到对话开头即可。

## 各模块速览

| 模块 | 类型 | 一句话 |
|------|------|--------|
| chinese-natural-writing | Skill | 让 AI 写的中文像人写的，七大原则去机械化 |
| universal-teacher | Skill | 深度讲解代码/架构/算法，四步结构化教学 |
| visualization-expert | Skill | 数据关系→图表类型，四大设计原则 |
| virtual-think-tank | Skill | 4-6 位虚拟专家辩论，揭示决策盲点 |
| Concept Demystifier | Prompt | 打破学术黑话，大白话讲透复杂概念 |
| Prompt Engineer | Prompt | 三阶段流程，把模糊需求变成高质量 Prompt |

## 设计理念

- **原则驱动**：每个模块不仅告诉 AI "做什么"，更解释"为什么"
- **流程结构化**：明确的工作步骤和门控机制，确保输出质量稳定
- **自包含**：每个模块是独立文件夹，复制即用，无外部依赖
- **角色明确**：清晰的角色边界和行为准则，而非模糊的建议

## 许可

MIT License
