# BrownDustHelper

BrownDustHelper 是游戏内素材导出工具，需要与 [ModStudio](https://github.com/gamechao/ModStudio) 配合使用：先在游戏内导出当前页面的素材，再到 ModStudio 中导入、预览和编辑。本仓库提供二进制程序及使用说明，不公开源代码。工具仅供学习、研究和技术交流使用。

## 下载

- [下载 BrownDustHelper.zip](https://github.com/gamechao/BrownDustHelper/raw/refs/heads/main/BrownDustHelper.zip)
- [下载配套 ModStudio.zip](https://github.com/gamechao/ModStudio/raw/refs/heads/main/ModStudio.zip)
- [查看压缩包 SHA-256 校验和](SHA256SUMS.txt)

下载后先解压。BrownDustHelper 是游戏插件，不能作为独立桌面程序启动。

## 安装

1. 自行安装与你的游戏版本兼容的 BepInEx。
2. 将解压目录中的 `BepInEx` 文件夹合并到游戏目录。
3. 确认插件路径为 `BepInEx/plugins/BrownDustHelper/BrownDustHelper.dll`，然后启动游戏。

本包不包含 BepInEx 加载器或游戏客户端。升级时替换本工具 DLL；卸载时移走该 DLL，保留需要的个人导出文件。

## 与 ModStudio 配合使用

1. 在游戏中打开需要制作的角色皮肤展示页。
2. 按 **F9** 导出当前加载、可见的 Spine UI 素材。
3. 在 `BepInEx/plugins/BrownDustHelper/exports/<批次>/<资源ID>/` 找到导出结果，包含骨骼、图集、贴图和来源说明。
4. 启动 ModStudio，点击 **“打开 MOD 编辑器”**。
5. 在编辑器中选择 MOD 工作目录，使用 **“导入素材制作 MOD”** 或 **“导入游戏导出”**，选择上一步的资源目录。
6. 在 ModStudio 中完成预览、贴图修改、保存和 MOD 导出。

两者分工不同：**BrownDustHelper 负责游戏内导出，ModStudio 负责桌面管理与编辑**。BrownDustHelper 本身不加载或启用 MOD；编辑后的 MOD 要在游戏中生效，还需要兼容的 MOD 加载插件。

## 快捷键与导出说明

快捷键可在 BepInEx 配置中更改；旧版单独 F8 绑定会迁移为 F9。导出失败的目录以 `.partial` 结尾，请勿将不完整结果作为完整素材导入。

导出的是当前实际加载的资源。如果其他插件已替换立绘，导出结果可能包含替换素材；不保证还原原皮或导出全部游戏资源。Helper 不安装 Harmony 补丁，游戏更新后仍需检查兼容性和导出结果。

## 使用说明与许可

使用或传播导出结果前，请确认你具有相应权利，并先备份相关文件。软件未经 Windows 代码签名，校验和仅用于完整性比对。

详见 [使用许可](LICENSE.txt)、[第三方声明](THIRD_PARTY_NOTICES.md)、[免责声明](DISCLAIMER.md) 和 [隐私说明](PRIVACY.md)。
