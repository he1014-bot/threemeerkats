# 安卓屏连 - 竖屏控制 (extend)

> 本代码适用于 **荣耀手机有线投屏** 场景。

本项目是从较大的 [安卓屏连](https://gitee.com/connect-screen/connect-screen) 工程中筛选出的 **竖屏控制（extend）** 相关部分，
包含可直接安装的 APK 与可完整编译的 Android 工程源码。

## 📱 适用范围

本工程的目标场景是 **荣耀手机有线投屏**，通过 USB/有线方式将荣耀手机画面投到屏幕或电脑上，并**强制竖屏显示 / 竖屏控制**，
解决部分荣耀机型有线投屏时宽高比、旋转、分辨率等控制不理想的问题。

- 代码在实现思路上**参考了 [屏易连](https://connect-screen.com/) 软件的代码**（竖屏控制、虚拟显示、旋转/分辨率/DPI 调节等逻辑）。
- 同时使用 Shizuku 权限调用系统隐藏 API 能力辅助实现投屏控制。

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

## 🏗️ 主要功能

- **有线投屏**：通过 DisplayLink® / USB 方式连接显示器或电脑。
- **竖屏控制**：强制/切换竖屏显示，适配荣耀手机屏幕。
- **分辨率 / DPI / 旋转调节**：通过隐藏 API 与 Shizuku 权限动态调整。
- **虚拟显示**：创建虚拟显示目标，实现双屏异显。
- **触摸板 / 外部输入绑定**：将触摸、鼠标等输入绑定到指定显示。

## 🙏 致谢与参考

- 参考了软件 **屏易连**（[connect-screen.com](https://connect-screen.com/)）的代码与思路。
- 借鉴了以下开源项目：
  - [安卓屏连（connect-screen）](https://gitee.com/connect-screen/connect-screen)
  - [Easycontrol](https://github.com/eiyooooo/Easycontrol)
  - [scrcpy](https://github.com/Genymobile/scrcpy)
  - [Shizuku](https://github.com/RikkaApps/Shizuku) / [awesome-shizuku](https://github.com/timschneeb/awesome-shizuku)

## ⚖️ 声明

- 本代码适用于 **荣耀手机有线投屏**，使用 DisplayLink® 驱动以支持 DisplayLink® 设备连接；DisplayLink® 为 Synaptics Incorporated 的注册商标，开发者与 Synaptics Incorporated 无官方关联。
- 本项目为学习与个人使用目的，使用请遵循各软件相关许可条款。

完整版权与许可信息见原工程 `LICENSE`。
