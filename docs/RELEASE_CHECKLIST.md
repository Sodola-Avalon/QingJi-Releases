# QingJi 正式发版清单

每个正式版本发布到本仓库前，按下面顺序执行。

## 构建与验证

- [ ] `versionName` / `versionCode` 已更新
- [ ] 使用清记既有签名证书签名
- [ ] APK 可覆盖安装上一正式版本，且用户数据保留
- [ ] 核验签名证书指纹与历史正式版本一致
- [ ] 计算 APK SHA-256
- [ ] Android 15 / API 35 自动化回归通过
- [ ] 针对本版本修改点完成至少一轮对抗性测试
- [ ] 无 `FATAL EXCEPTION`

## Release 内容

- [ ] Tag 使用 `vX.Y.Z`
- [ ] 标题使用 `清记 VX.Y.Z`
- [ ] 上传 `QingJi-vX.Y.Z.apk`
- [ ] 上传 `QingJi-vX.Y.Z.apk.sha256`
- [ ] Release 正文填写用户可读的更新日志
- [ ] Draft = false
- [ ] Prerelease = false

## 发布后验证

- [ ] GitHub `releases/latest` 返回刚发布的正式版本
- [ ] 匿名访问 GitHub API 可读取 Release
- [ ] APK asset 下载地址可访问
- [ ] `.sha256` 内容与 Release APK 实际哈希一致
- [ ] 上一正式版本中的“检查更新”能发现新版
- [ ] 下载完成后 SHA-256 校验通过
- [ ] Android 系统允许同签名覆盖安装

## 规则

若任意关键项失败，不发布正式 Release；先修复并重新测试。
