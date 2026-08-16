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

- 最新正式版：`V1.0.18`
- Release：`v1.0.18`
- versionCode：`21`
- APK：`QingJi-v1.0.18.apk`
- APK 大小：`326301` bytes
- APK SHA-256：`5090167f428390cc791c36b04ac837c82b7835c6d480dfb74a72bb61f1c60896`
- 配套 SHA 文件：`QingJi-v1.0.18.apk.sha256`

V1.0.18 发布前已再次验证原 QingJi signer、APK Signature Scheme v2/v3、版本号和 exact APK SHA；发布后又完成正式 V1.0.17 客户端的真实线上升级链路验证，包括发现 V1.0.18、下载 APK/.sha256、SHA 校验、未知来源授权、Android 系统安装器、原地升级和数据保留。

开发、测试和私有恢复资料继续存放于 Private `Sodola-Avalon/QingJi` 与 `Sodola-Avalon/qingji-android-test-lab`，不要提交到本公开发布仓库。
