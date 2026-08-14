# 安卓屏连 - 竖屏控制 (extend)

本项目是从较大的 [安卓屏连](https://gitee.com/connect-screen/connect-screen) 工程中筛选出的 **竖屏控制（extend）** 相关部分，
包含可直接安装的 APK 与可完整编译的 Android 工程源码。

## 📦 包含内容

| 内容 | 说明 |
|------|------|
| `安卓屏连-extend-竖屏控制.apk` | 竖屏控制（extend）已构建 APK，可直接安装 |
| `app-extend/` | extend（竖屏控制）模块完整源码 |
| `hidden-api-stub/` | extend 依赖的隐藏 API 桩模块 |
| Gradle 工程骨架 | `build.gradle` / `settings.gradle` / `gradle.properties` / `gradlew` 等 |

> 说明：原工程较大且包含多个模块与子模块，本仓库仅保留 **竖屏控制（extend）** 需要的模块，保证可独立打开与编译。

## 🔧 编译

使用 **Android Studio** 打开本工程（Gradle 同步），选择 `app-extend` 模块即可编译：

- ApplicationId: `com.connect_screen.extend`
- compileSdk / targetSdk: 34，minSdk: 26
- versionName: 1.3.8 (versionCode 38)

命令行编译示例：

```bash
gradlew :app-extend:assembleDebug
```

## ⚖️ 说明

本部分使用 DisplayLink® 驱动以支持 DisplayLink® 设备连接；DisplayLink® 为 Synaptics Incorporated 的注册商标。
开发者与 Synaptics Incorporated 无官方关联。完整版权声明见原工程 `LICENSE`。

相关教程与用户手册：https://connect-screen.com/
