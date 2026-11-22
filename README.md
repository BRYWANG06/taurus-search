<p align="center"><img src="Taurus-Search-Selected.png" width="120" alt="Taurus Search"></p>

# Taurus Search

免费的 macOS 菜单栏文件搜索工具。快捷键唤起，搜索文件、文件夹和应用。

**macOS 14 或更新版本 · Apple 芯片与 Intel**

## 下载与安装

从 [Releases 下载 Taurus Search](https://github.com/BRYWANG06/taurus-search/releases/latest) 中的 `Taurus Search 1.0.dmg`，打开后将 Taurus Search 拖入 Applications。

当前 1.0 使用开发签名，尚未经过 Apple 公证，首次打开可能被 macOS 拦截。也可下载 Xcode 源码包自行编译。

## 使用

- 点击菜单栏放大镜或按 **Option + Space** 打开搜索，Esc 或点击窗口外收起。
- 右键菜单栏放大镜，设置语言、快捷键、搜索位置和登录时启动。
- 首次使用选择要搜索的文件夹，或选择搜索这台 Mac；受保护目录需在系统设置中由用户授权。
- Enter 打开文件，Command + Enter 在 Finder 中显示。
- 拖动搜索框后可记住位置。

## 特点

- 原生玻璃界面，菜单栏常驻，不显示 Dock 图标。
- 应用优先显示，常见文件类型图标预先缓存。
- 文件变更自动同步索引，更新应用时保留已有索引。
- 默认搜索名称，支持简历等常用同义词；可切换仅文件名模式。
- 隐藏日志、缓存以及已识别的聊天与音乐客户端内部存储；可选择隐藏代码文件。
- 支持简体中文、繁体中文、English、日本語。

搜索覆盖已授权且本机可访问的位置。过滤只影响搜索结果，不删除文件。索引保存在本机。

## 构建

从 Releases 下载 `Taurus Search 1.0-Xcode.zip`，解压后使用 Xcode 打开 `TaurusSearchMac/TaurusSearch.xcodeproj`，选择 TaurusSearch 和 My Mac。部署目标为 macOS 14，玻璃效果在系统支持时使用原生实现。

```sh
xcodebuild -project TaurusSearchMac/TaurusSearch.xcodeproj -scheme TaurusSearch -configuration Release -derivedDataPath build ARCHS='arm64 x86_64' ONLY_ACTIVE_ARCH=NO CODE_SIGNING_ALLOWED=NO build
```

## 反馈

请在 Issues 中描述问题，并注明 macOS 版本。截图请先遮住私人文件名和路径。
