# EmboSceneExplorer: Embodied Scene Explorer for Multimodal Perception and Navigation

一个用于多模态感知和导航的具身场景探索综合框架。

## 🌐 在线演示

访问我们的项目主页：[https://EmboSceneExplorer.github.io/](https://EmboSceneExplorer.github.io/)

## 📖 项目简介

EmboSceneExplorer 是一个基于 Habitat 仿真环境构建的综合性多模态场景感知、理解和导航系统。它使具身 AI 智能体能够在虚拟 3D 场景（如 ScanNet）中执行 3D 感知和重建、基于 LLM 的定位以及目标导向的导航。

## ✨ 核心特性

- 🌐 **完整闭环系统** - 从感知到行动的完整管道
- 📹 **用户视频支持** - 支持用户拍摄的视频作为输入
- 🤖 **多智能体交互** - 初步的多智能体交互和语言对齐能力
- 🎯 **最先进的定位** - 在 3D 视觉定位方面达到最先进的性能
- 🌍 **真实世界验证** - 在多个公共真实世界场景数据集上验证
- 🗣️ **双语支持** - 支持中英文自然语言指令

## 🚀 GitHub Pages 部署指南

### 方法 1: 使用现有仓库部署

1. **Fork 或创建仓库**
   ```bash
   # 如果你有现有代码，创建新仓库
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/EmboSceneExplorer.git
   git push -u origin main
   ```

2. **启用 GitHub Pages**
   - 进入你的 GitHub 仓库
   - 点击 "Settings" 选项卡
   - 滚动到 "Pages" 部分
   - 在 "Source" 下选择 "Deploy from a branch"
   - 选择 "main" 分支和 "/ (root)" 文件夹
   - 点击 "Save"

3. **访问你的网站**
   - 几分钟后，你的网站将在 `https://YOUR_USERNAME.github.io/EmboSceneExplorer/` 可用
   - 如果你想使用自定义域名 `https://EmboSceneExplorer.github.io/`，你需要将仓库名称设置为 `EmboSceneExplorer.github.io`

### 方法 2: 使用 GitHub Actions 自动部署

1. **创建 GitHub Actions 工作流**（可选，用于更高级的部署）
   - 在仓库根目录创建 `.github/workflows/deploy.yml`
   - 配置自动化部署流程

### 重要注意事项

- 确保所有资源路径使用相对路径
- 大型视频文件可能需要使用 Git LFS 或外部托管
- GitHub Pages 有 1GB 的仓库大小限制

## 📁 项目结构

```
.
├── index.html          # 主页面
├── css/                # 样式文件
│   ├── bulma.min.css
│   ├── index.css
│   └── ...
├── js/                 # JavaScript 文件
│   ├── jquery.min.js
│   ├── index.js
│   └── ...
├── images/             # 图片资源
│   ├── logo.png
│   └── demov2.jpg
├── videos/             # 演示视频
│   └── demov4.mp4
└── README.md           # 项目说明
```

## 🛠️ 本地开发

1. **克隆仓库**
   ```bash
   git clone https://github.com/YOUR_USERNAME/EmboSceneExplorer.git
   cd EmboSceneExplorer
   ```

2. **启动本地服务器**
   ```bash
   # 使用 Python
   python -m http.server 8000
   
   # 或使用 Node.js
   npx serve .
   
   # 或使用 PHP
   php -S localhost:8000
   ```

3. **访问本地网站**
   - 打开浏览器访问 `http://localhost:8000`

## 📝 引用

如果您觉得我们的工作有用，请考虑引用：

```bibtex
@misc{embosceneexplorer2024,
  title={EmboSceneExplorer: Embodied Scene Explorer for Multimodal Perception and Navigation},
  author={Ao Gao, Luosong Guo, Chaoyang Li, Jiangming Shi, Zilong Xie, Jingyu Gong, Xin Tan, Zhizhong Zhang and Yuan Xie},
  year={2025},
  url={https://github.com/ECNU-AILab-SII/EmboSceneExplorer}
}
```

## 👥 团队

### 代码贡献者
- [Ao Gao](https://github.com/Yuhuoo)
- [Luosong Guo](https://max-luo-song.github.io/gls2000.github.io)
- [Chaoyang Li](https://github.com/GiIfoyle)
- [Jiangming Shi](https://shijiangming1.github.io/)
- [Zilong Xie](https://github.com/XieZilongAI)

### 指导老师
- [Jingyu Gong](https://jingyugong.github.io/)
- [Xin Tan](https://tanxincs.github.io/)
- [Zhizhong Zhang](https://faculty.ecnu.edu.cn/_s16/zzz2/main.psp)
- [Yuan Xie](https://faculty.ecnu.edu.cn/_s16/xy2_11342/main.psp) (项目负责人)

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🤝 贡献

欢迎贡献！请随时提交 Pull Request。

## 📞 联系我们

如有问题或建议，请通过以下方式联系我们：
- 创建 [GitHub Issue](https://github.com/ECNU-AILab-SII/EmboSceneExplorer/issues)
- 发送邮件给项目负责人

---

**EmboSceneExplorer** - 由 EmboSceneExplorer 团队用 ❤️ 构建。