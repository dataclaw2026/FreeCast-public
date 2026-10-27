# FreeCast 无限投屏 · 公共发布库

会议室投屏系统 **FreeCast** 的对外发布仓库：PC 客户端与 TV 端安装包。

## 下载

### PC 客户端（Windows）

| 文件 | 说明 |
|---|---|
| `FreeCast-pc-v1.1.4-win10-11.zip` | **推荐** · 自包含版（免装 .NET 运行时，解压运行 `FreeCast.exe` 即用，约 103MB） |
| `FreeCast-pc-v1.1.4.zip` | 轻量版（约 37MB，需先装 [.NET 8 Desktop Runtime x64](https://dotnet.microsoft.com/download/dotnet/8.0)） |

适用 **Windows 10（1607+）与 Windows 11** x64，单包通用无需分版本编译；Windows 7/8.1 不支持。

### TV 端（Android 5.0+，按 CPU 架构选择，不确定就下 universal）

| 文件 | 适用设备 |
|---|---|
| `FreeCast-tv-v1.1.4-universal.apk` | 全架构通用（推荐，体积稍大） |
| `FreeCast-tv-v1.1.4-armv7.apk` | 32 位 ARM（多数老电视/盒子，如海信/小米盒子） |
| `FreeCast-tv-v1.1.4-arm64.apk` | 64 位 ARM（新电视/盒子，Android 9+ 常见） |
| `FreeCast-tv-v1.1.4-x86.apk` | 32 位 x86（模拟器/少数盒子） |
| `FreeCast-tv-v1.1.4-x64.apk` | 64 位 x86_64（部分 Intel 平台盒子） |

## 使用

1. 电视装 TV 端并打开，右上角显示 6 位投屏码（每台电视固定一个码）
2. 电脑解压运行 FreeCast.exe，输入码点「开始投屏」——自动配对自动串流
3. 手机浏览器扫电视上的二维码进管理页：改名/改码/换背景图/自动重启/空闲自动关机等设置

## v1.1.4 特性

- **双端自动版本检查**：PC 关于窗显示远程版本并提示升级；TV 启动后在码屏信息区显示远程版本，发现新版自动下载安装
- **国内版本源（versionsrc）**：国内电视连不上 GitHub 时，可在管理页「电视设置 → 版本源」填一个国内可达的地址（NAS/镜像/PC 局域网），版本检测即刻可用；留空恢复 GitHub
- **码屏前台保障**：码屏被桌面等盖住 20 秒后自动回到前台，投屏码随时可见；也可在系统设置里把默认主页设为「无限投屏」一步到位
- 空闲自动关机（时限可配）、开机自启、每天 04:00 自动重启保流畅

## 版本更新

TV 端与 PC 端会自动检查本库 `version.json`，发现新版本自动下载（TV 拉起安装确认，PC 退出时自动替换重启）。自动更新始终使用 universal 包，全机型通用。

## 许可

本产品内置并封装 Sunshine（GPLv3）与 Moonlight（GPLv3）核心，依许可要求提供对应源码获取方式；应用源码请通过仓库 issue 联系获取书面源码副本。
