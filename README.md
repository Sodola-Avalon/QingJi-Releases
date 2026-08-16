# 清记 · QingJi Releases

这是清记（QingJi）的官方公开发布与在线更新仓库。

本仓库仅用于公开发布内容，不存放私有源码、签名密钥或开发凭据。

## 在线更新源

清记客户端通过 GitHub Releases 的 `latest` 接口检查更新：

`https://api.github.com/repos/Sodola-Avalon/QingJi-Releases/releases/latest`

默认仅在用户主动点击“检查更新”时联网，不在后台轮询。

## 发布约定

- Tag：`v1.0.17`、`v1.0.18`、`v1.1.0`……
- Release 标题：`清记 V1.0.17`
- APK：`QingJi-v1.0.17.apk`
- SHA-256：`QingJi-v1.0.17.apk.sha256`
- Release 正文：作为客户端显示的更新日志
- 正式版本不得标记为 Draft 或 Prerelease

客户端只接受符合上述命名规则的 APK 资产，并校验版本号后再提示安装。

## 当前正式版本

- 最新正式版：`V1.0.17`
- Release：`https://github.com/Sodola-Avalon/QingJi-Releases/releases/tag/v1.0.17`
- APK SHA-256：`d03b0521acbc4fa7eaca1dfd988e22312c3018774646a98ad327367bf6d82310`
- V1.0.17 已正式接入本仓库作为客户端“检查更新”来源，并完成发布后真实线上反向验证。

下一开发目标为 `V1.0.18`。开发/测试/私有恢复资料继续存放于 Private `Sodola-Avalon/QingJi` 与 `Sodola-Avalon/qingji-android-test-lab`，不要提交到本公开发布仓库。
