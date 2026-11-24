# 在 macOS 上安装 Nearkeep

[返回 README](../README.zh-CN.md) · [English](./getting-started.md)

使用 Windows？请看 [Windows x64 下载与安装说明](./releases/v1.0.2-windows.zh-CN.md)。

## 下载前

| 项目 | 当前版本 |
| --- | --- |
| 硬件 | Apple Silicon Mac；暂无 Intel Mac 安装包 |
| macOS | 最低构建目标为 macOS 14；测试范围见 [macOS 版本说明](./releases/v1.0.2.zh-CN.md) |
| 安装包 | 内含 Nearkeep.app 和本地搜索模型；约 619 MB，另需解压空间 |
| 版本 | 1.0.2，构建 20261123.1 |
| 签名 | 临时签名；没有 Developer ID 签名或 Apple 公证 |

## 1. 下载

从[官方版本页](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.2)下载 `Nearkeep-1.0.2-macOS-arm64.zip`。

1.0.2 使用独立标签、安装包与构建标识；此前的版本说明仍可查阅。

## 2. 安装与打开

解压 ZIP，将 **Nearkeep.app** 放入“应用程序”。已有版本请先正常退出，再替换应用；保留原资料库保存文件夹。

当前应用未公证，首次打开可能被 macOS 阻止。确认安装包来自官方页面后，按 [Apple 官方说明](https://support.apple.com/en-us/102445)处理具体提示。不要关闭系统整体保护；若提示恶意软件、会损害电脑或文件损坏，请停止并反馈。

## 3. 选择文件的保存方式

全新资料状态会打开空资料库，并引导选择专用保存文件夹；取消不会开始导入。已有用户会继续使用原资料库与保存位置。

点击上传、将文件拖入资料库，或拖给桌面 Nicole，然后选择：

- **复制：**保存独立副本，保留原件。
- **移动：**安全保存成功后再移除来源。若来源包含可识别的 Nearkeep 内部记录，会保留来源并提示。
- **在设置中关联已有文件夹：**直接管理原位置文件，不导入副本。其中的改名、移动或删除会影响原件；解除关联会保留文件。

嵌套结构和空文件夹会保留。导入后，点“查看”定位本批资料，或点“完成”关闭提示。

## 日常使用与更新

- 首次使用不预设快捷键；在设置中录制或清空。窗口与快速搜索在 Nearkeep 运行时全局生效；Nicole 快捷键仅在资料库窗口前台、设置及其他弹层关闭时生效。
- 文件预览由 macOS Quick Look 提供，具体格式支持取决于系统。常见图片缩略图包括 JPEG/JPG、PNG、HEIC、TIFF、GIF、BMP、WebP；动图显示静态帧，损坏或不受支持的文件可能无法预览。临时失败会有限重试，也可手动重新加载。
- 默认保存目录会识别访达中的新增、移动与改名，大型文件夹可能有同步延迟。扫描范围及旧文件处理细节见[版本记录](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.0)。
- 通过 [Releases](https://github.com/jayueseven/Nearkeep/releases) 手动更新。更新前正常退出、备份重要资料并保留保存位置；并非所有历史版本的升级、回退组合都已验证。
- 不要同时运行多个 Nearkeep 版本；本地开发版与发行版目前共享资料身份。

[搜索与隐私说明](./search-and-privacy.zh-CN.md) · [反馈问题](https://github.com/jayueseven/Nearkeep/issues)

<details>
<summary>校验安装包（可选）</summary>

如需确认下载的文件与官方发布一致，请在下载文件夹打开终端，运行：

```sh
shasum -a 256 'Nearkeep-1.0.2-macOS-arm64.zip'
```

预期 SHA-256：

```text
a0ad6e551674a1df39c799fd3250f93462b47e71f6bba779dfa268977f8964a6
```

如果校验值不一致，请勿安装，并从官方入口重新下载。

</details>
