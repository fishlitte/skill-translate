# 🧩 Skill 汉化参考指南

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-blue)](https://claude.ai)

一个用于指导汉化 Claude Skill 元数据的参考指南，帮助你将 `SKILL.md` 中的 `description` 字段翻译为中文，同时保持功能正常。

## 📖 简介

Claude Skill 的 `SKILL.md` 文件使用 YAML frontmatter 定义名称、描述、触发关键词等元数据。为了便于中文用户识别和使用，本指南提供了：

- 清晰的汉化规则（哪些字段需要翻译）
- 逐字段的修改方法
- 常用技术术语的翻译对照表
- 完整的操作示例

## ✨ 功能特点

- **规则明确**：仅汉化 `description` 和 `argument-hint`，保留 `name` 和 `triggers` 英文
- **操作简单**：提供四步修改法（读取 → 定位 → 编辑 → 验证）
- **术语对照**：收录 20+ 个常见技术词汇的中文翻译
- **格式提醒**：包含 YAML 格式规范和 UTF-8 编码要求

## 📦 安装与使用

### 作为 Skill 使用

1. 将本仓库的 `SKILL.md` 文件放置在你的 Claude 项目目录中：
   ```
   .claude/plugins/marketplaces/skill-localize/
   ```
2. 在对话中输入以下任一触发词即可启用：
   - `skill translate`
   - `skill chinese`
   - `skill汉化`
   - `汉化skill`

### 手动参考

如果你希望直接阅读本指南，也可以直接打开仓库中的 `SKILL.md` 文件，其中包含了全部规则和示例。

## 📋 汉化规则速查

| 字段 | 是否汉化 | 说明 |
| :--- | :---: | :--- |
| `name` | ❌ 否 | 内部标识符，必须保持英文 |
| `description` | ✅ 是 | 显示给用户的功能描述 |
| `triggers` | ❌ 否 | 匹配关键词，保持英文 |
| `argument-hint` | ✅ 可选 | 参数提示，建议汉化 |

## 🔧 使用示例

**汉化前：**

```yaml
---
name: harness
description: "Multi-session autonomous agent work requiring progress checkpointing"
---
```

**汉化后：**

```yaml
---
name: harness
description: "多会话自主代理工作，需要进度检查点"
---
```

## 📚 常用术语对照

| 英文 | 中文 | 英文 | 中文 |
| :--- | :--- | :--- | :--- |
| Autonomous | 自主 | Framework | 框架 |
| Agent | 代理 | Multi-session | 多会话 |
| Research | 研究 | Checkpoint | 检查点 |
| Experiment | 实验 | Recovery | 恢复 |
| Training | 训练 | Dependency | 依赖 |
| Install | 安装 | Workflow | 工作流 |
| Configure | 配置 | Pipeline | 管道 |
| Setup | 设置 | Inference | 推理 |
| Run | 运行 | Validate | 验证 |
| Status | 状态 | Execute | 执行 |
| Results | 结果 | Debug | 调试 |
| Monitor | 监控 | | |

## ⚠️ 注意事项

1. 确保文件保存为 **UTF-8** 编码
2. YAML 格式中冒号后必须有一个空格
3. 描述中包含特殊字符时请使用引号包裹（如冒号、引号本身）
4. **严禁修改 `name` 和 `triggers` 字段**，否则可能导致 Skill 无法正常触发

## 🤝 贡献

欢迎提交 Pull Request 或 Issue 来改进本指南：

- 补充更多术语翻译
- 优化操作步骤描述
- 修复格式或拼写错误

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE) 开源。

---

**让 Skill 更贴近中文用户，从汉化开始。**
