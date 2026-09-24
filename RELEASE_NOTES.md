# GIF Converter v0.1.1 测试版

**现在支持 Android 10 及以上的 arm64 手机。** 本次为兼容性更新，安装版本 `0.1.1`，版本代码 `7`；保留图片/视频转 GIF、GIF 编辑、压缩、分解、拼接及生成历史筛选。

[下载 Android 安装包](https://github.com/LingXia979/GIF-Converter-Releases/releases/download/v0.1.1/GIF-Converter-v0.1.1-arm64.apk) · [完整下载材料](https://github.com/LingXia979/GIF-Converter-Releases/releases/tag/v0.1.1) · [界面预览](https://github.com/LingXia979/GIF-Converter-Releases#应用界面)

**安装补充（2026-09-24）：** 若早期直接安装的内测版更新时提示“签名不一致”，请保留现有 App，使用维护者提供的原内测签名专用升级包，避免卸载丢失历史。公开 v0.1.0 与 v0.1.1 的正式证书一致；独立“兼容测试”版另用包名。请按[最新安装来源对照表](https://github.com/LingXia979/GIF-Converter-Releases/blob/main/INSTALLATION.md)选择更新方式。原发布附件与校验值保留，附件内文档是首次发布时的快照。

## 本次更新

- 最低系统由 Android 12 降至 Android 10（API 29），应用和媒体库使用一致的最低系统要求。
- FFmpeg 按 Android 10 目标重新编译，保留现有编解码能力、透明背景处理及 16 KB 对齐。
- 加强媒体库构建身份的一致性检查，避免应用与原生库使用不同的构建记录。
- 保留现有界面、图标、历史筛选、日期拖动及数据格式。
- 沿用公开 v0.1.0 的包名和正式签名，可直接覆盖更新；旧发布包继续保留。

## 安装与已有数据

下载 `GIF-Converter-v0.1.1-arm64.apk`，设备需运行 Android 10+ 和 64 位 ARM 系统。文件大小及 SHA-256 见本页附件中的 `release-manifest.json` 和 `SHA256SUMS.txt`。

**从公开 v0.1.0 更新无需卸载，正常覆盖安装保留历史和设置。** 独立的“GIF Converter 兼容测试”可与正式版并存，历史不会自动互通。更早的同包名内部调试签名版不能直接被正式版覆盖；卸载会删除应用内数据，请先另存重要 GIF、PNG 和 ZIP。具体步骤见附件 `INSTALLATION.md`。

## 测试范围

2026-09-24，两位测试者分别在 **Android 10** 和 **Android 16** 使用独立兼容测试版后反馈没有发现问题。Android 10 设备型号未提供；Android 16 为维护者设备 BKQ AN80。正式签名发布包另做签名、版本、权限、原生依赖和文件校验。

同日补充公开包真机验证：在 BKQ AN80 / Android 16 安装公开 v0.1.0，生成 1 条项目图标示例历史，再直接覆盖更新到公开 v0.1.1。安装成功、冷启动正常，示例历史保留且能预览；手机实际 APK 与 GitHub 下载文件一致。这次验证覆盖安装、启动与已有历史预览，其他功能尚未对最终正式包逐项复测。后续已安装正式签名版的用户可直接下载同通道新版 APK 更新，无需卸载；详见[最新安装说明](https://github.com/LingXia979/GIF-Converter-Releases/blob/main/INSTALLATION.md)。

Android 检查为 JVM 387 通过、4 项平台条件跳过，lint 0 错误；Flutter 原生身份界面 7/7 通过。包内 8 个原生库已核对 API 29 依赖与 16 KB 对齐。Android 11～15 各版本、其他机型和真正的 16 KB 页面设备仍待补充运行验证；本次未使用模拟器。

## 本地处理与手机性能

图片、视频和 GIF 在手机本地处理，不上传到转换服务器。转换会使用处理器、内存和存储，可能增加耗电并使手机发热；较旧手机建议先用少量图片、短片段和 360/480 像素输出尝试，再按实际效果调整。

尽量避免边充电边连续处理大任务；明显发烫或系统提示温度过高时，请取消任务并等待降温。当前没有自动温度监测或过热暂停。不同相册对 GIF 循环次数、透明背景和缩放的处理可能不同，请保留原素材并检查结果。完整使用须知与责任范围见附件 `DISCLAIMER.md`。

## 第三方组件与反馈

使用 [FFmpeg](https://ffmpeg.org/) 8.1.2（LGPL-2.1-or-later）。本次按 API 29 构建的完整对应源码、补丁和重建方法在 `FFmpeg-8.1.2-source.zip`；第三方许可正文及通知在 `THIRD-PARTY-NOTICES.zip`，也可在 App 设置中查看。所有配套材料与 APK 同页提供。

遇到问题请在 [Issues](https://github.com/LingXia979/GIF-Converter-Releases/issues) 提供版本、机型、Android 版本、功能、参数和复现步骤。分享素材前请确认有权提供并去除个人信息。

## 共同作者

- [LingXia979](https://github.com/LingXia979)：项目维护、功能方向与真机体验验收。
- [Codex / ChatGPT](https://github.com/codex)：AI 开发协作，参与实现、修复、验证与材料整理。
