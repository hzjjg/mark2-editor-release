# Mark2

Binary releases for Mark2, a WYSIWYG Markdown editor for macOS.

[简体中文](README.zh-CN.md)

This repository contains release packages only. Mark2 source code is not published here.

## Download

Open the [latest release](https://github.com/hzjjg/mark2-editor-release/releases/latest) and download the `.dmg` that matches your Mac:

| Mac | File |
| --- | --- |
| Apple Silicon (M1/M2/M3/M4) | `mark2_<version>_aarch64.dmg` |
| Intel | `mark2_<version>_x64.dmg` |

The following files are used by the in-app updater and are not needed for a normal manual installation:

- `.app.tar.gz`: updater package
- `.app.tar.gz.sig`: updater signature
- `latest.json`: updater metadata

## Install on macOS

The current builds are not signed or notarized with an Apple Developer ID. macOS may therefore display a warning such as “Apple cannot check it for malicious software” or “unidentified developer” the first time you open Mark2.

1. Download the correct `.dmg` from the [latest release](https://github.com/hzjjg/mark2-editor-release/releases/latest).
2. Open the DMG and drag **Mark2** to the **Applications** folder.
3. Open **Applications**, then Control-click (or right-click) **Mark2** and choose **Open**.
4. In the confirmation dialog, choose **Open**.
5. If macOS still blocks the app, try opening it once, then go to **System Settings → Privacy & Security** and choose **Open Anyway** for Mark2. Authenticate if prompted.

You normally need to approve the app only on its first launch. Do not disable Gatekeeper globally. Only open an installer downloaded from this official release repository and from a release you trust. See Apple’s guide for [opening a Mac app from an unidentified developer](https://support.apple.com/en-ie/guide/mac-help/-mh40616/mac).

## Updating

When automatic update checking is enabled, Mark2 checks the GitHub Releases update endpoint. If a new version is found, it downloads the updater package in the background and shows an **Install update** action when the download is complete. Clicking it installs the update and restarts Mark2.

You can also update manually:

1. Download the matching `.dmg` from the latest release.
2. Quit Mark2.
3. Open the DMG and replace the existing Mark2 app in **Applications**.

## Troubleshooting

### Which package should I download?

Use `aarch64` for Apple Silicon Macs and `x64` for Intel Macs. For a normal installation, download only the `.dmg` file.

### The DMG is only a few KB

Do not install it. A valid DMG must contain the Mark2 application and should be much larger than a few KB. Use a corrected release instead.

### macOS does not show “Open Anyway”

Try launching Mark2 once from **Applications**, then return to **System Settings → Privacy & Security**. The option may only appear after macOS has blocked the app.

### Why does GitHub show “Source code (zip)” and “Source code (tar.gz)”?

GitHub automatically adds archive links for the release repository. They are snapshots of this release repository, not Mark2 application source code. They are not required for installation.

## Platform support

macOS is supported in the current release. Windows and Linux packaging are reserved for future releases.
