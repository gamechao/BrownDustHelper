# BrownDustHelper

BrownDustHelper 是游戏内素材导出工具，需要与 [ModStudio](https://github.com/gamechao/ModStudio) 配合使用：先在游戏内导出当前页面的素材，再到 ModStudio 中导入、预览和编辑。

BrownDustHelper is an in-game asset export plugin designed to work with [ModStudio](https://github.com/gamechao/ModStudio). Export assets from the current game screen, then import, preview, and edit them in ModStudio.

本仓库提供二进制程序及使用说明，不公开源代码。工具仅供学习、研究和技术交流使用。

This repository distributes binaries and documentation only; source code is not published. The tool is intended for learning, research, and technical exchange.

## 下载 / Downloads

- [BrownDustHelper v1.0.1 — 下载 / Download ZIP](https://github.com/gamechao/BrownDustHelper/releases/download/v1.0.1/BrownDustHelper.zip)
- [配套工具 / Companion tool: ModStudio v1.0.0 — 下载 / Download ZIP](https://github.com/gamechao/ModStudio/releases/download/v1.0.0/ModStudio.zip)
- [SHA-256 校验和 / Checksums](https://github.com/gamechao/BrownDustHelper/releases/download/v1.0.1/SHA256SUMS.txt)

下载后先解压。BrownDustHelper 是游戏插件，不能作为独立桌面程序启动。

Extract the ZIP before installation. BrownDustHelper runs inside the game and is not a standalone desktop application.

## 安装 / Installation

| 步骤 / Step | 中文 | English |
|---|---|---|
| 1 | 自行安装与你的游戏版本兼容的 BepInEx。 | Install a version of BepInEx compatible with your game. |
| 2 | 将解压目录中的 `BepInEx` 文件夹合并到游戏目录。 | Merge the extracted `BepInEx` folder into the game directory. |
| 3 | 确认插件位于下方路径，然后启动游戏。 | Confirm the plugin is at the path below, then start the game. |

```text
BepInEx/plugins/BrownDustHelper/BrownDustHelper.dll
```

本包不包含 BepInEx 加载器或游戏客户端。升级时替换本工具 DLL；卸载时移走该 DLL，保留需要的个人导出文件。

The package does not include BepInEx or the game client. To update, replace the plugin DLL. To uninstall, remove that DLL and keep any exported files you need.

## 配合使用 / Using Both Tools Together

**BrownDustHelper 游戏内导出 → ModStudio 导入、预览、编辑和导出 MOD。**

**Export in-game with BrownDustHelper → import, preview, edit, and export MODs with ModStudio.**

下方保留界面中的中文按钮名称，括号内为英文释义。

Chinese button labels below match the application UI; English translations are provided for reference.

| 步骤 / Step | 中文 | English |
|---|---|---|
| 1 | 在游戏中打开需要制作的角色皮肤展示页。 | Open the character costume display screen in the game. |
| 2 | 按 **F9** 导出当前加载、可见的 Spine UI 素材。 | Press **F9** to export the currently loaded, visible Spine UI assets. |
| 3 | 在下方导出目录中找到对应资源文件夹。 | Find the resource folder under the export directory below. |
| 4 | 启动 ModStudio，点击 **“打开 MOD 编辑器”**。 | Start ModStudio and click **“打开 MOD 编辑器” (Open MOD Editor)**. |
| 5 | 选择 MOD 工作目录，使用 **“导入素材制作 MOD”** 或 **“导入游戏导出”**，选择导出的资源文件夹。 | Select a MOD working directory, then choose **“导入素材制作 MOD” (Create MOD from Assets)** or **“导入游戏导出” (Import Game Export)** and select the exported resource folder. |
| 6 | 在 ModStudio 中完成预览、贴图修改、保存和 MOD 导出。 | Preview the assets, edit textures, save your work, and export the MOD in ModStudio. |

导出目录位于游戏目录内，包含骨骼、图集、贴图和来源说明。

The export directory is inside the game directory and contains skeleton data, atlases, textures, and source information.

```text
BepInEx/plugins/BrownDustHelper/exports/<batch>/<resource-id>/
```

BrownDustHelper 本身不加载或启用 MOD；编辑后的 MOD 要在游戏中生效，还需要兼容的 MOD 加载插件。

BrownDustHelper does not load or enable MODs. A compatible MOD loader is also required to use edited MODs in the game.

## 快捷键与导出说明 / Hotkey and Export Notes

快捷键可在 BepInEx 配置中更改；旧版单独 F8 绑定会迁移为 F9。导出失败的目录以 `.partial` 结尾，请勿将不完整结果作为完整素材导入。

You can change the hotkey in the BepInEx configuration. A legacy F8-only binding is migrated to F9. Failed exports have a `.partial` directory suffix; do not import incomplete exports as complete assets.

导出的是当前实际加载的资源。如果其他插件已替换立绘，导出结果可能包含替换素材；不保证还原原皮或导出全部游戏资源。Helper 不安装 Harmony 补丁，游戏更新后仍需检查兼容性和导出结果。

Exports reflect the assets currently loaded in the game. If another plugin has replaced the artwork, the export may contain those replacements. Original artwork recovery and complete game asset export are not guaranteed. Helper installs no Harmony patches; check compatibility and export results after game updates.

## 使用说明与许可 / Usage and Licensing

使用或传播导出结果前，请确认你具有相应权利，并先备份相关文件。软件未经 Windows 代码签名，校验和仅用于完整性比对。

Before using or sharing exported content, ensure you have the necessary rights and back up your files. The software is not Windows code-signed. Checksums verify file integrity only.

详见 / See: [使用许可 / License](LICENSE.txt)、[第三方声明 / Third-Party Notice](THIRD_PARTY_NOTICES.md)、[免责声明 / Disclaimer](DISCLAIMER.md)、[隐私说明 / Privacy](PRIVACY.md)。

## ❤️ 支持项目 / Support the Project

如果这些工具对你有帮助，欢迎通过以下链接支持后续开发与维护。

If you find these tools useful, you can support their continued development and maintenance here:

- [Ko-fi](https://ko-fi.com/gamechao)
- [爱发电 / Afdian](https://ifdian.net/a/Gamechao)

## 🧰 社区与相关作品 / Community & Related Projects

- [BD2ModManager — bruhnn](https://github.com/bruhnn/BD2ModManager)  
  该工具的 MOD 预览功能比本项目的 ModStudio 更强大。如果你只需要 MOD 预览，可以优先使用 bruhnn 的工具。  
  This tool offers more powerful MOD preview features than our ModStudio. If you only need MOD previews, consider using bruhnn's tool.

- [BD2 Live2D Viewer — jelosus2](https://jelosus2.github.io/BD2-L2D-Viewer/)  
  用于预览角色动画的网页工具。  
  A web-based viewer for character animations.

- [BDroid_X — Ark-Repoleved](https://github.com/Ark-Repoleved/BDroid_X)  
  Android 平台的 Brown Dust II MOD 管理工具。  
  A Brown Dust II MOD manager for Android.

