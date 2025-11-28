# GitHub Pages 部署指南

本指南将帮助您将浏览器指纹获取工具部署到 GitHub Pages。

## 🚀 快速部署步骤

### 1. 创建 GitHub 仓库

1. 登录您的 GitHub 账户
2. 点击右上角的 "+" 号，选择 "New repository"
3. 输入仓库名称（建议：`fp` 或 `fingerprint-tool`）
4. 选择 "Public"（公开仓库）
5. 勾选 "Add a README file"（可选）
6. 点击 "Create repository"

### 2. 上传项目文件

#### 方法一：使用 GitHub 网页界面

1. 进入您创建的仓库页面
2. 点击 "Add file" → "Upload files"
3. 将以下文件拖拽到上传区域：
   - `docs/` 文件夹（包含 index.html 和 404.html）
   - `.github/workflows/deploy.yml`
   - `.gitignore`
   - `README.md`
   - `DEPLOY.md`
4. 在底部提交更改

#### 方法二：使用 Git 命令行

```bash
# 克隆您的仓库
git clone https://github.com/您的用户名/仓库名称.git
cd 仓库名称

# 复制项目文件到仓库
# （将本项目的文件复制到克隆的仓库中）

# 添加所有文件
git add .

# 提交更改
git commit -m "初始提交：浏览器指纹获取工具"

# 推送到 GitHub
git push origin main
```

### 3. 启用 GitHub Pages

1. 进入您的仓库页面
2. 点击 "Settings" 选项卡
3. 在左侧菜单中找到 "Pages"
4. 在 "Source" 部分，选择 "GitHub Actions"
5. 保存设置

### 4. 配置 GitHub Actions（自动部署）

您的仓库中已经包含了 `.github/workflows/deploy.yml` 文件，它会：

- 自动检测到 `docs/` 文件夹
- 将其部署到 GitHub Pages
- 每次推送代码时自动更新网站

### 5. 等待部署完成

1. 进入仓库的 "Actions" 选项卡
2. 查看 "Deploy to GitHub Pages" 工作流的运行状态
3. 部署完成后（通常需要几分钟），您的网站将在线

## 🌐 访问您的网站

部署完成后，您的网站将在以下地址可用：

```
https://您的用户名.github.io/仓库名称/
```

例如：`https://username.github.io/fp/`

## 🔧 故障排除

### 如果网站未显示

1. 检查 GitHub Actions 是否成功运行
2. 确认 `docs/` 文件夹包含 `index.html` 文件
3. 等待最多 10 分钟让 GitHub Pages 完成初始化

### 如果需要自定义域名

1. 在 `docs/` 文件夹中创建 `CNAME` 文件
2. 在文件中写入您的自定义域名（如：`www.yourdomain.com`）
3. 在域名提供商处配置 DNS 记录

### 如果需要更新网站

1. 修改 `docs/index.html` 或其他文件
2. 提交并推送更改到 GitHub
3. GitHub Actions 将自动重新部署

## 📱 测试网站功能

部署完成后，您可以测试以下功能：

- ✅ 浏览器指纹生成
- ✅ 重新生成功能
- ✅ 查看详细信息
- ✅ 响应式设计（在移动设备上测试）
- ✅ 错误处理

## 🎨 自定义网站

您可以修改以下文件来自定义网站：

- `docs/index.html` - 主页面内容和样式
- `docs/404.html` - 404 错误页面
- `README.md` - 项目说明文档

## 📊 监控网站访问

GitHub Pages 提供基本的访问统计：

1. 进入仓库的 "Insights" 选项卡
2. 点击 "Traffic" 查看访问统计

---

🎉 恭喜！您的浏览器指纹获取工具现在已经部署到 GitHub Pages 上了！