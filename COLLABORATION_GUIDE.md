# Git 协作开发练习 Demo

## 项目结构
```
test_progress/
├── src/
│   └── TeamDemo.java
├── README.md
└── COLLABORATION_GUIDE.md
```

## 练习目标
学习如何多人并行开发同一个项目

## 基础协作流程

### 1. 克隆仓库
```bash
git clone <仓库URL>
cd test_progress
```

### 2. 创建功能分支
```bash
# 每个成员创建自己的分支
git checkout -b feature/alice-add-greeting
git checkout -b feature/bob-add-farewell
```

### 3. 开发流程
```bash
# 1. 在自己的分支上开发
git checkout feature/alice-add-greeting
# 修改代码...

# 2. 提交自己的更改
git add .
git commit -m "Alice: 添加问候功能"

# 3. 推送到远程
git push origin feature/alice-add-greeting
```

### 4. 发起 Pull Request
在 GitHub 上：
1. 进入仓库页面
2. 点击 "Pull Requests" → "New Pull Request"
3. 选择你的分支和 main/master 分支
4. 添加描述，点击创建

### 5. Code Review 和合并
1. 其他成员 Review PR
2. 确认没问题后合并到主分支
3. 删除已合并的分支

## 协作规则

### 分支命名规范
- `feature/<名字>-<功能名>`
- `bugfix/<名字>-<问题描述>`
- `hotfix/<紧急修复>`

### Commit 信息规范
- `名字: 简短描述`
- 示例: `Alice: 添加用户登录功能`

### 冲突处理
当合并时出现冲突：
1. `git checkout main` && `git pull`
2. `git checkout <你的分支>`
3. `git merge main` → 解决冲突
4. `git add .` && `git commit`
5. `git push`

## 练习任务

### 任务1: 添加再见功能
让 Bob 添加一个 farewell() 方法，输出一句告别语

### 任务2: 添加计算功能
让 Alice 添加一个简单的加法计算功能

### 任务3: 模拟冲突
两人同时修改同一行代码，练习解决冲突

## 常用命令速查
```bash
git status          # 查看状态
git branch          # 查看分支
git checkout -b    # 创建并切换分支
git merge          # 合并分支
git pull            # 拉取远程更新
git fetch           # 获取远程分支信息
```
