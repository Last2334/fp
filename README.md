# 浏览器指纹获取工具

一个基于 FingerprintJS 的浏览器指纹获取工具，可以生成唯一的浏览器标识符。

## 🌐 在线演示

访问 [GitHub Pages](https://Last2334.github.io/fp/) 查看在线演示。

## ✨ 功能特点

- 🔍 生成唯一的浏览器指纹 ID
- 📱 响应式设计，支持移动设备
- 🔒 完全本地计算，保护用户隐私
- 📊 显示详细的指纹组件信息
- 🎨 现代化的用户界面
- ⚡ 快速加载，使用 CDN 资源

## 🛠️ 技术栈

- **前端**: HTML5, CSS3, JavaScript (ES6+)
- **指纹库**: [FingerprintJS](https://fingerprintjs.com/)
- **部署**: GitHub Pages

## 📁 项目结构

```
fp/
├── docs/                   # GitHub Pages 发布目录
│   └── index.html         # 主页面
├── run_fingerprint_server.py  # 原始 FastAPI 服务器
└── README.md              # 项目说明文档
```

## 🚀 本地运行

### 方法一：直接打开 HTML 文件

1. 克隆或下载本项目
2. 直接在浏览器中打开 `docs/index.html` 文件

### 方法二：使用本地服务器（推荐）

```bash
# 使用 Python 启动简单 HTTP 服务器
cd docs
python -m http.server 8000

# 或使用 Node.js 的 http-server
npx http-server docs -p 8000
```

然后在浏览器中访问 `http://localhost:8000`

### 方法三：使用原始 FastAPI 服务器

```bash
# 安装依赖
pip install fastapi uvicorn requests

# 运行服务器
python run_fingerprint_server.py
```

然后在浏览器中访问 `http://localhost:33335`

## 📦 部署到 GitHub Pages

1. 将代码推送到 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages，选择 "GitHub Actions" 作为源
3. 保存设置后，GitHub Actions 将自动部署网站
4. 部署完成后即可访问网站

## 🔧 自定义配置

### 修改样式

编辑 `docs/index.html` 中的 CSS 部分，可以自定义：

- 颜色主题
- 字体
- 布局
- 动画效果

### 修改功能

编辑 `docs/index.html` 中的 JavaScript 部分，可以：

- 添加更多指纹组件显示
- 修改错误处理逻辑
- 添加数据导出功能
- 集成其他分析工具

## 📖 关于浏览器指纹

浏览器指纹是一种通过收集浏览器和设备的各种特征信息来生成唯一标识符的技术。这些特征包括：

- 用户代理字符串
- 屏幕分辨率和颜色深度
- 时区信息
- 安装的字体和插件
- WebGL 和 Canvas 指纹
- 音频上下文指纹
- 等等...

即使删除 Cookie，浏览器指纹通常仍然保持不变，这使得它成为一种强大的用户识别技术。

## 🔒 隐私说明

本工具仅在用户的本地浏览器中生成指纹，不会将任何数据发送到服务器。所有计算都在用户的设备上完成，确保用户隐私安全。

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这个项目！

## 📞 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 GitHub Issue
- 发送邮件至 [你的邮箱]

---

⭐ 如果这个项目对你有帮助，请给它一个星标！