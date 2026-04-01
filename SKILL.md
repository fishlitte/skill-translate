---
name: skill-translate
description: Skill汉化参考指南 - frontmatter元数据中文化方法
triggers:
  - skill translate
  - skill chinese
  - skill汉化
  - 汉化skill
argument-hint: "[查看|参考]"
---

# Skill 汉化参考指南

## Purpose

提供 skill 的 frontmatter 元数据汉化方法参考，汉化文件一般所在位置为.claude\plugins\marketplaces文件夹下。

## Frontmatter 格式说明

SKILL.md 文件开头的 YAML frontmatter：

```yaml
---
name: skill-name              # 内部标识符（保持英文，不修改）
description: 功能描述          # 显示在斜杠命令后（需要汉化）
triggers:
  - trigger-keyword           # 触发关键词（保持英文，不修改）
argument-hint: "[arg1|arg2]"  # 参数提示（可选，建议汉化）
---
```

## 汉化规则

| 字段 | 是否汉化 | 说明 |
|------|---------|------|
| `name` | ❌ 否 | 内部标识符，保持英文 |
| `description` | ✅ 是 | 显示给用户的功能描述 |
| `triggers` | ❌ 否 | 用于匹配的关键词 |
| `argument-hint` | ✅ 可选 | 参数提示，建议汉化 |

## 汉化方法

### 1. 读取目标 SKILL.md

```
读取文件前10行，查看 frontmatter 部分
```

### 2. 定位需要修改的字段

找到 `description:` 开头的行

### 3. 执行替换

使用 Edit 工具替换 frontmatter 部分：

```yaml
# 修改前
description: Original English description

# 修改后
description: 中文功能描述
```

### 4. 验证修改

重新读取文件，确认 frontmatter 格式正确

## 常用翻译对照

| 英文 | 中文 |
|------|------|
| Autonomous | 自主 |
| Agent | 代理 |
| Research | 研究 |
| Experiment | 实验 |
| Training | 训练 |
| Install | 安装 |
| Configure | 配置 |
| Setup | 设置 |
| Run | 运行 |
| Status | 状态 |
| Results | 结果 |
| Validate | 验证 |
| Execute | 执行 |
| Debug | 调试 |
| Monitor | 监控 |
| Workflow | 工作流 |
| Pipeline | 管道 |
| Inference | 推理 |
| Framework | 框架 |
| Multi-session | 多会话 |
| Checkpoint | 检查点 |
| Recovery | 恢复 |
| Dependency | 依赖 |

## 注意事项

1. **YAML 格式**: 冒号后需空格，特殊字符用引号包裹
2. **UTF-8 编码**: 确保文件保存为 UTF-8
3. **不修改 name**: 内部标识符必须保持英文
4. **不修改 triggers**: 匹配关键词保持英文

## 示例

### 汉化前

```yaml
---
name: harness
description: "Multi-session autonomous agent work requiring progress checkpointing"
---
```

### 汉化后

```yaml
---
name: harness
description: "多会话自主代理工作，需要进度检查点"
---
```
