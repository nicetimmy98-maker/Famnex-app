# FAMNEX 内部测试包

这个仓库只发布奈希智能管家的内部测试安装包。源码、签名证书和涂鸦配置都在私有仓库，不会放到这里。

目前只有 Android。iOS 测试包以后也放在这个仓库。

安装包仅供内部测试，不提供源码授权。

## Android

包名是 `com.famnex.app`。这是连测试接口 `api-test.famnex.vip` 的 release 包，使用内部测试证书，不是应用商店的正式版。

第一份安装包发布之后，下面两个地址保持不变：

- 检查更新清单：<https://raw.githubusercontent.com/nicetimmy98-maker/Famnex-app/main/android-test-latest.json>
- 最新安装包：<https://github.com/nicetimmy98-maker/Famnex-app/releases/latest/download/FAMNEX-android.apk>

手机安装时允许浏览器下载未知来源应用。新包会覆盖手机里已安装的 `com.famnex.app`，并保留应用数据。构建号必须高于手机里的版本，系统才会接受覆盖安装。

`android-test-latest.json` 在第一次发布时才会出现。它的 `downloadUrl` 固定指向上面的最新安装包地址，`channel` 为 `test`。每次发布更新清单里的版本、构建号、SHA-256 和更新说明。

## 这个仓库不存放的内容

不要把 APK、IPA、AAB、keystore、安全算法 AAR 或 `tuya.properties` 提交进 Git。Android 安装包以附件 `FAMNEX-android.apk` 放到 GitHub Release。历史 Release 保留，不删除。

## 以后的 iOS

iOS 测试包使用同一仓库里的另一份清单和另一个固定附件名：

- 清单：`ios-test-latest.json`
- 附件：`FAMNEX-ios.ipa`
