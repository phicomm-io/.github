# 斐讯设备社区项目

为斐讯 **TC1 智能排插、M1 空气检测仪和 A1 空气净化器**维护社区固件及配套网页，让设备通过本地网络继续使用，也能接入 MQTT、Home Assistant 和远程管理平台。

**[项目主页](https://phicomm-io.github.io/) · [固件下载](https://phicomm-io.github.io/#releases) · [使用文档](https://phicomm-io.github.io/#docs) · [在线演示](https://phicomm-io.github.io/#demos)**

## 支持的设备

| 设备 | 主要功能 | 刷机与使用 |
| --- | --- | --- |
| **TC1 智能排插** | 六路插座控制、功率与电量统计、定时、童锁 | [刷机](https://phicomm-io.github.io/guides/tc1-flash.html) · [使用](https://phicomm-io.github.io/guides/tc1-guide.html) |
| **M1 空气检测仪** | 温湿度、PM2.5、甲醛读数、屏幕设置与净化器联动 | [J-Link / Bootloader 刷机](https://phicomm-io.github.io/guides/a1-m1-flash.html) · [使用](https://phicomm-io.github.io/guides/m1-guide.html) |
| **A1 空气净化器** | 风机调速、触摸面板、RGB 灯环、夜间模式与多 M1 联动 | [J-Link / Bootloader 刷机](https://phicomm-io.github.io/guides/a1-m1-flash.html) · [使用](https://phicomm-io.github.io/guides/a1-guide.html) |

TC1 仅支持 **A1 硬件版本**，不支持 A2；它与 **A1 空气净化器**是不同产品，固件不能混用。M1 和 A1 空气净化器适用于原装 EMW3080B / MK3080B 模组。

## 从哪里开始

固件免费，无需原厂云服务。首次安装先阅读[刷机前准备](https://phicomm-io.github.io/guides/flash-prep.html)，再按型号下载固件并依照教程刷入。安装后通过[快速开始](https://phicomm-io.github.io/guides/quick-start.html)完成配网，用浏览器访问设备即可进行本地控制，不需要部署管理平台。

需要智能家居接入或远程集中管理时，再配置 [MQTT、Home Assistant 与设备联动](https://phicomm-io.github.io/guides/mqtt-link.html)。想先看看界面，可直接打开[在线演示](https://phicomm-io.github.io/#demos)。

## 项目组成

| 项目 | 负责内容 |
| --- | --- |
| [社区固件](https://github.com/phicomm-io/phicomm-community-firmware) | TC1、M1、A1 固件、构建脚本与设备文档 |
| [统一前端](https://github.com/phicomm-io/phicomm-community-frontend) | 设备 WebUI、平台管理界面与演示；固件构建使用锁定 commit 的前端 Release |
| [管理平台](https://github.com/phicomm-io/phicomm-community-mqtt) | TMCP 平台服务、MQTT 接入与部署配置 |
| [公开网站](https://github.com/phicomm-io/phicomm-io.github.io) | 使用文档、在线演示、固件下载与历史版本归档 |

目前固件和管理平台仓库为私有仓库，公开提供的文档、演示和固件下载请从[项目主页](https://phicomm-io.github.io/)进入。

感谢上游项目、SDK 提供方和社区贡献者。各组件的版权及授权以对应项目说明为准。本项目由社区维护，与原厂无隶属关系。
