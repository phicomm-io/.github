# IoTCloud community projects

[简体中文](https://github.com/phicomm-io/.github/blob/main/profile/README.md)

Keep TC1 power strips, M1 air quality monitors, A1 air purifiers and documented DAIKIN air quality monitors useful with local web control, MQTT, Home Assistant and IoTCloud device management.

**[Devices and features][devices] · [Install and update][install] · [Common questions][faq] · [Contribute][develop]**

## Devices and features

| Device | Main features | Use and installation |
| --- | --- | --- |
| TC1 power strip, A1 hardware revision | Six outlets, power and energy, schedules and child lock | [Use][tc1] · [Install without disassembly][tc1-flash] |
| M1 air quality monitor | PM2.5, formaldehyde, temperature, humidity, display and A1 automation; an optional open-source controller adds particle details, CO₂ display and music | [Use][m1] · [Install without disassembly][m1-flash] |
| A1 air purifier | Fan control, automatic mode, filters, light ring, night mode and automation; a separate fresh-air variant is available | [Use][a1] · [Wired installation][a1-flash] |
| DAIKIN air quality monitor | PM2.5, PM10, CO₂, temperature, humidity, TVOC and optional formaldehyde; A1 automation | [Use and install][daikin] · [BRY88AB151K stock OTA][daikin-flash] |

The TC1 A1 hardware revision and the A1 purifier are different products. Their images are not interchangeable. TC1 A2 is unsupported. M1 / A1 guides target original EMW3080B / MK3080B modules; DAIKIN guides target the listed ESP32 devices with 4 MB Flash.

M1 Wi-Fi firmware and its sensor controller update separately. The [open-source controller][mcu] uses **GPL-3.0** and is recommended for stock **11.x** controllers. Stock **17.1.2.3 / 17.x** differs substantially and needs further analysis; migration is currently discouraged. Ordinary Wi-Fi OTA does not update the sensor controller. Basic air readings do not require this extra update. See the [controller guide][mcu-guide].

## Install and update

Read [Before flashing][prep], follow the guide for your model, then use [Quick start][quick] for Wi-Fi setup. A local device page is sufficient for LAN use. For remote management, [connect to IoTCloud][cloud] or [host your own instance][deploy].

**[Existing 0.9.x downloads][downloads] · [Update guide][update] · [Demos][demos] · [Local connection][local]**

**v1.0 is in development and has not been released.** Plans include bilingual interfaces, configuration backup and migration recovery, M1 double-click actions, external online CO₂ / generic Wi-Fi display data, steadier PM2.5 readings, separate formaldehyde / PM2.5 buzzer switches off by default and a separate DAIKIN `hub` variant. Downloads continue to provide existing 0.9.x artifacts. Check each release for its feature requirements.

## Common questions

[Troubleshooting][troubleshooting] covers Wi-Fi setup, indicators, MQTT and recovery. Reports should include the model, Wi-Fi firmware version, M1 controller version and reproduction steps. Remove passwords and tokens.

Community: QQ group **1021750178** · [Join][qq] · [Report an issue][issues]

## Contribute

| Project | Contents |
| --- | --- |
| [Device firmware][firmware] | TC1, M1, A1 and DAIKIN firmware, builds and user guides |
| [Developer documentation][protocols] | Bilingual HTTP / MQTT and controller protocols, configuration compatibility and test vectors |
| [Shared frontend][frontend] | Device WebUIs, IoTCloud and demos |
| [IoTCloud platform][platform] | MQTT access, accounts and deployment |
| [M1 sensor controller][mcu] | Sensors, display, button and buzzer; GPL-3.0 |
| [Public website][website] | Guides, downloads and release archives |

Start with the [contribution guide](https://github.com/phicomm-io/.github/blob/main/CONTRIBUTING.md) and [roadmap](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.en.md). Each component documents its own license; third-party code retains its original license. This community project is independent of the manufacturers.

[devices]: https://phicomm-io.github.io/en/#devices
[install]: https://phicomm-io.github.io/en/#install
[faq]: https://phicomm-io.github.io/en/#faq
[develop]: https://phicomm-io.github.io/en/#develop
[downloads]: https://phicomm-io.github.io/en/#releases
[demos]: https://phicomm-io.github.io/en/#demos
[local]: https://phicomm-io.github.io/local/
[tc1]: https://phicomm-io.github.io/guides/en/tc1-guide.html
[tc1-flash]: https://phicomm-io.github.io/guides/en/tc1-no-disassembly.html
[m1]: https://phicomm-io.github.io/guides/en/m1-guide.html
[m1-flash]: https://phicomm-io.github.io/guides/en/m1-no-disassembly.html
[a1]: https://phicomm-io.github.io/guides/en/a1-guide.html
[a1-flash]: https://phicomm-io.github.io/guides/en/a1-m1-flash.html
[daikin]: https://phicomm-io.github.io/guides/en/daikin-guide.html
[daikin-flash]: https://phicomm-io.github.io/guides/en/daikin-stock-ota.html
[prep]: https://phicomm-io.github.io/guides/en/flash-prep.html
[quick]: https://phicomm-io.github.io/guides/en/quick-start.html
[update]: https://phicomm-io.github.io/guides/en/firmware-update.html
[cloud]: https://phicomm-io.github.io/guides/en/iotcloud-connect.html
[deploy]: https://phicomm-io.github.io/guides/en/iotcloud-deploy.html
[troubleshooting]: https://phicomm-io.github.io/guides/en/faq.html
[mcu-guide]: https://phicomm-io.github.io/guides/en/m1-mcu-firmware.html
[protocols]: https://phicomm-io.github.io/iotcloud-community-protocols/en/
[firmware]: https://github.com/phicomm-io/iotcloud-community-firmware
[frontend]: https://github.com/phicomm-io/iotcloud-community-frontend
[platform]: https://github.com/phicomm-io/iotcloud-community-mqtt
[mcu]: https://github.com/phicomm-io/phicomm_m1_mcu_atsamd20
[website]: https://github.com/phicomm-io/phicomm-io.github.io
[issues]: https://github.com/phicomm-io/.github/issues
[qq]: https://qm.qq.com/q/9L150V85kk?from=tim
