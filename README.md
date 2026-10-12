# 记账 Android 网页套壳

- 应用名称：记账
- 应用图标：使用需求中提供的图标
- 启动网址：`https://creamci.cn:8010/mobile`
- 技术：原生 Android Java + WebView
- 最低 Android 版本：Android 6.0（API 23）

## 使用 Android Studio 打包 APK

1. 安装 Android Studio（建议较新版本）及 Android SDK Platform 35。
2. 解压本工程，在 Android Studio 中选择 **Open** 并打开 `jizhang-app` 文件夹。
3. 等待 Gradle Sync 完成。如提示安装 Android SDK Build-Tools / Platform 35，请按提示安装。
4. 菜单选择 **Build → Build Bundle(s) / APK(s) → Build APK(s)**。
5. 成功后点击提示中的 **locate**，或在 `app/build/outputs/apk/debug/app-debug.apk` 找到 APK。
6. 将 APK 发送到安卓手机安装；如系统提示，允许本次安装来源安装应用。

## 功能说明

- 全屏 WebView 加载指定移动网页。
- 支持 JavaScript、DOM Storage、Cookie，适用于常见移动 Web 页面。
- Android 返回键优先返回网页上一页。
- 页面需要上传文件时可调起系统文件选择器。
- creamci.cn 站内链接在应用内打开，其他外部链接交由系统浏览器/对应应用处理。
- 不绕过 HTTPS 证书校验；服务器证书异常时需要先修复服务端证书。

## 注意

这是网页套壳，不包含网站后端或离线页面。手机必须能够访问 `creamci.cn:8010`。若网页使用了需要额外权限的原生功能（如扫码硬件、蓝牙等），需要再单独适配。
