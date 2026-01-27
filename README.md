

# PicList For Fedora

> 专为 Fedora 43 系统优化的 PicList 安装与配置指南。

## 📖 项目简介 | Introduction

**PicList** 是一款高效的云存储管理与图片上传工具（基于 PicGo 二次开发），支持多种图床平台。

本项目 (`piclist-Fedora`) 旨在解决在 **Fedora 43** 环境下安装和运行 PicList 可能遇到的依赖缺失、桌面图标配置及 Wayland 兼容性问题。我们提供了一套简便的脚本/指南，帮助您在 Fedora 上获得丝滑的体验。

## ✨ 特性 | Features

* ✅ **适配 Fedora 43**: 针对最新 Fedora 系统的库依赖进行测试。
* 📦 **一键安装/配置**: 提供便捷的脚本（或详细步骤）集成到系统菜单。
* 🔧 **Wayland 支持**: 修复 Electron 应用在 Wayland 下可能出现的黑屏或无法启动问题。
* 🔌 **Typora/Obsidian 集成**: 完美的 Markdown 编辑器伴侣。

---



## ⚙️ 配置与使用 | Configuration

### 配合 Typora 使用

1. 打开 Typora -> `偏好设置` -> `图像`。
2. **上传服务**选择 `PicList` (或者选择 Custom Command)。
3. **命令**填写：
```bash
/path/to/your/PicList.AppImage upload

```


4. 点击“验证图片上传选项”进行测试。

### 配合 Obsidian 使用

推荐安装 **Image Auto Upload Plugin** 插件，并在配置中连接到 PicList 的本地服务器端口（默认为 `36677`）。

---

## ❓ 常见问题 | FAQ

**Q: 在 Fedora 43 (Wayland) 下双击 AppImage 没有任何反应？**

> **A:** 这通常是沙箱权限问题。请尝试在终端运行 `./PicList.AppImage --no-sandbox`。如果在 `.desktop` 文件中，请确保 `Exec` 行包含 `--no-sandbox` 参数。

**Q: 顶部状态栏图标不显示 (Gnome)?**

> **A:** Fedora 默认的 Gnome 桌面可能不支持传统的托盘图标。您需要安装 Gnome 扩展 [AppIndicator and KStatusNotifierItem Support](https://extensions.gnome.org/extension/615/appindicator-support/)。

**Q: 无法拖拽图片上传？**

> **A:** 请检查是否以管理员权限运行了 PicList（不推荐），这会导致拖拽操作被系统拦截。请以普通用户运行。

---

## 🤝 贡献 | Contributing

欢迎提交 Issue 或 Pull Request！如果您发现 Fedora 43 更新导致了新的兼容性问题，请告诉我们。

1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request

## 📜 许可证 | License

本指南及脚本遵循 [MIT License](https://www.google.com/search?q=LICENSE)。
PicList 软件本身的版权归原作者 [Kuingsmile](https://github.com/Kuingsmile) 所有。

---

**Enjoy your writing with PicList on Fedora! 🐧**

---

### 💡 针对您项目的建议 (Next Steps)

为了让这个 README 真正生效，我建议您执行以下操作：

1. **确认内容:** 检查您仓库里具体包含什么？是一个 `.sh` 脚本，还是仅仅是文档？如果是脚本，请确保 `install.sh` 的部分是准确的。
2. **添加截图:** 在 README 中加入一张 PicList 在 Fedora 系统上运行的截图，这非常有说服力。
3. **链接:** 记得把文中 `https://github.com/your-username/piclist-Fedora.git` 替换为您真实的仓库地址。

**您希望我帮您写一个用于 Fedora 的自动安装 Shell 脚本 (`install.sh`) 放在这个仓库里吗？**
