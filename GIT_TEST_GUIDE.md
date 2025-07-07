# Git 协作测试指南

## 📋 测试目标
通过实际操作熟悉 Git 团队协作流程，包括克隆、分支管理、提交和推送等基本操作。

## 🚀 开始之前

### 前置条件
- [x] 已安装 Git
- [x] 已有 GitHub 账号
- [x] 已被添加为项目协作者

### 检查 Git 配置
```bash
# 检查用户名和邮箱配置
git config --global user.name
git config --global user.email

# 如果没有配置，请设置：
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱@example.com"
```

## 📦 步骤1：克隆项目

```bash
# 1. 选择一个工作目录
cd ~/Desktop  # 或者你想要的任何目录

# 2. 克隆项目
git clone https://github.com/XueFengLH/git_group_test.git

# 3. 进入项目目录
cd git_group_test

# 4. 查看项目结构
ls -la
```

## 🌿 步骤2：创建个人分支

```bash
# 1. 查看当前分支
git branch -a

# 2. 确保在主分支
git checkout main

# 3. 获取最新代码
git pull origin main

# 4. 创建你的个人分支（请用你的名字替换 yourname）
git checkout -b yourname-dev

# 例如：git checkout -b zhangsan-dev
```

## ✏️ 步骤3：进行测试修改

### 选项A：修改 README.md
在 `README.md` 的"团队成员"部分添加你的信息：

```markdown
## 团队成员
- hance - 参与日期：2025年7月7日
- 你的名字 - 参与日期：2025年7月7日  <!-- 添加这一行 -->
```

### 选项B：实现一个简单函数
在 `group_test.py` 中选择一个函数来实现，例如：

```python
# 实现加法函数
def add(a, b):
    return a + b  # 将 return x 改为 return a + b
```

### 选项C：创建个人测试文件
创建一个以你名字命名的文件：

```bash
# 创建个人测试文件
echo "这是 [你的名字] 的测试文件" > yourname_test.txt
```

## 📝 步骤4：提交更改

```bash
# 1. 查看修改状态
git status

# 2. 查看具体修改内容
git diff

# 3. 添加文件到暂存区
git add .
# 或者指定特定文件：git add README.md

# 4. 提交更改
git commit -m "测试提交：[你的名字] 加入项目协作测试"

# 5. 查看提交历史
git log --oneline -3
```

## 🔄 步骤5：推送到远程仓库

```bash
# 推送你的分支到远程仓库
git push origin yourname-dev

# 第一次推送可能需要设置上游分支：
# git push --set-upstream origin yourname-dev
```

## 🔀 步骤6：创建 Pull Request（可选）

1. 访问项目页面：https://github.com/XueFengLH/git_group_test
2. 会看到提示创建 Pull Request 的横幅
3. 点击 "Compare & pull request"
4. 填写 Pull Request 描述：
   ```
   测试PR：[你的名字] 的协作测试
   
   ## 修改内容
   - [ ] 更新了 README.md
   - [ ] 实现了某个函数
   - [ ] 创建了测试文件
   
   ## 测试说明
   这是团队协作的测试提交，验证 Git 工作流程。
   ```
5. 点击 "Create pull request"

## 🔍 步骤7：验证和清理

```bash
# 查看所有分支
git branch -a

# 切换回主分支
git checkout main

# 更新主分支（获取其他人的提交）
git pull origin main

# 删除本地的测试分支（可选）
# git branch -d yourname-dev
```

## 🛠️ 常用命令速查

| 命令 | 说明 |
|------|------|
| `git status` | 查看工作区状态 |
| `git diff` | 查看修改内容 |
| `git add .` | 添加所有修改到暂存区 |
| `git commit -m "message"` | 提交更改 |
| `git push origin branch-name` | 推送到远程分支 |
| `git pull origin main` | 拉取主分支最新代码 |
| `git branch` | 查看本地分支 |
| `git checkout branch-name` | 切换分支 |
| `git log --oneline` | 查看提交历史 |

## 🚨 注意事项

1. **分支命名**：请使用 `yourname-dev` 格式，方便识别
2. **提交信息**：写清楚修改内容，便于团队了解
3. **冲突处理**：如果遇到冲突，先 `git pull` 获取最新代码
4. **文件操作**：不要修改他人的个人文件
5. **测试完成**：记得在群里报告测试完成状态

## 📞 需要帮助？

如果遇到问题，可以：
1. 查看错误信息并搜索解决方案
2. 在群里询问
3. 参考 Git 官方文档：https://git-scm.com/doc

## ✅ 测试完成检查清单

- [ ] 成功克隆项目
- [ ] 创建了个人分支
- [ ] 进行了测试修改
- [ ] 成功提交到本地仓库
- [ ] 推送到远程仓库
- [ ] （可选）创建了 Pull Request
- [ ] 在群里报告测试完成

---

**祝测试顺利！** 🎉

_如有问题，随时在群里交流讨论。_
