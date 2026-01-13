# Skill 模板使用说明

这个目录包含了创建新 Skill 的模板文件。

## 如何使用模板

### 方法 1：复制整个目录

```bash
# 复制模板目录
cp -r skills/_template skills/your-skill-name

# 进入新目录
cd skills/your-skill-name

# 编辑文件
# - 修改 SKILL.md
# - 修改 instructions.md
# - 删除本 README.md（可选）
```

### 方法 2：手动创建

1. 在 `skills/` 下创建新目录
2. 复制 `SKILL.md` 和 `instructions.md` 到新目录
3. 根据你的需求修改文件内容

## 模板文件说明

### SKILL.md

这是技能的主要说明文档，包含：
- YAML frontmatter（元数据）
- 功能描述
- 使用场景
- 使用方法
- 配置说明
- 示例
- 限制和注意事项

### instructions.md

这是给 Claude 的指令文件，包含：
- 目标说明
- 工作流程
- 具体指令
- 输出格式
- 错误处理

## 填写指南

### 1. 更新 YAML Frontmatter

```yaml
---
name: your-skill-name        # 改为你的技能名称
description: 简短描述         # 一句话说明功能
version: 1.0.0               # 保持初始版本
author: 你的名字              # 填写你的名字
created: 2026-01-13          # 更新为当前日期
updated: 2026-01-13          # 更新为当前日期
tags:                        # 添加相关标签
  - 标签1
  - 标签2
dependencies: []             # 如果有依赖，在这里列出
---
```

### 2. 填写功能描述

清晰地说明：
- 这个 Skill 做什么
- 解决什么问题
- 主要功能点

### 3. 说明使用场景

列出 3-5 个实际的使用场景，帮助用户理解何时使用这个 Skill。

### 4. 提供使用方法

说明：
- 如何触发这个 Skill
- 需要提供什么输入
- 如何配置（如果需要）

### 5. 添加示例

至少提供 2-3 个实际的使用示例，包括：
- 输入内容
- 期望的输出
- 说明

### 6. 编写指令

在 `instructions.md` 中：
- 明确说明工作流程
- 提供具体的处理步骤
- 定义输出格式
- 说明错误处理

## 检查清单

提交前确保：

- [ ] 更新了所有 YAML frontmatter 字段
- [ ] 功能描述清晰完整
- [ ] 提供了使用场景
- [ ] 说明了使用方法
- [ ] 添加了实际示例
- [ ] instructions.md 清晰具体
- [ ] 删除了所有模板占位符
- [ ] 检查了拼写和格式

## 需要帮助？

- 查看 [example-skill](../example-skill/) 了解实际示例
- 阅读 [Skill 开发规范](../../docs/skill-guidelines.md)
- 查看 [上传指南](../../docs/how-to-upload.md)

---

祝你创建出优秀的 Skill！🎉
