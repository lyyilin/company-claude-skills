# 贡献指南

感谢你为 Company Claude Skills Library 做出贡献！本文档将指导你如何向仓库提交你的技能。

## 📋 目录

- [开始之前](#开始之前)
- [提交流程](#提交流程)
- [Skill 结构要求](#skill-结构要求)
- [命名规范](#命名规范)
- [文档标准](#文档标准)
- [代码审查](#代码审查)

## 🚀 开始之前

在提交你的 Skill 之前，请确保：

1. ✅ 你的 Skill 已经过充分测试
2. ✅ 遵循了 [Skill 开发规范](./docs/skill-guidelines.md)
3. ✅ 提供了完整的文档
4. ✅ 使用了清晰的命名
5. ✅ 没有包含敏感信息（API 密钥、密码等）

## 🔄 提交流程

### 方法 1：使用 Pull Request（推荐）

1. **Fork 本仓库**
   ```bash
   # 在 GitHub 上点击 Fork 按钮
   ```

2. **克隆你的 Fork**
   ```bash
   git clone https://github.com/your-username/company-claude-skills.git
   cd company-claude-skills
   ```

3. **创建新分支**
   ```bash
   git checkout -b add-my-skill-name
   ```

4. **添加你的 Skill**
   - 在 `skills/` 目录下创建新文件夹
   - 使用 `skills/_template/` 作为起点
   - 按照规范填写所有必需文件

5. **提交更改**
   ```bash
   git add skills/your-skill-name/
   git commit -m "Add: your-skill-name - 简短描述"
   git push origin add-my-skill-name
   ```

6. **创建 Pull Request**
   - 在 GitHub 上打开你的 Fork
   - 点击 "New Pull Request"
   - 填写 PR 描述模板
   - 等待审查

### 方法 2：直接提交（需要权限）

如果你有直接提交权限：

```bash
git checkout -b add-my-skill-name
# 添加你的 skill
git add skills/your-skill-name/
git commit -m "Add: your-skill-name - 简短描述"
git push origin add-my-skill-name
# 创建 Pull Request 进行审查
```

## 📁 Skill 结构要求

每个 Skill 必须包含以下文件：

```
skills/your-skill-name/
├── SKILL.md              # 必需：技能说明文档
├── instructions.md       # 必需：技能指令
└── README.md            # 可选：额外说明
```

### SKILL.md 格式

```markdown
---
name: your-skill-name
description: 简短描述你的技能功能
version: 1.0.0
author: 你的名字
created: 2026-01-13
---

# Skill 名称

## 功能描述
详细描述你的技能做什么...

## 使用场景
什么时候应该使用这个技能...

## 使用方法
如何使用这个技能...

## 配置说明
如果有配置项，在这里说明...

## 示例
提供使用示例...
```

### instructions.md 格式

```markdown
# 技能指令

这里是给 Claude 的具体指令...
```

## 🏷️ 命名规范

### Skill 目录命名

- 使用小写字母
- 使用连字符分隔单词
- 使用描述性名称
- 避免使用缩写

**✅ 好的命名：**
- `pdf-analyzer`
- `code-reviewer`
- `meeting-summarizer`

**❌ 不好的命名：**
- `MySkill`
- `skill1`
- `pdfAnalyzer`
- `pdf_analyzer`

### Commit 消息规范

使用以下格式：

```
<类型>: <简短描述>

<详细描述>（可选）
```

**类型：**
- `Add`: 添加新 Skill
- `Update`: 更新现有 Skill
- `Fix`: 修复 Bug
- `Docs`: 文档更新
- `Refactor`: 重构

**示例：**
```
Add: pdf-analyzer - 添加 PDF 分析技能

这个技能可以分析 PDF 文档并提取关键信息。
支持多种 PDF 格式，包括扫描版和文本版。
```

## 📝 文档标准

### 必需文档

1. **SKILL.md**
   - 清晰的功能描述
   - 使用场景说明
   - 详细的使用方法
   - 配置说明（如果适用）
   - 实际使用示例

2. **instructions.md**
   - 完整的 Claude 指令
   - 清晰的逻辑结构
   - 必要的上下文说明

### 文档质量要求

- ✅ 使用清晰、简洁的语言
- ✅ 提供实际的使用示例
- ✅ 说明限制和注意事项
- ✅ 使用 Markdown 格式化
- ✅ 检查拼写和语法

## 🔍 代码审查

所有提交都需要经过审查。审查者会检查：

### 功能性
- ✅ Skill 是否按预期工作
- ✅ 是否有明显的 Bug
- ✅ 是否处理了边界情况

### 文档质量
- ✅ 文档是否完整
- ✅ 说明是否清晰
- ✅ 示例是否有效

### 代码质量
- ✅ 是否遵循命名规范
- ✅ 结构是否合理
- ✅ 是否包含敏感信息

### 可维护性
- ✅ 代码是否易于理解
- ✅ 是否有足够的注释
- ✅ 是否易于修改和扩展

## 🎯 最佳实践

1. **从模板开始**
   - 使用 `skills/_template/` 作为起点
   - 保持一致的结构

2. **充分测试**
   - 在多个场景下测试你的 Skill
   - 确保边界情况被处理

3. **清晰文档**
   - 假设用户不了解你的 Skill
   - 提供足够的上下文和示例

4. **及时更新**
   - 当你改进 Skill 时更新文档
   - 使用版本号跟踪变更

5. **响应反馈**
   - 及时回复 PR 评论
   - 根据反馈改进你的 Skill

## ❓ 常见问题

### Q: 我的 Skill 需要外部依赖怎么办？
A: 在 `SKILL.md` 中明确说明所有依赖，并提供安装指南。

### Q: 可以更新别人的 Skill 吗？
A: 可以！提交 PR 并说明你的改进。

### Q: Skill 出现 Bug 怎么办？
A: 创建 Issue 报告问题，或直接提交修复的 PR。

### Q: 如何删除一个 Skill？
A: 创建 PR 并说明删除原因，需要经过审查。

## 📞 获取帮助

如果你有任何问题：
- 📝 创建 Issue
- 💬 在 PR 中提问
- 🗣️ 联系仓库维护者

---

感谢你的贡献！🎉
