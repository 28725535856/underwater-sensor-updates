# 水下传感器更新

此仓库只发布已签名 Android 安装包、版本信息和发布流程，不包含客户端源码、签名私钥或传感器测量数据。

## 在手机 App 内更新

固定更新清单地址：

```text
https://github.com/28725535856/underwater-sensor-updates/releases/latest/download/latest.json
```

在 App 的“检查更新”中保存此地址，点击“保存并检查”，有新版本时确认下载和安装。首次按系统提示允许本应用安装更新。已经安装此前测试版时无需先卸载。

当前在线版本：**1.0.5（versionCode 6）**，Android 6 及以上。

- [当前版本下载页](https://github.com/28725535856/underwater-sensor-updates/releases/tag/v1.0.5)
- [所有版本](https://github.com/28725535856/underwater-sensor-updates/releases)
- [当前清单副本](latest.json)

当前 APK SHA-256：

```text
17d2d32d282b1f0db4ce9b546160266c10f02e805d0311a7d7ded601490ee59b
```

已从执行环境验证固定清单链接与完整 APK 下载，摘要匹配。手机网络访问和系统安装尚在验收中，不将单一网络的访问结果视为所有手机均可访问。

## 后续发布约定

新版本保持原包名和同一签名，增加 versionCode。创建对应 Release，附加已签名 APK 和名为 latest.json 的清单，并将其设为 Latest。清单应指向该版本的固定 APK 下载地址，填写 APK 实际 SHA-256；同时更新仓库根目录的清单副本。App 的固定清单地址无需修改。

.github/workflows/publish-1.0.5.yml 记录本次迁移发布步骤：下载已签名包、核对 SHA-256 与字节数、发布 Release 附件。它仅针对 1.0.5，不会构建客户端或修改签名。不需要将账户密码、长期访问密钥或签名私钥加入仓库。
