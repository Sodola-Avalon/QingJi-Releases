# 清记 · QingJi Releases

这是清记（QingJi）的官方公开发布与在线更新仓库。

本仓库仅用于公开发布内容，不存放私有源码、签名密钥或开发凭据。

## 在线更新源

清记客户端通过 GitHub Releases 的 `latest` 接口检查更新：

`https://api.github.com/repos/Sodola-Avalon/QingJi-Releases/releases/latest`

默认仅在用户主动点击“检查更新”时联网，不在后台轮询。

## 发布约定

- Tag：`v1.0.18`、`v1.0.19`、`v1.1.0`……
- Release 标题：`清记 Vx.y.z`
- APK：`QingJi-vx.y.z.apk`
- SHA-256：`QingJi-vx.y.z.apk.sha256`
- Release 正文：作为客户端显示的更新日志
- 正式版本不得标记为 Draft 或 Prerelease

客户端只接受符合命名规则的 APK 资产，并在安装前校验配套 SHA-256。

## 当前正式版本

- 最新正式版：`V1.0.19`
- Release：`v1.0.19`
- versionCode：`24`
- APK：`QingJi-v1.0.19.apk`
- APK 大小：`322010` bytes
- APK SHA-256：`93519c21cea293d6ecab446a3050a5ed7b4724bb61341316fab0e82fa3d84d9d`
- 配套 SHA 文件：`QingJi-v1.0.19.apk.sha256`
- 原 QingJi signer SHA-256：`09826dcef6717e502e1d09f498e9733fe5b6773f16c69a82bf7cea7ecf092e33`

V1.0.19 使用 HyperOS 真机验收通过的 V1.0.19-r3 作为 exact 正式产物。发布门禁重新从公开 V1.0.18 基底重建该 APK，并在创建 Release 前硬校验二进制增量、最终 APK SHA-256/文件大小、versionCode/versionName、APK Signature Scheme v2/v3 和原 QingJi signer；发布后又将公开资产重新下载并再次核对 exact SHA。

开发、测试和私有恢复资料继续存放于 Private `Sodola-Avalon/QingJi` 与 `Sodola-Avalon/qingji-android-test-lab`，不要提交到本公开发布仓库。
