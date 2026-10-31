# FreeCast-public · 无限投屏公共发布库

本仓库是无限投屏 FreeCast 的**版本源**（update feed）：电视端 / 手机端 / PC 端的升级检测都从这里拉 `version.json` 与安装包。

- Gitee（默认源，国内可达）：`https://gitee.com/dataclaw2026/FreeCast-public/raw/master/`
- GitHub 镜像：`https://github.com/dataclaw2026/FreeCast-public`
- 源码仓库：`https://github.com/dataclaw2026/FreeCast`

## 当前版本 v1.2.1

| 端 | 文件 | 说明 |
|---|---|---|
| TV / 盒子 | FreeCast-tv-v1.2.1-{arm64,armv7,universal,x64,x86}.apk | 接收端（码屏 + 管理 + 串流解码） |
| 手机端 | FreeCast-phone-v1.2.1-{arm64,armv7,universal}.apk | 投屏端（输入码 → 投屏，代码与接收端完全分离） |
| PC 轻量版 | FreeCast-pc-v1.2.1.zip | 需先装 .NET 8 桌面运行时 |
| PC 完整版 | [Release 资产](https://github.com/dataclaw2026/FreeCast-public/releases/download/v1.2.1/FreeCast-pc-v1.2.1-win10-11.zip) | 自包含（>100MB，走 GitHub Release），内嵌 Sunshine 引擎 |

## version.json 字段

- `version`：当前版本号（三端比较基准）
- `tv_abi` / `phone` / `phone_abi`：按 CPU 架构取小包（相对路径 = 本仓库 raw 直链）
- `pc`：自包含完整包（GitHub Release 资产直链）
- `pc_light`：轻量包（相对路径，需 .NET 8）

## 维护约定

- 发新版：更新 `version.json` 的 `version` 与各端文件名，APK 按同名规则放本仓库根目录；
  PC 完整包传 GitHub Release（`v<版本>` tag）。
- 本仓库 master 保持**只有 feed 文件**，不要混入源码（源码在 FreeCast 仓库）。
