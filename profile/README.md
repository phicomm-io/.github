# IoTCloud 社区项目

[English](https://github.com/phicomm-io/.github/blob/main/profile/README.en.md)

让 TC1 智能排插、M1 空气检测仪、A1 空气净化器和 DAIKIN 大金空气检测仪继续好用：本地网页控制，接入 MQTT、Home Assistant，或使用 IoTCloud 集中管理。

**[设备与功能][devices] · [安装升级][install] · [常见问题][faq] · [参与开发][develop]**

## 设备与功能

| 设备 | 主要功能 | 使用与安装 |
| --- | --- | --- |
| TC1 智能排插（A1 硬件版本） | 六路开关、功率与电量、定时、童锁 | [使用][tc1] · [免拆安装][tc1-flash] |
| M1 空气检测仪 | PM2.5、甲醛、温湿度、屏幕与 A1 联动；配套开源主控可扩展颗粒物详情、CO₂ 显示和音乐 | [使用][m1] · [免拆安装][m1-flash] |
| A1 空气净化器 | 风机、自动模式、滤芯、灯环、夜间模式与多检测仪联动；另有新风版 | [使用][a1] · [有线安装][a1-flash] |
| DAIKIN 大金空气检测仪 | PM2.5、PM10、CO₂、温湿度、TVOC 与可选甲醛，支持 A1 联动 | [使用与安装][daikin] · [BRY88AB151K 原厂 OTA][daikin-flash] |

TC1 的 A1 硬件版本与 A1 空气净化器是不同产品，固件不能混用。当前不支持 TC1 A2。M1 / A1 教程适用于原装 EMW3080B / MK3080B 模组；大金教程适用于文档列出的 ESP32 / 4 MB Flash 设备。

M1 的 Wi-Fi 模块与传感器主控独立升级。[开源传感器主控][mcu]采用 **GPL-3.0**，推荐用于原厂 **11.x** 主控；原厂 **17.1.2.3 / 17.x** 差异较大，尚待分析，暂不建议迁移。普通 Wi-Fi OTA 不会更新主控，基本空气读数也不要求另刷主控。详见[主控说明][mcu-guide]。

## 安装升级

先阅读[刷机前准备][prep]，按机型安装，再通过[快速开始][quick]配网。只在局域网使用时，直接访问设备网页即可；远程管理可[接入 IoTCloud][cloud]，也可[自行部署][deploy]。

**[现有 0.9.x 下载][downloads] · [更新教程][update] · [在线演示][demos] · [本地直连][local]**

**v1.0 正在开发，尚未发布。** 开发内容包括双语界面、配置备份与迁移恢复、M1 甲醛 / PM2.5 两个位置的独立用户读数与双击整体切换、PM2.5 稳定处理，以及默认关闭的甲醛 / PM2.5 独立蜂鸣报警开关。用户读数可来自本机传感器、TC1 功率、A1 主风机输出百分比、大金或 API。独立的大金 `hub` 中枢提供自带 WebUI 配置入口，MQTT Broker、上游客户端、巴法云转发与 HAP 可并行运行。下载区继续提供已有 0.9.x 制品，功能与版本条件以发布说明为准。

## 常见问题

[故障排查][troubleshooting]涵盖配网、灯光提示、MQTT 和恢复。反馈时请写明机型、联网固件版本、M1 主控版本和复现步骤，并去掉密码、令牌等信息。

交流：QQ 群 **1021750178** · [加入群聊][qq] · [提交问题][issues]

## 参与开发

| 项目 | 内容 |
| --- | --- |
| [设备固件][firmware] | TC1、M1、A1 与 DAIKIN 固件、构建和使用指南 |
| [开发文档][protocols] | HTTP / MQTT、主控协议、配置兼容性与测试向量，中英文集中维护 |
| [统一前端][frontend] | 设备 WebUI、IoTCloud 与在线演示 |
| [IoTCloud 平台][platform] | MQTT 接入、账户管理与部署 |
| [M1 传感器主控][mcu] | 传感器、屏幕、按键与蜂鸣器，GPL-3.0 |
| [公开网站][website] | 安装使用文档、下载与版本归档 |

从[贡献指南](https://github.com/phicomm-io/.github/blob/main/CONTRIBUTING.md)和[路线图](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.md)开始。各组件许可见对应仓库，第三方代码保留原许可。项目由社区维护，与原厂无隶属关系。

[devices]: https://phicomm-io.github.io/#devices
[install]: https://phicomm-io.github.io/#install
[faq]: https://phicomm-io.github.io/#faq
[develop]: https://phicomm-io.github.io/#develop
[downloads]: https://phicomm-io.github.io/#releases
[demos]: https://phicomm-io.github.io/#demos
[local]: https://phicomm-io.github.io/local/
[tc1]: https://phicomm-io.github.io/guides/tc1-guide.html
[tc1-flash]: https://phicomm-io.github.io/guides/tc1-no-disassembly.html
[m1]: https://phicomm-io.github.io/guides/m1-guide.html
[m1-flash]: https://phicomm-io.github.io/guides/m1-no-disassembly.html
[a1]: https://phicomm-io.github.io/guides/a1-guide.html
[a1-flash]: https://phicomm-io.github.io/guides/a1-m1-flash.html
[daikin]: https://phicomm-io.github.io/guides/daikin-guide.html
[daikin-flash]: https://phicomm-io.github.io/guides/daikin-stock-ota.html
[prep]: https://phicomm-io.github.io/guides/flash-prep.html
[quick]: https://phicomm-io.github.io/guides/quick-start.html
[update]: https://phicomm-io.github.io/guides/firmware-update.html
[cloud]: https://phicomm-io.github.io/guides/iotcloud-connect.html
[deploy]: https://phicomm-io.github.io/guides/iotcloud-deploy.html
[troubleshooting]: https://phicomm-io.github.io/guides/faq.html
[mcu-guide]: https://phicomm-io.github.io/guides/m1-mcu-firmware.html
[protocols]: https://phicomm-io.github.io/iotcloud-community-protocols/
[firmware]: https://github.com/phicomm-io/iotcloud-community-firmware
[frontend]: https://github.com/phicomm-io/iotcloud-community-frontend
[platform]: https://github.com/phicomm-io/iotcloud-community-mqtt
[mcu]: https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20
[website]: https://github.com/phicomm-io/phicomm-io.github.io
[issues]: https://github.com/phicomm-io/.github/issues
[qq]: https://qm.qq.com/q/9L150V85kk?from=tim
