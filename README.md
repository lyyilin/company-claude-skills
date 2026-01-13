# XSCM Claude Skills Library 🚀

欢迎来到 XSCM 公司的 Claude Skills 共享仓库！

## 📚 关于本仓库

这是 XSCM 团队成员分享优秀 Claude Skills 的地方。发现好用的 Skill？上传到这里，让全公司都能使用！

## 🎯 快速开始

### 使用现有 Skill

1. 浏览 [`skills/`](./skills/) 目录查看所有可用技能
2. 阅读技能的 `SKILL.md` 了解功能和用法
3. 将技能目录复制到你的项目的 `.claude/skills/` 目录下
4. 开始使用！

### 上传你的 Skill

#### 使用 skill-uploader（推荐）

我们提供了自动上传工具，一句话搞定：

```
打包 [你的skill路径] 上传到 GitHub 仓库
```

**首次使用准备：**

1. 克隆本仓库到本地
   ```bash
   git clone https://github.com/lyyilin/company-claude-skills.git
   ```

2. 配置 Git
   ```bash
   cd company-claude-skills
   git config user.name "你的名字"
   git config user.email "你的邮箱"
   ```

3. 在 Claude 中使用 skill-uploader
   - 说："打包 [你的skill路径] 上传到 GitHub 仓库"
   - 首次使用时提供仓库路径
   - 之后就可以直接使用了！

详细说明请查看 [skill-uploader](./skills/skill-uploader/)

#### 手动上传

如果你熟悉 Git，也可以手动操作：

```bash
# 1. 拉取最新代码
git pull origin main

# 2. 复制你的 skill 到 skills/ 目录
cp -r /path/to/your-skill skills/

# 3. 提交并推送
git add skills/your-skill/
git commit -m "Add: your-skill - 简短描述"
git push origin main
```

## 🌟 可用技能列表

### 工具类

- **[skill-uploader](./skills/skill-uploader/)** - 自动上传 Skills 到本仓库的工具

> 💡 更多优秀 Skills 等你来分享！

## 📝 Skill 基本结构

一个标准的 Skill 至少应该包含：

```
your-skill/
├── SKILL.md           # 技能说明文档
└── instructions.md    # 技能指令
```

**SKILL.md 应包含：**
- 功能描述
- 使用方法
- 使用示例

## 💬 获取帮助

如果你有任何问题：
- 📝 创建 Issue 讨论
- 🗣️ 联系仓库维护者
- 💡 在团队群里提问

## 📜 许可证

XSCM 公司内部使用

---

**Happy Sharing! 🎉**

让我们一起打造 XSCM 最强大的 Skills 库！
