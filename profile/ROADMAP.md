# 斐讯设备社区项目路线图

为 TC1 智能排插、M1 空气检测仪与 A1 空气净化器维护社区固件、设备网页及管理平台。

[项目主页](https://phicomm-io.github.io/) · [使用文档](https://phicomm-io.github.io/#docs) · [固件下载](https://phicomm-io.github.io/#releases) · [在线演示](https://phicomm-io.github.io/#demos)

## 四个方向

- **设备支持**：完善 TC1 A1、M1、A1 的实机验收与稳定性，探索 DC1、TC1 A2。
- **国际化**：已有多语言界面，继续完善地区时区与夏令时。
- **OTA 在线更新**：已有双来源更新与固件归档，继续完善频道、累计更新说明及故障恢复验证。
- **工程化与发布**：固件、前端、平台分仓，持续完善文档、自动化验收与贡献规范。

## 任务概览

以下为 2026-10-16 的任务概览；最新进展见[项目看板](https://github.com/orgs/phicomm-io/projects/3)，不承诺交付日期。软件交付与实机验收分别跟踪。

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
