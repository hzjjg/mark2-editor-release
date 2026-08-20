# Mark2

Mark2 是一款所见即所得的 Markdown 编辑器。本仓库用于发布 macOS 安装包。

[English](README.md)

本仓库只发布 macOS 安装包和更新所需文件，不包含 Mark2 源代码。

## 下载

打开[最新版本](https://github.com/hzjjg/mark2-editor-release/releases/latest)，根据 Mac 芯片类型下载对应的 `.dmg` 文件：

| Mac 类型 | 文件 |
| --- | --- |
| Apple 芯片（M1/M2/M3/M4） | `mark2_<version>_aarch64.dmg` |
| Intel 芯片 | `mark2_<version>_x64.dmg` |

手动安装只需要下载 `.dmg`。`.app.tar.gz`、`.app.tar.gz.sig` 和 `latest.json` 供应用内更新使用。

## macOS 安装教程

当前版本尚未使用 Apple Developer ID 完成签名和公证。首次打开 Mark2 时，macOS 可能显示安全提示。

1. 从[最新版本](https://github.com/hzjjg/mark2-editor-release/releases/latest)下载与你的 Mac 芯片匹配的 `.dmg` 文件。
2. 打开 DMG，将 **mark2** 拖入 **应用程序（Applications）** 文件夹。
3. 在 **应用程序（Applications）** 中右键点击 **mark2**，选择“打开”，然后确认“打开”。
4. 如果 macOS 拦截应用，先尝试打开一次，然后进入 **系统设置 → 隐私与安全性 → 仍要打开**。

如果仍然无法打开，并且你已确认安装包来自本仓库，可在“终端”中执行：

```bash
sudo xattr -dr com.apple.quarantine /Applications/mark2.app
```

然后再次打开 **mark2**。该命令只移除这个应用的下载隔离标记。不要全局关闭 Gatekeeper。更多信息请参考 Apple 的[打开来自身份不明开发者的 Mac App](https://support.apple.com/en-ie/guide/mac-help/-mh40616/mac)指南。

## 更新应用

开启自动检查更新后，Mark2 会检查 GitHub Releases。发现新版本后，应用会在后台下载更新，并在准备完成后显示“安装更新”。点击后会自动安装更新并重启 Mark2。

也可以手动下载匹配的 `.dmg`，退出 Mark2，然后用新版本替换 **应用程序（Applications）** 中的旧版本。

## 平台支持

当前版本支持 macOS。Windows 和 Linux 安装包后续支持。
