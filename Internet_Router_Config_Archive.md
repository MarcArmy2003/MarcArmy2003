# 🌐 Internet and Router Configuration Archive
**As of 📅 August 10, 2025**

## 🖧 Spectrum Router Information
- **📶 Internet Status:** ✅ Connected
- **☁️ Cloud Status:** ✅ Connected
- **🌍 Public IPv4:** `173.170.164.12`
- **🪐 Public IPv6:** `2603:9000:ff00:7a:ec28:bb63:b2e4:61c8/128`
- **🔗 Router MAC Address:** `58:9B:4A:9D:0E:AE`
- **🏷 Serial Number:** `61RS23500086640`
- **📦 Model:** `SAX2V1R`
- **⚙️ Firmware Version:** `1.5.0-1-620922-g202503140018-SAX2V1R-prod`

---

## 📌 Reserved IP Addresses
| 💻 Device Name                                | 🖥 Device Type               | 🆔 MAC Address                                              | 🌐 Reserved IP                 | 📝 Notes                                                             |
| --------------------------------------------- | ---------------------------- | ----------------------------------------------------------- | ------------------------------ | -------------------------------------------------------------------- |
| **QNAP NAS (Plex Server)**                    | NAS / Media Server           | 24:5E:BE:87:82:8E                                            | 192.168.1.230                  | 🎬 Core Plex + storage; already set. Forward port 32401→32400 (TCP). |
| **Yamaha R-N800A**                            | Network Receiver             | *(Find in Yamaha settings → Network Info)*                  | 192.168.1.231                  | 🎵 Main audio hub, MusicCast source.                                 |
| **Bose Lifestyle 650**                        | AV Receiver                  | *(Find in Bose app or router device list)*                  | 192.168.1.232                  | 🎭 Theater system; stable IP helps with ARC/eARC & app control.      |
| **WiiM Pro Plus** *(future)*                  | Hi-Res Streaming Bridge      | *(TBD when purchased)*                                      | 192.168.1.233                  | 🔊 Will integrate Yamaha with other streaming devices.               |
| **Samsung 65” UHD Smart TV (Family Room)**    | Smart TV                     | *(Find in TV → Network Status)*                             | 192.168.1.234                  | 📺 Stable casting target.                                            |
| **Vizio TV (Security Monitor)**               | Smart TV                     | *(Find in Vizio settings → Network Info)*                   | 192.168.1.235                  | 🛡 Used for security dashboard casting.                              |
| **Nest Hub / Chromecast 1**                   | Smart Display / Streaming    | *(Find in Google Home app)*                                 | 192.168.1.236                  | 🎤 For multi-room audio & casting.                                   |
| **Chromecast 2**                              | Streaming Dongle             | *(Find in Google Home app)*                                 | 192.168.1.237                  | 📡 For casting to second display.                                    |
| **Ring Cameras / Doorbell**                   | Security Camera              | *(Each has unique MAC; find in Ring app or router list)*    | 192.168.1.240–192.168.1.242    | 🔔 Stable IP reduces “offline” errors.                               |
| **Main PC (GDMARCHE)**                        | Desktop                      | 98:E7:43:7C:BA:B8                                            | 192.168.1.210                  | 🖥 For NAS streaming & file sync.                                    |
| **Work Laptop**                               | Laptop                       | *(Find in VA laptop network settings)*                      | 192.168.1.211                  | 💼 Bridge Folder NAS access.                                         |

---

## 🚪 Port Forwarding Rules
| 🔧 Service                         | 🌍 External Port     | 🏠 Internal Port | 📡 Protocol | 💻 Internal IP   | 📝 Purpose                                |
| ---------------------------------- | ------------------- | ---------------- | ----------- | ---------------- | ----------------------------------------- |
| Plex Media Server                  | 32401               | 32400            | TCP         | 192.168.1.230    | 🎬 Remote Plex streaming                  |
| QNAP L2TP VPN *(optional)*         | 500 / 1701 / 4500   | same              | UDP         | 192.168.1.230    | 🔐 Only if using QNAP VPN                 |
| Security Dashboard *(optional)*    | 8080 (custom)       | 8080              | TCP         | 192.168.1.230    | 📷 Remote camera viewing from QNAP/Docker |

---

## 🗒 Notes
- 📌 Reserved IPs prevent DHCP changes that can break streaming, casting, or remote access.
- 📡 Only the Plex port forward is required for your current remote streaming use case.
- 🛡 Avoid exposing AV devices (Yamaha, WiiM, TVs) directly to the internet for security; prefer VPN or local-only access.
- 🔐 L2TP VPN rules are only needed if you intentionally use QNAP’s VPN service.
