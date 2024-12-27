# Aquarium Automation using NodeMCU 12E

An automated aquarium control system that manages lights, filters, skimmers, and power heads with WiFi control, timers, and visual feedback.

## Features

- Control 4 different aquarium components independently
- WiFi-enabled remote control via web interface
- Automatic timers with customizable schedules
- Real-time clock with auto time sync
- OLED display showing status and temperature
- OTA (Over The Air) firmware updates
- Power saver modes for equipment
- Visual feedback with WiFi signal strength indicators

## Hardware Requirements

### Main Components

- NodeMCU-ESP8266 Development Board ESP12E
- 4 Channel 5V Relay Board Module with Optocouplers
- DS3231 AT24C32 IIC Precision RTC
- 1.3 Inch I2C IIC 128x64 OLED Display Module (White)
- Appropriate power supplies for NodeMCU and relays

### Pin Configuration

#### I2C Devices (DS3231 and OLED)
| NodeMCU | Device |
|---------|--------|
| D1      | SCL    |
| D2      | SDA    |
| 3.3V    | VCC    |
| GND     | GND    |

*Note: Both I2C devices share the same pins*

#### 4 Channel Relay Board
| NodeMCU | Relay |
|---------|-------|
| D3      | In1   |
| D5      | In2   |
| D6      | In3   |
| D7      | In4   |

## Installation

1. Add ESP8266 board support:
   - In Arduino IDE: File → Preferences → Additional Boards Manager URLs
   - Add: `http://arduino.esp8266.com/stable/package_esp8266com_index.json`

2. Install Required Libraries:
   - DS3231 (from https://github.com/NorthernWidget/DS3231/releases)
   - Other libraries via Arduino IDE Library Manager:
     - Adafruit GFX
     - Adafruit SSD1306
     - ESP8266WiFi
     - NTPClient

3. Configure WiFi:
   - Open `aqua_NODEMCU.ino`
   - Update `STASSID` and `STAPSK` with your WiFi credentials

## Important Notes

- **Power Supply**: Use separate power supplies for NodeMCU and relay board
  - Do not power relays from NodeMCU
  - Connect GND of both power supplies if using separate supplies

- **I2C Troubleshooting**: If experiencing I2C address conflicts:
  - Check device addresses
  - Adjust pull-up resistor values
  - Ensure proper power supply to I2C devices

## Web Interface

Access the control panel by navigating to the NodeMCU's IP address in a web browser.
Features:
- Manual/Auto mode switching
- Timer controls
- Power saver modes
- Temperature monitoring
- Time synchronization

## Support

For questions or issues, please contact through:
https://iotthings.pythonanywhere.com/contact

## Disclaimer

This code is provided as-is without any warranty. Use at your own risk.

## Images

### Relay Board
<img src="https://m.media-amazon.com/images/I/71TWos73PrL._SL1100_.jpg" alt="Relay Board" width="200" height="200">

### DS3231 RTC
<img src="https://m.media-amazon.com/images/I/41RP9FjC+jL.jpg" alt="DS3231" width="200" height="200">

### NodeMCU
<img src="https://m.media-amazon.com/images/I/51lIrI5vnQL.jpg" alt="NodeMCU" width="200" height="200">

### OLED Display
<img src="https://www.electronicscomp.com/image/cache/catalog/13-inch-i2c-iic-oled-display-module-4pin-white-800x800.jpg" alt="OLED" width="200" height="200">

### Web Interface
<img src="https://github.com/aniket-patra/aqua_NODEMCU/blob/main/aa.jpg" alt="Web Interface" width="800" height="400">
