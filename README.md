# Ultimate ARP Spoofing Tool 🌐

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8+-orange.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

## 🎯 Overview
Advanced network packet analysis and ARP spoofing tool built with Python. Featuring pattern matching, real-time monitoring, and beautiful reporting interfaces.

## ✨ Key Features

🔍 **Network Analysis**
- Real-time packet capture and filtering
- Pattern-based traffic monitoring
- MAC address resolution
- Hostname detection

🛡️ **ARP Operations**
- Smart gateway detection
- Target device mapping
- Traffic interception
- Custom packet rules

📊 **Reporting & Export**
- Interactive HTML reports
- JSON data export
- CSV compatibility
- Plain text logs

## 🖥️ Screenshots

### ARP Spoofing Tool in Action

![Application Running]()

*Initializes the tool and displays the status of the ARP spoofing attack.*

### Packet Capture Overview

![Packet Capture]()

*Real-time packet capture showing intercepted network packets with source and destination details. (Press **Ctrl+C** to stop packet capturing)* 

### Export Format Options

![Export Format Options]()

*Options for exporting captured data in various formats such as HTML, JSON, CSV, and plain text.*

### HTML Report

![HTML Report]()

*Generated HTML report providing a detailed analysis of the captured packets.*


## 🚀 Quick Start

## ⚠️ Precautions Before Using **Ultimate Arp Spoofing Tool**  
🛡️ Follow these steps to stay secure & undetected:

1. **Use a compatible WiFi adapter**  
   Recommended: **TP-Link Archer T2U Plus (AC600)**
   
   ![Recommended WiFi Adapter](https://github.com/paarthkaringula2004/Ultimate-Spoof-Caplet/blob/main/images/tp-link-adapter.jpg)
   
   - [Amazon India](https://www.amazon.in/tp-link-archer-t2u-plus/s?k=tp+link+archer+t2u+plus)  
   - [Flipkart](https://www.flipkart.com/tp-link-archer-t2u-plus-ac600-high-gain-wireless-dual-band-usb-adapter/p/itm78f701f57c630)  
   - [TP-Link Official Store](https://www.tp-link.com/in/home-networking/high-gain-adapter/archer-t2u-plus/)

3. **Change the MAC Address:**  
   ```sh
   sudo ifconfig wlan1 down  
   sudo ifconfig wlan1 hw ether 00:11:22:33:44:55  
   sudo ifconfig wlan1 up  
   ```
4. **Enable Monitor Mode:**  
   ```sh
   sudo airmon-ng check kill  
   sudo ifconfig wlan1 down  
   sudo iwconfig wlan1 mode monitor  
   sudo ifconfig wlan1 up  
   ```
```bash
# Clone repository
https://github.com/paarthkaringula2004/Ultimate-Arp-Spoofing-Tool.git
cd Ultimate Arp Spoof
```

### Install dependencies
```bash
pip install -r requirements-dev.txt
```

### Run with default settings
```bash
# Linux/macOS
sudo python -m src

# Windows (run PowerShell/CMD as Administrator)
python -m src
```

> ⚠️ **Note**: Root/Administrator privileges are required for network operations

## 💻 **Usage Examples**

### Basic Monitoring:
```bash
# Linux/macOS
sudo python -m src --target [TARGET IP]

# Windows (run PowerShell/CMD as Administrator)
python -m src --target [TARGET IP]
```

### Pattern Matching:
```bash
# Linux/macOS
sudo python -m src --patterns "HTTP,FTP"

# Windows (run PowerShell/CMD as Administrator)
python -m src --patterns "HTTP,FTP"
```

### Custom Export:
```bash
# Linux/macOS
sudo python -m src --format json

# Windows (run PowerShell/CMD as Administrator)
python -m src --format json
```

### Example:
```bash
# Linux/macOS
    sudo python -m src -t [TARGET IP] -g [GATEWAY IP] -p "password" "secret" -f html

# Windows (run PowerShell/CMD as Administrator)
python -m src -t [TARGET IP] -g [GATEWAY IP] -p "password" "secret" -f html
```

## 📋 **Command Options**

| Option       | Description           | Default       |
|--------------|-----------------------|---------------|
| -t, --target | Target IP address     | Auto-detect   |
| -g, --gateway| Gateway IP address    | Auto-detect   |
| -p, --patterns| Search patterns      | None          |
| -f, --format | Export format         | html          |

## 📁 **Project Structure**
```
src/
├── core/          # Core functionality
├── network/       # Network operations
├── spoofer/       # ARP implementation
├── models/        # Data models
└── utils/         # Helper functions
```

## 📦 **Dependencies**
- scapy - Network packet manipulation
- rich - Terminal UI components
- netifaces - Network interface handling
- jinja2 - Report templating

## 🔧 **Development**
```bash
# Setup development environment
python -m venv venv
source venv/Scripts/activate  # Windows
pip install -r requirements-dev.txt
```

## ⚠️ **Security Notice**
Educational Purposes Only: This tool should only be used on networks where you have explicit permission to test.

## 🤝 **Contributing**
1. Fork repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Submit pull request

## 📜 **License**
MIT License

## 👤 **Author**
- **Paarth Karingula**  
  - GitHub: [@paarthkaringula2004](https://github.com/paarthkaringula2004)
  - LinkedIn: [Paarth Karingula](https://www.linkedin.com/in/paarthkaringula2004)

💬 **Support**
Report issues on GitHub
