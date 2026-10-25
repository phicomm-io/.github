# IoTCloud 社区项目路线图

[English](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.en.md) · [项目主页](https://phicomm-io.github.io/) · [项目看板](https://github.com/orgs/phicomm-io/projects/3)

## 当前可用

TC1 A1 硬件版本、M1、A1 与文档列出的 DAIKIN 设备已有 0.9.x 固件、安装使用文档及版本归档。支持本地网页、MQTT、Home Assistant 与 IoTCloud。M1 开源传感器主控独立发布，采用 GPL-3.0；推荐原厂 11.x 使用，17.1.2.3 / 17.x 暂不建议迁移。

## v1.0 开发中

v1.0 尚未正式发布，以下功能仍需联调和真机验证，不提供 v1 下载。

| 方向 | 计划内容 |
| --- | --- |
| 使用与升级 | 中英文界面、设备语言设置、配置备份恢复、迁移失败保护与跨版本升级差异 |
| M1 | 甲醛 / PM2.5 两个位置各自配置用户读数、色灯与有效期，双击整体切换原始 / 用户显示，失效位置恢复原读数；来源可选本机传感器、TC1 功率（W）、A1 主风机输出（0–100%，非实测转速）、大金或 API，原屏不增加单位字形；PM2.5 稳定处理，甲醛 / PM2.5 蜂鸣报警独立开关、默认关闭，色灯、闹钟与手动鸣叫独立；需要配套主控、联网固件和前端 |
| DAIKIN `hub` | 独立中枢版本：通过自带 WebUI（`/iotcloud/#/`）配置独立本地账户、TCP / WebSocket MQTT Broker、局域网 Home Assistant、上游 MQTT 客户端、巴法云转发与 HAP；这些服务可并行运行，各设备 MQTT 需手动指向中枢 |
| Apple 家庭 | 在大金中枢上通过 HAP 桥接，iPhone 家庭 App 的配对、控制与恢复仍待实机验收；目前不宣称支持 Matter |
| 开源与贡献 | 按各仓库许可维护源码；固定前端制品、自动检查和贡献规范 |

接口、协议与配置约定集中在[中英文开发文档](https://phicomm-io.github.io/iotcloud-community-protocols/)。旧 0.9.x 制品与说明保留，正式版本以发布记录为准。

## 后续设备

DC1、TC1 A2 仍是后续支持方向，目前不在支持范围内。若能提供设备或测试结果，请在[项目看板](https://github.com/orgs/phicomm-io/projects/3)或 [Issue](https://github.com/phicomm-io/.github/issues)中交流。
