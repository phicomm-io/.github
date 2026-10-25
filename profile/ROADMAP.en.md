# IoTCloud community roadmap

[简体中文](https://github.com/phicomm-io/.github/blob/main/profile/ROADMAP.md) · [Project home](https://phicomm-io.github.io/en/) · [Project board](https://github.com/orgs/phicomm-io/projects/3)

## Available now

TC1 A1 hardware, M1, A1 and the documented DAIKIN devices have 0.9.x firmware, installation guides and release archives. Local WebUI, MQTT, Home Assistant and IoTCloud are available. The M1 sensor controller has separate GPL-3.0 releases, recommended for stock 11.x; migration from 17.1.2.3 / 17.x is currently discouraged.

## v1.0 in development

v1.0 has not been released. These features still require integration and physical-device validation. There are no v1 downloads.

| Area | Planned work |
| --- | --- |
| Use and updates | Chinese / English interfaces, device language, configuration backup and restore, migration recovery and upgrade comparisons |
| M1 | Independent user readings, colors and validity periods in the formaldehyde / PM2.5 positions; one double click switches both original / user displays, and an invalid lane returns to its original reading. Sources include local sensors, TC1 power (W), A1 main-fan output (0–100%, not measured RPM), DAIKIN or the API; the glass gains no new unit symbols. Steadier PM2.5 readings; separate formaldehyde / PM2.5 buzzer switches, off by default and independent of light thresholds, alarms and manual tones; matching controller, Wi-Fi firmware and frontend required |
| DAIKIN `hub` | Separate hub variant: configure its independent local account, TCP / WebSocket MQTT Broker, LAN Home Assistant, upstream MQTT client, Bemfa forwarding and HAP through the embedded WebUI (`/iotcloud/#/`). These services can run concurrently; each device's MQTT settings must point to the hub manually |
| Apple Home | HAP bridging on the DAIKIN hub; pairing, controls and recovery in the iPhone Home app still await physical-device acceptance. Matter support is not currently claimed |
| Open source and contributions | Maintain source under each repository’s license; pinned frontend artifacts, automated checks and contribution guidelines |

Interfaces, protocols and configuration contracts are maintained in the [bilingual developer documentation](https://phicomm-io.github.io/iotcloud-community-protocols/en/). Existing 0.9.x artifacts and notes remain available. Release records determine published availability.

## Future devices

DC1 and TC1 A2 remain future targets and are currently unsupported. Share devices or test results through the [project board](https://github.com/orgs/phicomm-io/projects/3) or [issues](https://github.com/phicomm-io/.github/issues).
