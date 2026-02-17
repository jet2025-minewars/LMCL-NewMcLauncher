# LMCL - Lightning Minecraft Launcher

<div align="center">

![LMCL Logo](assets/icons/game.png)

**轻量、快速、简洁的 Minecraft 启动器**

[![Version](https://img.shields.io/badge/version-1.1.0-blue.svg)](https://github.com/your-username/lmcl/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)](https://github.com/your-username/lmcl)
[![Electron](https://img.shields.io/badge/Electron-latest-47848F.svg)](https://www.electronjs.org/)

[下载使用](#下载安装) • [功能特性](#功能特性) • [使用文档](#使用说明) • [更新日志](#更新日志) • [问题反馈](#问题反馈)

</div>

---

## 📖 项目简介

LMCL（Lightning Minecraft Launcher）是一款专为中国玩家设计的 Minecraft 启动器，采用 Electron + Node.js 开发，提供极速下载、智能管理、简洁界面等特性。

### ✨ 为什么选择 LMCL？

- 🚀 **极速下载** - 使用 BMCLAPI 国内镜像，下载速度提升 10 倍以上
- 🎯 **简单易用** - 直观的界面设计，新手也能快速上手
- ☕ **智能 Java 管理** - 自动检测和管理 Java 环境
- 🧩 **模组下载** - 内置模组搜索和下载功能（MCIM 镜像）
- 🔐 **正版登录** - 支持微软账户正版登录
- 🎨 **现代化界面** - 精美的 UI 设计，支持自定义主题
- 📦 **轻量级** - 体积小巧，资源占用低

---

## 🎯 功能特性

### 核心功能

#### 🎮 游戏管理
- ✅ 支持原版、Fabric、Forge 版本下载
- ✅ 版本隔离，互不干扰
- ✅ 快速启动已安装版本
- ✅ 版本详细信息查看
- ✅ 一键删除和管理版本

#### ⚡ 高速下载
- ✅ 使用 BMCLAPI 国内镜像
- ✅ 多线程并发下载（库文件 20 线程，资源文件 50 线程）
- ✅ 断点续传支持
- ✅ 智能文件校验
- ✅ 资源文件预检查，只下载缺失文件

#### 🧩 模组管理
- ✅ 模组搜索和浏览
- ✅ 热门模组推荐
- ✅ 模组详情查看
- ✅ 一键下载安装
- ✅ 版本兼容性检查

#### ☕ Java 管理
- ✅ 自动检测系统 Java
- ✅ 手动添加 Java 路径
- ✅ Java 版本兼容性提示
- ✅ 内存分配设置
- ✅ JVM 参数自定义

#### 🔐 账户系统
- ✅ 离线登录（自定义用户名）
- ✅ 微软正版登录
- ✅ 账户信息保存
- ✅ 快速切换账户

#### 🎨 个性化设置
- ✅ 主题切换（浅色/深色）
- ✅ 动画效果开关
- ✅ 背景粒子效果
- ✅ 游戏窗口设置
- ✅ 下载源选择

---

## 📥 下载安装

### 系统要求

- **操作系统**: Windows 10/11（64位）
- **内存**: 至少 4GB RAM
- **存储空间**: 至少 2GB 可用空间
- **网络**: 稳定的互联网连接

### 安装步骤

1. **下载启动器**
   - 前往 [Releases](https://github.com/your-username/lmcl/releases) 页面
   - 下载最新版本的安装包（`LMCL-Setup-x.x.x.exe`）

2. **安装**
   - 双击运行安装包
   - 按照安装向导完成安装
   - 首次启动会显示欢迎界面

3. **配置 Java**
   - 启动器会自动检测系统 Java
   - 如未检测到，请前往 [Java 官网](https://www.java.com/) 下载安装
   - 或在启动器的 Java 页面手动添加 Java 路径

4. **开始游戏**
   - 前往"下载"页面选择游戏版本
   - 等待下载完成
   - 返回主页点击"启动游戏"

---

## 📚 使用说明

### 快速开始

#### 1. 下载游戏版本

```
主页 → 下载 → 游戏版本 → 选择版本 → 开始下载
```

- 支持原版、Fabric、Forge
- 自动下载所需的库文件和资源文件
- 下载进度实时显示

#### 2. 启动游戏

```
主页 → 选择版本 → 启动游戏
```

- 首次启动会进行文件校验
- 支持离线登录和正版登录
- 可自定义游戏窗口大小和内存分配

#### 3. 下载模组

```
下载 → 模组下载 → 搜索模组 → 选择版本 → 下载
```

- 使用 MCIM 国内镜像
- 支持按游戏版本筛选
- 自动安装到对应版本的 mods 文件夹

### 高级功能

#### 自定义 JVM 参数

```
设置 → 游戏设置 → JVM 参数
```

推荐参数：
```
-XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```

#### 版本隔离

每个版本都有独立的文件夹，包括：
- `mods/` - 模组文件夹
- `saves/` - 存档文件夹
- `resourcepacks/` - 资源包文件夹
- `shaderpacks/` - 光影包文件夹

#### 崩溃诊断

游戏崩溃时会自动分析崩溃原因并提供解决方案：
- 内存不足
- Java 版本不兼容
- 模组冲突
- 缺少依赖

---

## 🔄 更新日志

### v1.1.0 (2024-01-15)

#### 🎉 新增功能
- 优化下载器性能，库文件并发数提升至 20，资源文件并发数提升至 50
- 添加资源文件预检查，只下载缺失的文件
- 解决高版本（1.16+）下载速度慢的问题
- 修复 Fabric 启动时的重复类错误
- 优化启动游戏按钮，添加多层阴影和涟漪效果
- 所有 emoji 替换为自定义图标，界面更加统一美观

#### 🔧 优化改进
- 重置页面和弹窗的滚动位置和折叠状态
- 添加图标白色底衬效果，提升可读性
- 优化 Fabric 图标大小显示
- 添加全局动画开关，可在设置中关闭所有过渡动画

#### 🐛 问题修复
- 修复 CSS 兼容性警告
- 修复版本组闪烁问题
- 修复崩溃窗口滚动位置重置问题

### v1.0.5 (2024-01-10)

#### 🎉 新增功能
- 添加模组下载功能
- 支持正版登录

#### 🔧 优化改进
- 优化主页布局
- 改进下载管理器

[查看完整更新历史](版本更新历史.md)

---

## 🛠️ 技术栈

- **框架**: Electron
- **前端**: HTML5 + CSS3 + JavaScript
- **后端**: Node.js
- **下载源**: BMCLAPI（游戏文件）、MCIM（模组）
- **认证**: Microsoft OAuth 2.0

---

## 📂 项目结构

```
LMCL/
├── assets/              # 资源文件
│   └── icons/          # 图标文件
├── md/                 # 文档文件
├── main.js             # Electron 主进程
├── renderer.js         # 渲染进程逻辑
├── index.html          # 主界面
├── style.css           # 样式文件
├── minecraft-downloader.js  # 下载器
├── minecraft-launcher.js    # 启动器
├── mod-manager.js      # 模组管理器
├── microsoft-auth.js   # 微软认证
└── package.json        # 项目配置
```

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 开发环境搭建

1. **克隆仓库**
```bash
git clone https://github.com/your-username/lmcl.git
cd lmcl
```

2. **安装依赖**
```bash
npm install
```

3. **启动开发模式**
```bash
npm start
```

4. **打包应用**
```bash
npm run build
```

### 代码规范

- 使用 2 空格缩进
- 遵循 ESLint 规则
- 提交前请测试功能
- 提交信息使用中文，格式：`类型: 描述`

### 提交类型

- `新增`: 新功能
- `修复`: Bug 修复
- `优化`: 性能优化
- `文档`: 文档更新
- `样式`: 代码格式调整

---

## ❓ 常见问题

### Q: 下载速度慢怎么办？
A: 启动器默认使用 BMCLAPI 国内镜像，速度已经很快。如果仍然慢，请检查网络连接或尝试切换下载源。

### Q: 游戏启动失败？
A: 请检查：
1. Java 是否正确安装
2. 内存分配是否合理（建议至少 2GB）
3. 版本文件是否完整
4. 查看崩溃日志获取详细信息

### Q: 如何安装模组？
A: 
1. 确保已安装 Fabric 或 Forge 版本
2. 前往"下载 → 模组下载"搜索模组
3. 选择对应游戏版本下载
4. 或手动将模组文件放入版本的 mods 文件夹

### Q: 支持 macOS 和 Linux 吗？
A: 目前仅支持 Windows，未来可能会支持其他平台。

### Q: 如何更新启动器？
A: 启动器会自动检测更新并显示公告，请前往 Releases 页面下载最新版本。

---

## 📞 问题反馈

如果遇到问题或有建议，欢迎通过以下方式反馈：

- 📧 **邮箱**: your-email@example.com
- 💬 **QQ 群**: 123456789
- 🐛 **Issue**: [提交 Issue](https://github.com/your-username/lmcl/issues)
- 💡 **讨论**: [GitHub Discussions](https://github.com/your-username/lmcl/discussions)

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。

---

## 🙏 致谢

感谢以下项目和服务：

- [Electron](https://www.electronjs.org/) - 跨平台桌面应用框架
- [BMCLAPI](https://bmclapidoc.bangbang93.com/) - 提供国内镜像下载服务
- [MCIM](https://www.mcmod.cn/) - 提供模组下载服务
- [Minecraft](https://www.minecraft.net/) - 伟大的游戏

---

## 📊 统计信息

![GitHub stars](https://img.shields.io/github/stars/your-username/lmcl?style=social)
![GitHub forks](https://img.shields.io/github/forks/your-username/lmcl?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/your-username/lmcl?style=social)

---

<div align="center">

**如果这个项目对你有帮助，请给一个 ⭐ Star 支持一下！**

Made with ❤️ by [Your Name](https://github.com/your-username)

</div>
