# 斐讯设备社区项目

为已淘汰或原厂云服务停止的 IoT 设备维护社区固件、操作网页与管理平台。目前支持斐讯 **TC1 智能排插、M1 空气检测仪、A1 空气净化器**及 **DAIKIN 大金空气检测仪**，让设备在本地网络继续使用，也能接入 MQTT、Home Assistant 和 IotCloud。

**[项目主页](https://phicomm-io.github.io/) · [固件下载](https://phicomm-io.github.io/#releases) · [使用文档](https://phicomm-io.github.io/#docs) · [在线演示](https://phicomm-io.github.io/#demos)**

## 支持的设备

| 设备 | 主要功能 | 刷机与使用 |
| --- | --- | --- |
| **TC1 智能排插（A1 硬件版本）** | 六路插座控制、功率与电量统计、定时、童锁 | [免拆刷机](https://phicomm-io.github.io/guides/tc1-no-disassembly.html) · [有线刷机与恢复](https://phicomm-io.github.io/guides/tc1-flash.html) · [使用](https://phicomm-io.github.io/guides/tc1-guide.html) |
| **M1 空气检测仪** | 温湿度、PM2.5、甲醛、屏幕设置与净化器联动；配套开源主控可扩展颗粒物详情、屏幕 CO₂ 与音乐闹钟 | [免拆刷机](https://phicomm-io.github.io/guides/m1-no-disassembly.html) · [有线刷机与恢复](https://phicomm-io.github.io/guides/a1-m1-flash.html) · [使用](https://phicomm-io.github.io/guides/m1-guide.html) |
| **A1 空气净化器** | 风机调速、自动模式、滤芯统计、触摸面板、RGB 灯环、夜间模式与多检测仪联动；另有新风版固件 | [免拆刷机](https://phicomm-io.github.io/guides/a1-no-disassembly.html) · [有线刷机与恢复](https://phicomm-io.github.io/guides/a1-m1-flash.html) · [使用](https://phicomm-io.github.io/guides/a1-guide.html) |
| **DAIKIN 大金空气检测仪** | PM2.5、PM10、CO₂、温湿度、TVOC 与可选甲醛，支持 A1 联动 | [BRY88AB151K 原厂 OTA 刷机](https://phicomm-io.github.io/guides/daikin-stock-ota.html) · [BRY88AX151K 安装与使用](https://phicomm-io.github.io/guides/daikin-guide.html) |

**TC1 的 A1 硬件版本与 A1 空气净化器是不同产品，固件不能混用。** TC1 A2 尚不在当前支持范围内。M1 和 A1 空气净化器适用于原装 EMW3080B / MK3080B 模组；大金教程对应 ESP32 / 4 MB Flash 设备，不能推定其他型号兼容。免拆刷机是否适用，需先核对各教程的原厂版本与前提。

## M1 开源传感器主控

M1 内部有两颗分别升级的 MCU：**EMW3080 Wi-Fi MCU**负责联网与网页，**ATSAMD20G18A 传感器主控**负责与机内传感器通信，以及屏幕、按键和蜂鸣器。我们为后者提供采用 **MIT 许可**的[开源主控固件](https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20)。

在原有传感器读数基础上，开源主控增加：

- **颗粒物详情**：读取 PM1.0 / PM2.5 / PM10、六档累计颗粒数和原始传感器帧；配套 Wi-Fi v0.9.27 可直接在网页查看。
- **实体屏幕显示 CO₂**：可替换原数字位置或交替显示，需要另接 CO₂ 传感器并提供有效数据，原机不会因此自动获得 CO₂ 测量能力。
- **提示音与音乐闹钟**：四种提示音、自定义 RTTTL 单音音乐，支持写入、读回、播放、停止与保存。
- **诊断与调试**：传感器健康状态、显示缓存、屏幕段码与蜂鸣器调试，以及阈值设置修复。

当前主控发布为 **v0.9.4 开发预览**。不同功能需要对应的主控版本与能力，网页新功能还需配套 Wi-Fi 固件。**普通 Wi-Fi OTA 不会更新传感器主控。** 为降低新手误刷风险，主控没有 WebUI 上传入口；请使用电脑脚本，通过 API 单独升级。基本温湿度、PM2.5、甲醛读数无需为此额外刷主控。

**[功能与版本条件](https://phicomm-io.github.io/guides/m1-mcu-firmware.html) · [主控 API 升级教程](https://phicomm-io.github.io/guides/m1-mcu-update.html) · [主控发布与下载](https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20/releases)**

## 从哪里开始

固件免费，无需原厂云服务。首次安装先阅读[刷机前准备](https://phicomm-io.github.io/guides/flash-prep.html)，再按型号下载固件并依照教程刷入。安装后通过[快速开始](https://phicomm-io.github.io/guides/quick-start.html)完成配网，用浏览器访问设备即可进行本地控制，不需要部署管理平台。

- **只在家里使用**：直接访问设备网页，或使用[本地设备管理](https://phicomm-io.github.io/local/)。
- **远程集中管理**：按[接入 IotCloud](https://phicomm-io.github.io/guides/iotcloud-connect.html)选择节点、注册并配置设备；两个节点的账号和数据独立。
- **智能家居与自动化**：配置 [MQTT、Home Assistant 与设备联动](https://phicomm-io.github.io/guides/mqtt-link.html)。
- **已经安装社区固件**：查看[固件更新](https://phicomm-io.github.io/guides/firmware-update.html)与 [Release Log / 跨版本升级差异](https://phicomm-io.github.io/guides/release-log.html?view=compare)。

## 项目组成

| 项目 | 负责内容 | 公开情况 |
| --- | --- | --- |
| [社区固件](https://github.com/phicomm-io/phicomm-community-firmware) | TC1、M1、A1、DAIKIN 联网固件、构建脚本与设备文档 | 源码仓库私有；固件与文档从项目主页获取 |
| [M1 开源主控](https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20) | ATSAMD20G18A 传感器主控固件、协议分析、升级工具与验证记录 | 公开，MIT 许可；独立开发预览发布 |
| [统一前端](https://github.com/phicomm-io/phicomm-community-frontend) | 设备 WebUI、平台管理界面与演示 | 公开；固件使用锁定提交的前端 Release |
| [管理平台](https://github.com/phicomm-io/phicomm-community-mqtt) | IotCloud / TMCP 平台服务、MQTT 接入与部署配置 | 公开 |
| [公开网站](https://github.com/phicomm-io/phicomm-io.github.io) | 使用文档、在线演示、固件下载与历史版本归档 | 公开 |

## 项目路线图

已具备本地控制、MQTT / Home Assistant 接入、IotCloud、签名 OTA 与固件归档、跨版本更新说明，以及 M1 开源传感器主控。接下来继续完善设备兼容性与长期稳定性、国际化、升级恢复和自动化验收；DC1、TC1 A2 仍为后续支持方向。

具体任务见[公开 Project 路线图](https://github.com/orgs/phicomm-io/projects/3)与[文字版路线图](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.md)。不承诺交付日期；软件功能、正式发布和实机验收分别记录，以各版本说明为准。

感谢上游项目、SDK 提供方和社区贡献者。各组件的版权及授权以对应项目说明为准，M1 主控的 MIT 许可不代表其他仓库采用同一许可。本项目由社区维护，与原厂无隶属关系。
