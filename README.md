<h1 align="center">🌊 Smart Aquarium V2.0 🐠</h1>

<div align="center">

![GitHub last commit](https://img.shields.io/github/last-commit/desifish/Smart-Aquarium-V2.0?style=for-the-badge&color=green)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge)](https://www.gnu.org/licenses/gpl-3.0)
![Project Status: Closed](https://img.shields.io/badge/Project%20Status-Closed-red?style=for-the-badge)

<h3>🎛️ IoT-Based Aquarium Automation System</h3>
<p>Control your aquarium using a web interface!</p>
</div>

> ⚠️ **CAUTION**: This project involves working with electrical components and may require handling of high voltage connections. Always prioritize safety, use proper insulation, and consult with a qualified electrician if you're unsure about any aspect of the installation or operation.

> 📢 **NOTE**: This project (V2.0) is now closed. For the latest updates and improvements, please check out [Smart Aquarium V3.0](https://github.com/desiFish/Smart-Aquarium-V3.0).

## ✨ Features

- 🌐 Web-based control interface 
- ⏰ Automated timing controls
- 🌡️ Real-time temperature monitoring
- 💡 Smart lighting control
- 🔄 Power-saving modes
- 📱 Mobile-responsive design
- 🔄 OTA (Over-The-Air) updates
- ⚡ Low latency control

## 🛠️ Hardware Required

<table align="center">
<tr>
<th>Component</th>
<th>Image</th>
<th>Purpose</th>
</tr>
<tr>
<td>NodeMCU ESP8266</td>
<td><img src="https://m.media-amazon.com/images/I/51lIrI5vnQL.jpg" width="100"></td>
<td>Main controller with WiFi capabilities</td>
</tr>
<tr>
<td>DS3231 RTC Module</td>
<td><img src="https://m.media-amazon.com/images/I/41RP9FjC+jL.jpg" width="100"></td>
<td>Accurate time keeping</td>
</tr>
<tr>
<td>OLED Display</td>
<td><img src="https://www.electronicscomp.com/image/cache/catalog/13-inch-i2c-iic-oled-display-module-4pin-white-800x800.jpg" width="100"></td>
<td>Status display</td>
</tr>
<tr>
<td>4-Channel Relay</td>
<td><img src="https://m.media-amazon.com/images/I/71TWos73PrL._SL1100_.jpg" width="100"></td>
<td>Control aquarium equipment</td>
</tr>
</table>

## 📥 Installation

```bash
# Clone this repository
git clone https://github.com/desifish/Smart-Aquarium-V2.0.git

# Navigate to the directory
cd Smart-Aquarium-V2.0

# Open in Arduino IDE
# Update WiFi credentials in aqua_NODEMCU.ino
# Flash to NodeMCU
```

> **Important**: The favicon image inside the `data` folder needs to be copied into the flash storage of the NodeMCU. This ensures the web interface can properly display the favicon. For instructions on how to upload files to the ESP8266 filesystem using LittleFS, please refer to [this updated guide](https://randomnerdtutorials.com/install-esp8266-nodemcu-littlefs-arduino/).

## 📝 Documentation

<details>
<summary>📌 Version History</summary>

- v1.12 - Added Power Saver Mode
- v1.11 - Updated UI with customizable timers
- v1.10 - Added auto-start relay feature
- v1.9 - Added web-based time updates
- v1.8 - Added Auto/Manual Control
</details>

<details>
<summary>🔌 Wiring Diagram</summary>

```
NodeMCU ESP8266 -> OLED Display
D1 -> SCL
D2 -> SDA
3.3V -> VCC
GND -> GND

NodeMCU ESP8266 -> DS3231
D1 -> SCL
D2 -> SDA
3.3V -> VCC
GND -> GND

NodeMCU ESP8266 -> 4 Channel Relay
D0 -> IN1
D6 -> IN2
D7 -> IN3
D5 -> IN4
5V -> VCC
GND -> GND
```

</details>

## 📱 Web Interface

The system provides an intuitive web interface accessible from any device on your network:

- 💻 Desktop View
- 📱 Mobile-Responsive
- 🎛️ Real-time Controls
- 📊 Status Monitoring

### Web Interface
<img src="https://github.com/aniket-patra/aqua_NODEMCU/blob/main/resources/aa.jpg" alt="Web Interface" width="800" height="400">

## 🔒 License

This project is licensed under GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

### GNU General Public License v3.0

<details>
<summary>License Details</summary>

Permissions:
- ✅ Commercial use
- ✅ Modification
- ✅ Distribution
- ✅ Patent use
- ✅ Private use

Conditions:
- 📝 License and copyright notice
- 📄 State changes
- 📦 Disclose source
- 📜 Same license

Limitations:
- ❌ Liability
- ❌ Warranty

</details>

---

<div align="center">

Made with ❤️ for the IoT Community

[![Follow on GitHub](https://img.shields.io/github/followers/desifish?style=social)](https://github.com/desifish)

</div>
```
