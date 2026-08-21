# Mark2

Binary releases for Mark2, a WYSIWYG Markdown editor for macOS.

![screenshot-2026-08-21 13.28.10](./assets/screenshot-2026-08-21%2013.28.10.png)[简体中文](README.zh-CN.md)

This repository publishes macOS installers and updater files only. Mark2 source code is not included.

## Download

Open the [latest release](https://github.com/hzjjg/mark2-editor-release/releases/latest) and download the `.dmg` that matches your Mac:

| Mac                         | File                          |
| :-------------------------- | :---------------------------- |
| Apple Silicon (M1/M2/M3/M4) | `mark2_<version>_aarch64.dmg` |
| Intel                       | `mark2_<version>_x64.dmg`     |

For manual installation, download only the `.dmg`. The `.app.tar.gz`, `.app.tar.gz.sig`, and `latest.json` files are used by the in-app updater.

## Install on macOS

Current builds are not signed or notarized with an Apple Developer ID. macOS may show a security warning the first time you open Mark2.

1. Download the correct `.dmg` from the [latest release](https://github.com/hzjjg/mark2-editor-release/releases/latest).
2. Open the DMG and drag **mark2** to **Applications**.
3. In **Applications**, Control-click (or right-click) **mark2**, choose **Open**, then confirm **Open**.
4. If macOS blocks the app, try opening it once, then go to **System Settings → Privacy & Security → Open Anyway**.

If the app is still blocked, and you have verified that it came from this repository, run the following command in Terminal:

```bash
sudo xattr -dr com.apple.quarantine /Applications/mark2.app
```

Then open **mark2** again. This removes the downloaded-file quarantine flag for this app only. Do not disable Gatekeeper globally. See Apple’s guide for [opening a Mac app from an unidentified developer](https://support.apple.com/en-ie/guide/mac-help/-mh40616/mac).

## Updating

When automatic update checking is enabled, Mark2 checks for new GitHub Releases. It downloads the update in the background and shows an **Install update** action when ready. Clicking it installs the update and restarts Mark2.

To update manually, download the matching `.dmg`, quit Mark2, and replace the existing app in **Applications**.

## Platform support

macOS is supported in the current release. Windows and Linux packaging are reserved for future releases.
