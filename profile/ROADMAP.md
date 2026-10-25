# 斐讯设备社区项目路线图

为 TC1 智能排插、M1 空气检测仪、A1 空气净化器与 DAIKIN 大金空气检测仪维护社区固件、设备网页及管理平台；另独立维护 M1 ATSAMD20G18A 开源传感器主控。

[项目主页](https://phicomm-io.github.io/) · [使用文档](https://phicomm-io.github.io/#docs) · [固件下载](https://phicomm-io.github.io/#releases) · [在线演示](https://phicomm-io.github.io/#demos)

## 当前进展（2026-10-25）

- **设备支持**：当前覆盖 TC1 A1 硬件版本、M1、A1 和 DAIKIN；提供按型号区分的免拆迁移与有线恢复教程。DC1、TC1 A2 仍为后续支持方向，不能把开发基线视为已支持。
- **M1 开源主控**：ATSAMD20G18A 固件以 MIT 许可公开，v0.9.4 为开发预览；增加完整传感器帧、CO₂ 屏幕显示、提示音与 RTTTL 音乐。联网 MCU 与传感器主控独立升级，[功能与版本条件](https://phicomm-io.github.io/guides/m1-mcu-firmware.html)以文档为准。
- **国际化**：已有中英文使用文档、多语言界面与明暗主题，继续完善翻译及地区设置，具体支持以对应固件版本为准。
- **OTA 与发布**：已有签名 OTA、GitHub Pages 与境内外更新来源、固件历史归档和跨版本升级差异；各型号的在线检查、文件上传与首次迁移入口以[更新教程](https://phicomm-io.github.io/guides/firmware-update.html)为准。继续完善故障恢复与发布验证。
- **平台与工程化**：统一前端、IotCloud / MQTT 管理平台及 M1 主控源码已公开，联网固件源码仓库仍为私有。持续完善设备联动、文档、自动化验收与长期稳定性验证。

以上是已实现能力概览，不代表所有正式镜像、硬件修订和异常场景均已验收。最新任务进度见[项目看板](https://github.com/orgs/phicomm-io/projects/3)，软件交付、正式发布和实机验收分别跟踪。

## 历史任务快照（2026-10-16）

以下保留 2026-10-16 的历史任务概览，**不是当前状态**；最新进展见[项目看板](https://github.com/orgs/phicomm-io/projects/3)，不承诺交付日期。软件交付与实机验收分别跟踪。

| 方向 | 任务 | 状态 |
| --- | --- | --- |
| 扩展斐讯遗产设备支持 | [支持 DC1](https://github.com/phicomm-io/.github/issues/1) | 待开始 |
| 扩展斐讯遗产设备支持 | [支持 TC1 A2 硬件版本](https://github.com/phicomm-io/.github/issues/2) | 待开始 |
| 扩展斐讯遗产设备支持 | [验证 TC1 A1 硬件支持](https://github.com/phicomm-io/.github/issues/3) | 进行中 |
| 扩展斐讯遗产设备支持 | [验证 A1 空气净化器等现有设备支持](https://github.com/phicomm-io/.github/issues/4) | 进行中 |
| 国际化支持 | [国际化支持](https://github.com/phicomm-io/.github/issues/5) | 进行中 |
| 国际化支持 | [增加多语言支持](https://github.com/phicomm-io/.github/issues/6) | 已完成 |
| 国际化支持 | [增加时区支持](https://github.com/phicomm-io/.github/issues/7) | 进行中 |
| OTA 在线更新体系 | [OTA 在线更新体系](https://github.com/phicomm-io/.github/issues/8) | 进行中 |
| OTA 在线更新体系 | [定义 OTA channel 与更新源元数据](https://github.com/phicomm-io/.github/issues/9) | 进行中 |
| OTA 在线更新体系 | [增加 OTA 签名与设备端验签](https://github.com/phicomm-io/.github/issues/10) | 进行中 |
| OTA 在线更新体系 | [通过 CI 发布 OTA 到 Cloudflare R2 并提供 HTTP 反代](https://github.com/phicomm-io/.github/issues/11) | 进行中 |
| OTA 在线更新体系 | [WebUI 显示当前版本与最新版本](https://github.com/phicomm-io/.github/issues/12) | 进行中 |
| OTA 在线更新体系 | [WebUI 从更新源在线更新](https://github.com/phicomm-io/.github/issues/13) | 进行中 |
| OTA 在线更新体系 | [增加 MQTT 触发在线更新](https://github.com/phicomm-io/.github/issues/14) | 进行中 |
| OTA 在线更新体系 | [显示当前版本到最新版本之间的 Release Log](https://github.com/phicomm-io/.github/issues/15) | 进行中 |
| 工程化与发布记录 | [工程化与发布记录](https://github.com/phicomm-io/.github/issues/16) | 进行中 |
| 工程化与发布记录 | [规范 Release Log 记录与发布流程](https://github.com/phicomm-io/.github/issues/17) | 进行中 |
| 工程化与发布记录 | [增加 Issue 模板](https://github.com/phicomm-io/.github/issues/18) | 待开始 |
| 工程化与发布记录 | [制定编码规范](https://github.com/phicomm-io/.github/issues/19) | 待开始 |
| 工程化与发布记录 | [制定 PR 规范与模板](https://github.com/phicomm-io/.github/issues/20) | 进行中 |
| 工程化与发布记录 | [集成 TMCP 平台、账号权限迁移与平台 CI](https://github.com/phicomm-io/.github/issues/21) | 已完成 |
| 工程化与发布记录 | [完成 TMCP 平台设备验收与生产切换](https://github.com/phicomm-io/.github/issues/22) | 进行中 |
| 工程化与发布记录 | [完成平台设备首页复用与控制交互收尾](https://github.com/phicomm-io/.github/issues/23) | 已完成 |
| 工程化与发布记录 | [交付可调 TC1 A1 M1 WebUI 开发模拟器](https://github.com/phicomm-io/.github/issues/24) | 已完成 |
| 工程化与发布记录 | [统一公开站点设计及站点 Wiki 文档单一来源](https://github.com/phicomm-io/.github/issues/25) | 进行中 |
| 扩展斐讯遗产设备支持 | [统一固件命令服务、自动化与 TMCP v2 软件基线](https://github.com/phicomm-io/.github/issues/26) | 已完成 |
| 扩展斐讯遗产设备支持 | [改进按键事件分组、动作说明与编辑交互](https://github.com/phicomm-io/.github/issues/27) | 已完成 |
| 扩展斐讯遗产设备支持 | [修复 A1 触摸面板与灯带时序及交互反馈](https://github.com/phicomm-io/.github/issues/28) | 进行中 |
| 扩展斐讯遗产设备支持 | [扩展斐讯遗产设备支持](https://github.com/phicomm-io/.github/issues/29) | 进行中 |
| 扩展斐讯遗产设备支持 | [交付独立设备控制、默认名称恢复与 A1 导光反馈软件](https://github.com/phicomm-io/.github/issues/30) | 已完成 |
| OTA 在线更新体系 | [feat: dual-source OTA releases and public version archive](https://github.com/phicomm-io/.github/issues/31) | 已完成 |
| 工程化与发布记录 | [交付 stable 双来源 OTA 发布链路与 Pages 历史归档](https://github.com/phicomm-io/.github/issues/32) | 已完成 |
