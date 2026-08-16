# QingJi 在线更新协议

本文档定义清记客户端与 `Sodola-Avalon/QingJi-Releases` 之间的更新检查约定。

## 1. 更新入口

客户端请求：

`GET https://api.github.com/repos/Sodola-Avalon/QingJi-Releases/releases/latest`

不需要 GitHub Token。

## 2. 客户端行为

1. 仅在用户主动点击“检查更新”时请求网络。
2. 读取 `tag_name`，去掉开头的 `v` 后与本地 `versionName` 比较。
3. 若远端版本不高于本地版本，显示“已是最新版本”。
4. 若存在新版，读取 Release 的 `name`、`body`、发布时间和 assets。
5. 只接受名称符合 `QingJi-v<version>.apk` 的 APK。
6. 同时寻找同版本的 `.apk.sha256` 资产；若存在，下载完成后必须校验 SHA-256。
7. 校验成功后交由 Android 系统安装器处理更新。
8. 网络失败、GitHub API 异常、Release 缺少 APK 或哈希不匹配时，必须明确提示失败，不静默安装。

## 3. 正式 Release 规则

- Tag：`vX.Y.Z`
- 标题：`清记 VX.Y.Z`
- APK：`QingJi-vX.Y.Z.apk`
- 校验文件：`QingJi-vX.Y.Z.apk.sha256`
- Release 正文：Markdown 更新日志
- `draft=false`
- `prerelease=false`

## 4. 安全约束

- 客户端不得内置 GitHub Personal Access Token。
- 更新源仓库必须保持 Public，否则普通客户端无法匿名读取。
- APK 必须继续使用清记现有 Android 签名证书签名。
- 客户端安装前优先进行 SHA-256 校验；系统升级安装还会进一步受 Android 同签名约束。
- 不接受来自其他仓库、重定向配置或任意 URL 的 APK。

## 5. V1.0.17 接入目标

V1.0.17 将把现有“检查更新”入口接到本协议，并保持手动检查为默认行为，不增加后台轮询或常驻服务。
