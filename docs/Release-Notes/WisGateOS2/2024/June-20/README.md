---
release_date: 06/20/2024
version: "2.2.6"
release_note_description: Unified operative system for the WisGate Edge line that provides a feature-rich environment to access and configure the LoRaWAN gateway. The latest version of WisGateOS 2 is based on the latest version of the OpenWRT kernel for better security. WisGateOS 2 uses a simplified user interface that makes it easier to use and program. Integrated with WisDM, which allows the remote management of gateways and firmware. With extension functionality, the user can add extra features and functions to their gateways.
download_link: https://downloads.rakwireless.com/LoRa/WisGateOS2/WisGateOS2_Latest_Firmware.zip
logo: /assets/images/release-notes/WisGateOS2.png

---

<rk-release-notes/>

---

::: tip 📝 NOTE

WisGateOS 2 is available only for version 2 WisGate Edge gateways.
The supported models are as follows:
 - WisGate Edge Pro version 2: RAK7289V2, RAK7289CV2, RAK7289V2H, RAK7289CV2H
 - WisGate Edge Lite 2 version 2:  RAK7268V2, RAK7268CV2, RAK7268V2H, RAK7268CV2H
 - WisGate Edge Prime version 2: RAK7240V2, RAK7240CV2, RAK7240V2H, RAK7240CV2H

:::


:::warning ⚠️ IMPORTANT
- The WisGateOS2 firmware has been updated significantly. After this update, it is ***no longer possible*** to revert to previous versions of WisDM or the local WebUI. All WisGateOS2 2.2.x extensions are digitally signed. During this process, extensions will automatically update. Contact RAK support before updating the WireGuard Extension.
- An internet connection is mandatory for the update process. This is because the new firmware signature needs to be confirmed, and the Extension Gallery should be accessible to update the already installed extensions.
:::

## Added

| No. | Feature                                                     |
| --- | ----------------------------------------------------------- |
| 1   | WisDM agent updated to v1.2.7, optimizing the WAN failover. |

## Fixed

**WisGateOS2-related fixes:**

| No. | Description                                                                                                          |
| --- | -------------------------------------------------------------------------------------------------------------------- |
| 1   | Removed the link to the Offline Extensions - Online Extension Gallery is available.                                  |
| 2   | Tracking IPs update. Removed CN tracking IP for non CN gateways.                                                     |
| 3   | Supporting `%` symbol in the applications topics.                                                                    |
| 4   | In Basics Station mode, the GPS cannot be parsed - [`SYN:ERRO`] Failed to convert `xtime`.                           |
| 5   | Added special characters support in the MQTT password in Built-In NS mode.                                           |
| 6   | Some gateways running WisGateOS2 2.2.x cannot recognize the RS485 module.                                            |
| 7   | The whitelist function in Packet Forwarder mode is not turned off if the work mode is changed.                       |
| 8   | In Built-In work mode, if HTTP integration is configured for one Application, it will also be replicated for others. |
| 9   | WAN connection status is not properly updated for long time after it is disconnected.                                |



