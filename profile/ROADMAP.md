# IoTCloud 社区项目路线图

[English](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.en.md) · [项目主页](https://phicomm-io.github.io/) · [项目看板](https://github.com/orgs/phicomm-io/projects/3)

## 当前可用

TC1 A1 硬件版本、M1、A1 与文档列出的 DAIKIN 设备支持本地网页、MQTT、Home Assistant 与 IoTCloud。稳定通道保留 v0.9.27 与 0.9.x 历史制品；v1.0.0-rc.1 单独提供候选下载。M1 开源传感器主控独立发布，采用 GPL-3.0；推荐原厂 11.x 使用，17.1.2.3 / 17.x 暂不建议迁移。

## v1.0.0-rc.1 候选版

v1.0.0-rc.1 为预发布版本，供体验与测试。按机型选择镜像，并先阅读对应发布说明。

[联网固件候选版](https://github.com/phicomm-io/iotcloud-community-firmware/releases/tag/v1.0.0-rc.1) · [M1 主控候选版](https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20/releases/tag/v1.0.0-rc) · [IoTCloud 平台候选版](https://github.com/phicomm-io/iotcloud-community-mqtt/releases/tag/v1.0.0-rc.1) · [0.9.x 历史下载](https://phicomm-io.github.io/#releases)

| 方向 | 候选版内容 |
| --- | --- |
| 使用与升级 | 中英文界面、设备语言设置、配置备份恢复、迁移失败保护与跨版本升级差异 |
| M1 | 甲醛 / PM2.5 两区分别配置来源、数字格式、字样、单位、九段色灯与有效期，双击整体切换原始 / 用户显示，失效位置恢复原读数；来源可选本机与其他在线传感器、TC1 功率（W）、A1 主风机输出（0–100%，非实测转速）、大金或 API，原屏不增加单位字形；PM2.5 稳定处理，甲醛 / PM2.5 蜂鸣报警独立开关、默认关闭，色灯、闹钟与手动鸣叫独立；需要配套主控、联网固件和前端 |
| 通用读数接口 | RC.1 统一发布规范字段标识、名称、数值类型、单位、有效性与新鲜度，M1 按设备与字段读取；同步升级来源设备、M1 接收端和前端。旧联网 RC 已弃用，独立主控候选版不受影响 |
| DAIKIN `hub` | 独立中枢版本：通过自带 WebUI（`/iotcloud/#/`）配置独立本地账户、TCP / WebSocket MQTT Broker、局域网 Home Assistant、上游 MQTT 客户端、巴法云转发与 HAP；这些服务可并行运行，各设备 MQTT 需手动指向中枢 |
| Apple 家庭 | 大金中枢的实验性 HomeKit HAP 桥接，iPhone 家庭 App 的配对、控制与恢复仍待实机验收；当前未实现 Matter |
| 开源与贡献 | 按各仓库许可维护源码；固定前端制品、自动检查和贡献规范 |

接口、协议与配置约定集中在[中英文开发文档](https://phicomm-io.github.io/iotcloud-community-protocols/)。旧 0.9.x 制品与说明保留，正式版本以发布记录为准。

## 后续设备

DC1、TC1 A2 仍是后续支持方向，目前不在支持范围内。若能提供设备或测试结果，请在[项目看板](https://github.com/orgs/phicomm-io/projects/3)或 [Issue](https://github.com/phicomm-io/.github/issues)中交流。
