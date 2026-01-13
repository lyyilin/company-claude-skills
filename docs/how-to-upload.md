# 如何上传你的 Skill 到仓库

本指南将一步步教你如何将自己开发的 Claude Skill 上传到公司共享仓库。

## 📋 前置准备

在开始之前，确保你已经：

- ✅ 安装了 Git
- ✅ 配置了 GitHub 账号
- ✅ 有一个已开发完成的 Skill
- ✅ 阅读了 [Skill 开发规范](./skill-guidelines.md)

## 🚀 方法一：使用 Git 命令行（推荐）

### 步骤 1：Fork 并克隆仓库

1. **Fork 仓库**
   - 访问 `https://github.com/your-company/company-claude-skills`
   - 点击右上角的 "Fork" 按钮

2. **克隆到本地**
   ```bash
   git clone https://github.com/your-username/company-claude-skills.git
   cd company-claude-skills
   ```

### 步骤 2：创建新分支

```bash
git checkout -b add-my-skill-name
```

> 💡 **提示**：使用描述性的分支名，例如 `add-pdf-analyzer`

### 步骤 3：准备你的 Skill

1. **使用模板**
   ```bash
   cp -r skills/_template skills/your-skill-name
   ```

2. **填写 SKILL.md**
   
   编辑 `skills/your-skill-name/SKILL.md`：
   
   ```markdown
   ---
   name: your-skill-name
   description: 简短描述（一句话）
   version: 1.0.0
   author: 你的名字
   created: 2026-01-13
   ---
   
   # Skill 名称
   
   ## 功能描述
   详细说明这个 Skill 做什么...
   
   ## 使用场景
   什么时候应该使用这个 Skill...
   
   ## 使用方法
   如何使用这个 Skill...
   
   ## 示例
   提供实际的使用示例...
   ```

3. **填写 instructions.md**
   
   编辑 `skills/your-skill-name/instructions.md`：
   
   ```markdown
   # 技能指令
   
   这里是给 Claude 的具体指令...
   ```

### 步骤 4：验证你的 Skill

在提交前，请确保：

- ✅ 所有必需文件都存在
- ✅ SKILL.md 包含完整信息
- ✅ instructions.md 清晰明确
- ✅ 没有包含敏感信息
- ✅ 文件命名符合规范

### 步骤 5：提交更改

```bash
# 添加你的 skill
git add skills/your-skill-name/

# 提交
git commit -m "Add: your-skill-name - 简短描述"

# 推送到你的 Fork
git push origin add-my-skill-name
```

### 步骤 6：创建 Pull Request

1. 访问你的 Fork 页面
2. 点击 "Compare & pull request"
3. 填写 PR 描述：
   ```markdown
   ## 添加新 Skill: your-skill-name
   
   ### 功能描述
   简要说明这个 Skill 的功能...
   
   ### 使用场景
   什么时候应该使用...
   
   ### 测试情况
   - [x] 已在本地测试
   - [x] 文档完整
   - [x] 遵循命名规范
   ```
4. 点击 "Create pull request"

### 步骤 7：等待审查

- 仓库维护者会审查你的 PR
- 根据反馈进行修改（如果需要）
- PR 被合并后，你的 Skill 就可以被所有人使用了！

## 🖱️ 方法二：使用 GitHub 网页界面

如果你不熟悉 Git 命令行，可以使用网页界面：

### 步骤 1：Fork 仓库

访问仓库页面，点击 "Fork" 按钮

### 步骤 2：创建新文件夹

1. 在你的 Fork 中，进入 `skills/` 目录
2. 点击 "Add file" → "Create new file"
3. 在文件名中输入 `your-skill-name/SKILL.md`
4. 这会自动创建文件夹

### 步骤 3：添加文件内容

1. 复制模板内容到 SKILL.md
2. 填写你的 Skill 信息
3. 点击 "Commit new file"

### 步骤 4：添加其他文件

重复步骤 3，创建 `instructions.md` 和其他必需文件

### 步骤 5：创建 Pull Request

1. 回到仓库主页
2. 点击 "Contribute" → "Open pull request"
3. 填写 PR 描述
4. 提交

## 📝 Skill 文件清单

确保你的 Skill 包含以下文件：

```
skills/your-skill-name/
├── SKILL.md              ✅ 必需
├── instructions.md       ✅ 必需
└── README.md            ⭕ 可选
```

## ✅ 提交前检查清单

在提交 PR 之前，请检查：

- [ ] Skill 名称使用小写和连字符
- [ ] SKILL.md 包含所有必需字段
- [ ] instructions.md 清晰完整
- [ ] 提供了使用示例
- [ ] 没有包含敏感信息（API 密钥等）
- [ ] 测试过 Skill 可以正常工作
- [ ] Commit 消息格式正确
- [ ] PR 描述清晰

## 🔄 更新现有 Skill

如果你想更新已存在的 Skill：

```bash
# 创建新分支
git checkout -b update-skill-name

# 修改文件
# ...

# 提交
git add skills/skill-name/
git commit -m "Update: skill-name - 更新说明"
git push origin update-skill-name

# 创建 PR
```

记得在 SKILL.md 的 frontmatter 中更新版本号：

```yaml
version: 1.1.0  # 从 1.0.0 更新
```

## ❓ 常见问题

### Q: 我的 Skill 需要多个文件怎么办？

A: 可以在 Skill 目录下添加任意文件，但确保在 SKILL.md 中说明每个文件的用途。

### Q: 可以包含示例数据吗？

A: 可以！在 Skill 目录下创建 `examples/` 文件夹存放示例。

### Q: PR 被拒绝了怎么办？

A: 查看审查意见，根据反馈修改后重新提交。

### Q: 如何测试我的 Skill？

A: 在本地项目的 `.claude/skills/` 目录中测试，确保功能正常后再提交。

## 🎯 最佳实践

1. **清晰的文档**
   - 假设用户不了解你的 Skill
   - 提供足够的上下文
   - 包含实际的使用示例

2. **描述性命名**
   - 使用能说明功能的名称
   - 避免使用缩写
   - 保持简洁

3. **版本管理**
   - 使用语义化版本号（1.0.0）
   - 重大更新增加主版本号
   - 小改进增加次版本号

4. **及时响应**
   - 关注 PR 的评论
   - 及时回复问题
   - 根据反馈改进

## 📞 需要帮助？

如果你在上传过程中遇到问题：

- 📝 查看 [贡献指南](../CONTRIBUTING.md)
- 💬 在 Issue 中提问
- 🗣️ 联系仓库维护者

---

祝你上传顺利！🎉
