# Mark2

Mark2 是一款所见即所得的 Markdown 编辑器。本仓库用于发布 macOS 安装包。

[English](README.md)

本仓库只发布应用安装包和更新所需文件，不包含 Mark2 源代码。

## 下载

打开[最新版本](https://github.com/hzjjg/mark2-editor-release/releases/latest)，根据 Mac 芯片类型下载对应的 `.dmg` 文件：

| Mac 类型 | 文件 |
| --- | --- |
| Apple 芯片（M1/M2/M3/M4） | `mark2_<version>_aarch64.dmg` |
| Intel 芯片 | `mark2_<version>_x64.dmg` |

以下文件供应用内更新使用，手动安装时不需要下载：

- `.app.tar.gz`：更新包
- `.app.tar.gz.sig`：更新包签名
- `latest.json`：更新元数据

## macOS 安装教程

当前版本尚未使用 Apple Developer ID 完成签名和公证。首次打开 Mark2 时，macOS 可能提示“无法验证开发者”或“Apple 无法检查其是否包含恶意软件”。

1. 从[最新版本](https://github.com/hzjjg/mark2-editor-release/releases/latest)下载与你的 Mac 芯片匹配的 `.dmg` 文件。
2. 打开 DMG，将 **Mark2** 拖入 **应用程序（Applications）** 文件夹。
3. 打开 **应用程序（Applications）**，按住 Control 点击（或右键点击）**Mark2**，选择“打开”。
4. 在确认对话框中点击“打开”。
5. 如果 macOS 仍然拦截应用，先尝试打开一次，然后进入 **系统设置 → 隐私与安全性**，找到 Mark2 后点击“仍要打开”。如有提示，请完成身份验证。

通常只需在首次启动时执行放行操作。不要全局关闭 Gatekeeper。请确认安装包来自这个官方 release 仓库，并且你信任对应版本。更多信息请参考 Apple 的[打开来自身份不明开发者的 Mac App](https://support.apple.com/en-ie/guide/mac-help/-mh40616/mac)指南。

## 更新应用

开启自动检查更新后，Mark2 会检查 GitHub Releases 更新地址。发现新版本后，应用会在后台下载更新包；下载完成后显示“安装更新”操作。点击后会自动安装更新并重启 Mark2。

也可以手动更新：

1. 从最新版本下载与你的 Mac 芯片匹配的 `.dmg` 文件。
2. 退出 Mark2。
3. 打开 DMG，将新的 Mark2 替换到 **应用程序（Applications）** 文件夹中。

## 常见问题

### 应该下载哪个文件？

Apple 芯片 Mac 下载 `aarch64`，Intel Mac 下载 `x64`。普通安装只需要下载 `.dmg` 文件。

### 为什么 DMG 只有几 KB？

不要安装。有效的 DMG 应包含完整的 Mark2 应用，体积不会只有几 KB。请改用修正后的版本。

### 系统设置里没有“仍要打开”怎么办？

先从 **应用程序（Applications）** 启动一次 Mark2，再回到 **系统设置 → 隐私与安全性** 查看。这个选项通常会在 macOS 拦截应用后出现。

### 为什么 GitHub 还显示“Source code (zip)”和“Source code (tar.gz)”？

这是 GitHub 自动为 release 仓库生成的归档链接，内容只是本仓库的快照，不是 Mark2 应用源代码，也不需要用于安装。

## 平台支持

当前版本支持 macOS。Windows 和 Linux 的安装包暂未发布，后续会预留支持。
