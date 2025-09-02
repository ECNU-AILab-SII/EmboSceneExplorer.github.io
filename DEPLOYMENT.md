# GitHub Pages 部署指南

本指南将帮助您将 EmboSceneExplorer 项目部署到 GitHub Pages，使其可以通过 `https://EmboSceneExplorer.github.io/` 访问。

## 🚀 快速部署步骤

### 1. 创建 GitHub 仓库

1. 在 GitHub 上创建一个新仓库，命名为 `EmboSceneExplorer.github.io`
   - ⚠️ **重要**: 仓库名必须是 `EmboSceneExplorer.github.io` 才能使用自定义域名
   - 如果您想使用不同的仓库名，网站将在 `https://YOUR_USERNAME.github.io/REPO_NAME/` 访问

### 2. 上传项目文件

```bash
# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 提交文件
git commit -m "Initial commit: EmboSceneExplorer website"

# 添加远程仓库
git remote add origin https://github.com/YOUR_USERNAME/EmboSceneExplorer.github.io.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入您的 GitHub 仓库
2. 点击 "Settings" 选项卡
3. 滚动到 "Pages" 部分
4. 在 "Source" 下选择 "GitHub Actions"
5. 系统会自动检测到我们提供的 GitHub Actions 工作流

### 4. 等待部署完成

- 部署通常需要 2-5 分钟
- 您可以在 "Actions" 选项卡中查看部署进度
- 部署完成后，您的网站将在 `https://EmboSceneExplorer.github.io/` 可用

## 📁 项目结构说明

```
.
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions 自动部署配置
├── css/                        # 样式文件
├── js/                         # JavaScript 文件
├── images/                     # 图片资源
├── videos/                     # 视频文件
├── index.html                  # 主页面
├── _config.yml                 # Jekyll 配置文件
├── CNAME                       # 自定义域名配置
├── robots.txt                  # 搜索引擎爬虫配置
├── sitemap.xml                 # 网站地图
├── .gitignore                  # Git 忽略文件配置
├── README.md                   # 项目说明
└── DEPLOYMENT.md               # 部署指南（本文件）
```

## 🔧 高级配置

### 自定义域名

如果您想使用自己的域名（如 `www.embosceneexplorer.com`）：

1. 修改 `CNAME` 文件，将内容改为您的域名
2. 在您的域名提供商处配置 DNS 记录：
   ```
   Type: CNAME
   Name: www (或 @)
   Value: EmboSceneExplorer.github.io
   ```

### Google Analytics

要启用 Google Analytics 跟踪：

1. 在 Google Analytics 中创建新的属性
2. 获取跟踪 ID（格式：GA_TRACKING_ID）
3. 在 `index.html` 中取消注释 Google Analytics 代码
4. 将 `GA_TRACKING_ID` 替换为您的实际跟踪 ID

### 视频文件优化

由于 GitHub 对文件大小有限制（单个文件最大 100MB，仓库总大小建议不超过 1GB）：

1. **压缩视频文件**: 使用工具如 FFmpeg 压缩视频
   ```bash
   ffmpeg -i input.mp4 -vcodec libx264 -crf 28 output.mp4
   ```

2. **使用外部托管**: 将大视频文件上传到 YouTube、Vimeo 或其他视频托管服务

3. **使用 Git LFS**: 对于大文件，可以使用 Git Large File Storage
   ```bash
   git lfs track "*.mp4"
   git add .gitattributes
   ```

## 🛠️ 本地开发

### 使用 Jekyll 本地预览

```bash
# 安装 Jekyll
gem install jekyll bundler

# 创建 Gemfile
echo 'source "https://rubygems.org"' > Gemfile
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile

# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

### 使用简单 HTTP 服务器

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

## 🔍 故障排除

### 常见问题

1. **网站无法访问**
   - 检查仓库名是否正确
   - 确认 GitHub Pages 已启用
   - 等待几分钟让部署完成

2. **样式或脚本无法加载**
   - 检查文件路径是否正确
   - 确保所有资源文件都已上传

3. **视频无法播放**
   - 检查视频文件大小是否超过限制
   - 确认视频格式兼容性

4. **自定义域名不工作**
   - 检查 CNAME 文件内容
   - 验证 DNS 配置
   - 等待 DNS 传播（可能需要 24-48 小时）

### 检查部署状态

1. 在仓库的 "Actions" 选项卡查看工作流状态
2. 在 "Settings" > "Pages" 查看部署状态
3. 检查浏览器开发者工具的控制台错误

## 📞 获取帮助

如果您遇到问题：

1. 查看 [GitHub Pages 官方文档](https://docs.github.com/en/pages)
2. 检查 [GitHub Actions 文档](https://docs.github.com/en/actions)
3. 在项目仓库创建 Issue
4. 联系项目维护者

---

**祝您部署顺利！** 🎉