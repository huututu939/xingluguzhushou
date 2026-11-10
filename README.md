# 星露小助手 · 发布仓库

这个仓库放五样东西：**APK 安装包**、**version.json（版本清单）**、**data/（整理数据，CC BY-NC-SA 3.0）**、**tools/（电脑端推送脚本与模组）**、**mods/（Mod 扩展包与其清单）**。
> ⚠ 2026-11-10 起本仓迁到 GitHub（原 Gitee 仓已删除）。发布物走 **Release 资产**
> 而不是 raw 文件：`raw.githubusercontent.com` 在境内不通，而 Release 资产的响应带
> `Content-Disposition: attachment`（浏览器会落盘）、下载走境内可达的 CDN、且免认证。
> 源码仓：https://github.com/huututu939/StardewHelper

它是「星露小助手」App 内「设置 → 检查更新」的数据源，以及「村民 → 扩展」的扩展包仓库，源码不在这里。

- App 读取：`https://github.com/huututu939/xingluguzhushou/releases/download/v2.151.0/version.json`
- 手动下载：Release 资产直链（永远指向最新版）`https://github.com/huututu939/xingluguzhushou/releases/download/v2.151.0/stardew-assistant_latest.apk`；或进 `apk/` 目录选带版本号的包；或 App 内点「获取更新」
- 扩展包清单：`https://github.com/huututu939/xingluguzhushou/releases/download/v2.151.0/index.json`（App 里可换成自建仓库或单包 .zip 直链）
- **电脑端模组（存档自动推送）**：`https://github.com/huututu939/xingluguzhushou/releases/download/v2.151.0/save_auto_push.zip` —— 在电脑上点这个链接直接下载（浏览器会存成 zip），解压后把 `StardewAutoPush/` 文件夹放进《星露谷物语》的 `Mods` 目录即可；需要先装 SMAPI。同一个文件在 App 内「从电脑接收 → 下载到手机」也能拿到，两边内容逐字节一致
- 联网口径：攻略与数据功能全部离线可用；App 的联网行为——每次打开 App 时静默检查一次更新（可在设置里关掉），以及你点的「检查更新」、「下载电脑脚本」、「Mod 扩展」页里的下载/刷新清单、「从电脑接收」（后者只连同一个 WiFi，不往外发数据）

星露小助手：星露谷物语攻略工具（Kotlin + Jetpack Compose，像素风）。

## 数据来源与协议

本仓**不含 App 源码** —— 源码在 [`huututu939/StardewHelper`](https://github.com/huututu939/StardewHelper)，已开源（MIT + CC BY-NC-SA 分层协议，见该仓 LICENSE）。根目录的 MIT License **覆盖 [`tools/`](./tools/) 下的电脑端脚本与电脑端模组**（都是本项目自己的作品）；`data/` 适用 CC BY-NC-SA 3.0、`apk/` 是构建产物（包内各第三方协议见 App 内「设置 → 关于 → 数据来源与协议」），三者互不覆盖 —— 范围说明见根目录 [`LICENSE`](./LICENSE)。

- 游戏数据整理自 **Stardew Valley Wiki**（[英文站](https://stardewvalleywiki.com/) / [官方简中站](https://zh.stardewvalleywiki.com/)），内容遵循 **CC BY-NC-SA 3.0**；整理后的数据以同一协议开源在本仓 [`data/`](./data/)（JSON 清单见 `data/` 目录本身，协议见 `data/LICENSE`，说明见 `data/README.md`）
- 界面字体为缝合像素字体 [Fusion Pixel Font](https://github.com/TakWolf/fusion-pixel-font)（TakWolf）的子集，以 **SIL OFL 1.1** 授权使用（子集更名为 TutuPixel，协议全文随 APK 内置）
- 底栏液态玻璃效果的算法移植自 [AndroidLiquidGlass](https://github.com/Kyant0/AndroidLiquidGlass)（Kyant），以 **Apache License 2.0** 授权使用；本项目对其着色器与效果链做了修改，协议全文随 APK 内置（App 内「设置 → 关于 → 开源与数据来源」可查看归属与全文）
- 【Stardew Valley Expanded（星露谷扩展 SVE）】扩展包的 NPC 数据与头像素材来自该 Mod——**作者: FlashShifter**，来源链接: https://www.nexusmods.com/stardewvalley/mods/3753 。按 Nexus Mods 授权条款使用并署名；本应用只读取不修改包内文件。包文件与清单见 [`mods/`](./mods/)，该 Mod 归原作者所有，本应用与其作者、ConcernedApe 均无关联
- 《星露谷物语》(Stardew Valley) 的游戏素材、名称与商标归 **ConcernedApe** 所有。本应用为**非官方粉丝工具**，与 ConcernedApe 无关联、未获其背书
- **Steam** 是 **Valve Corporation** 的注册商标，Steam 云存档功能由 Valve 提供。本应用为**非官方粉丝工具**，与 Valve / ConcernedApe 均无关联、未获其背书。「从 Steam 云获取存档」只把 Steam 官方页面交给**用户自己的浏览器**打开，账号密码由用户本人输入，本应用**不获取、不记录**；下载下来的存档只在本机本地读取解析，**不上传任何服务器、不再分发**
