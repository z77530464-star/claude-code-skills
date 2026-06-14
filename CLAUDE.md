# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库性质

这是一个 **内容仓库**（非代码工程），存放 Claude Code 的 Skills 和 Prompt 模板。无构建、测试、lint 流程。

## 目录约定

```
skill/<name>/                  # Claude Code Skill（含 YAML frontmatter，可自动触发）
    SKILL.md                   # Skill 定义文件（必须有 frontmatter）
    README.md                  # 详细介绍（内容、原理、场景、优点、问题）
    references/                # 可选：Skill 引用的辅助文件

prompts/<name>/                # Prompt 模板（无 frontmatter，手动复制使用）
    <模板名>.md                 # Prompt 模板文件
    README.md                  # 详细介绍
```

## 新增模块的标准工作流

当用户提供新的 skill 或 prompt 时：

1. **撰写 README**：每个模块必须有 README.md，包含：内容概述、核心原理、适用场景、优点、可能的问题。深入理解模块的 SKILL.md/模板内容后再写 README，不要套模板。
2. **更新目录 README**：更新 `skill/README.md` 或 `prompts/README.md` 中的列表和目录结构。
3. **新增根 README 条目**：若模块值得在仓库首页展示，更新根 `README.md` 的表格。
4. **提交并推送**：`git add -A && git commit -m "<描述>" && git push`

## Git 操作注意事项

此仓库 remote 已配置为 `https://github.com/z77530464-star/claude-code-skills.git`。

推送命令（Windows 下 `gh` 需手动指定路径）：

```bash
export PATH="$PATH:/c/Program Files/GitHub CLI"
git push
```

## 用户偏好（来自全局 CLAUDE.md）

- 沟通语言：中文
- 架构原则：关注点分离、拒绝单文件、高内聚低耦合
- 编码原则：简单优先，只写最少必要代码
- 每个文件开头用中文简要说明内容
