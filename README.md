# BrownDustHelper

独立 BepInEx 游戏内当前可见 Spine UI 资源导出工具。二进制审核候选，不公开源代码。

## 安装与使用

先自行取得并安装与你游戏版本兼容且获授权使用的 BepInEx；本包不包含加载器或游戏 DLL。
将本目录的 BepInEx 文件夹合并到游戏目录。插件位置是
`BepInEx/plugins/BrownDustHelper/BrownDustHelper.dll`。
打开角色皮肤展示页，按 F9。快捷键可在 BepInEx 配置中更改；旧单独 F8 绑定会迁移到 F9。
输出位于插件目录的 `exports/<批次>/<资源ID>/`，包含当前骨骼、图集、贴图和来源说明；
失败目录以 `.partial` 结尾。卸载时移走本工具 DLL，保留需要的个人导出文件。

导出的是当前实际加载资源，其他插件替换后可能导出其素材，不保证原皮或全部游戏资源。
Helper 不加载 MOD，不安装 Harmony 补丁；游戏运行兼容性、共存和导出颜色仍需实际验证。
使用或传播导出结果前必须另行确认内容权利。

使用边界见 [DISCLAIMER.md](DISCLAIMER.md)，许可见 [LICENSE.txt](LICENSE.txt)，
依赖见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)，隐私见 [PRIVACY.md](PRIVACY.md)。
当前未经 Windows 代码签名；校验和仅用于完整性比对，不是安全或版权认证。
