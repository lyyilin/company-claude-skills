---
name: example-skill
description: 一个简单的示例技能，展示基本结构和最佳实践
version: 1.0.0
author: Company Skills Team
created: 2026-01-13
updated: 2026-01-13
tags:
  - example
  - tutorial
  - beginner
dependencies: []
---

# 示例技能 (Example Skill)

## 功能描述

这是一个示例技能，用于演示如何创建和组织 Claude Skill。它展示了：
- 标准的目录结构
- 完整的文档格式
- 清晰的指令编写
- 实用的示例

**主要功能：**
- 演示 Skill 的基本结构
- 提供文档编写范例
- 展示最佳实践

## 使用场景

这个示例 Skill 适用于：

1. **学习参考**：新手学习如何创建 Skill
2. **模板基础**：作为创建新 Skill 的参考
3. **规范示例**：展示符合规范的 Skill 结构

## 使用方法

### 基本用法

这个示例 Skill 主要用于参考，不需要实际运行。你可以：

1. 查看文件结构
2. 阅读文档格式
3. 学习最佳实践
4. 复制作为模板

### 作为模板使用

```bash
# 复制示例作为新 Skill 的起点
cp -r skills/example-skill skills/your-new-skill

# 修改文件内容
cd skills/your-new-skill
# 编辑 SKILL.md 和 instructions.md
```

## 配置说明

本示例 Skill 无需配置。

在实际的 Skill 中，如果有配置项，应该这样说明：

| 配置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| max_length | number | 1000 | 最大处理长度 |
| format | string | "markdown" | 输出格式 |
| verbose | boolean | false | 是否显示详细信息 |

## 示例

### 示例 1：查看文件结构

**操作：**
```bash
ls -la skills/example-skill/
```

**输出：**
```
SKILL.md           # 主要说明文档
instructions.md    # 技能指令
```

### 示例 2：阅读文档

**操作：**
打开 `SKILL.md` 查看完整的文档结构

**学习要点：**
- YAML frontmatter 的格式
- 各个章节的组织方式
- 示例的编写方法

## 文件说明

### SKILL.md
主要的说明文档，包含：
- 元数据（YAML frontmatter）
- 功能描述
- 使用场景
- 使用方法
- 配置说明
- 示例
- 限制和注意事项

### instructions.md
给 Claude 的具体指令，包含：
- 目标说明
- 工作流程
- 具体指令
- 输出格式

## 限制和注意事项

关于这个示例 Skill：

- ℹ️ 这是一个演示性质的 Skill，不执行实际功能
- 💡 主要用于学习和参考
- 📖 建议结合 [Skill 开发规范](../../docs/skill-guidelines.md) 一起阅读

在实际的 Skill 中，应该说明：
- ⚠️ 已知的限制
- ⚠️ 不支持的功能
- 💡 使用注意事项
- 💡 性能考虑

## 最佳实践

从这个示例中可以学到：

1. **清晰的结构**
   - 使用标准的目录结构
   - 文件命名规范
   - 逻辑组织合理

2. **完整的文档**
   - 包含所有必需章节
   - 提供实际示例
   - 说明限制和注意事项

3. **用户友好**
   - 语言清晰简洁
   - 提供足够的上下文
   - 易于理解和使用

## 更新日志

### v1.0.0 (2026-01-13)
- 初始版本
- 创建基本结构
- 添加完整文档

## 贡献者

- Company Skills Team - 初始开发

## 相关资源

- [Skill 模板](../_template/) - 快速开始的模板
- [开发规范](../../docs/skill-guidelines.md) - 详细的开发标准
- [上传指南](../../docs/how-to-upload.md) - 如何上传你的 Skill

## 许可证

公司内部使用

---

💡 **提示**：这个示例展示了一个完整、规范的 Skill 应该包含的所有元素。创建你自己的 Skill 时，可以参考这个结构！
