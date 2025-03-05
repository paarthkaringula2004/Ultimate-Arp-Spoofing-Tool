# Ultimate ARP Spoofing Tool

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8+-orange.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

##  Overview
**Ultimate ARP Spoofing Tool** is a powerful network security and penetration testing tool designed for advanced network packet analysis and ARP spoofing. Built with Python, it provides real-time monitoring, pattern-based traffic analysis, and comprehensive reporting interfaces.

##  Key Features

###  Network Analysis
- Real-time packet capture and filtering
- Pattern-based traffic monitoring
- MAC address resolution
- Hostname detection

###  ARP Operations
- Smart gateway detection
- Target device mapping
- Traffic interception
- Custom packet injection rules

###  Reporting & Export
- Interactive HTML reports
- JSON data export
- CSV compatibility
- Plain text logs

---

##  Screenshots

### ARP Spoofing in Action

![Application Running](https://github.com/paarthkaringula2004/Project-Images-Video/blob/main/Images-Videos/Ultimate-Arp-Spoofing-Tool/Application%20Running.jpg)

*Displays the status of the ARP spoofing attack.*

### Packet Capture Overview

![Packet Capture](https://github.com/paarthkaringula2004/Project-Images-Video/blob/main/Images-Videos/Ultimate-Arp-Spoofing-Tool/Packet%20Capture.jpg)

*Real-time capture showing intercepted packets with source and destination details.*

### Export Format Options

![Export Format Options](https://github.com/paarthkaringula2004/Project-Images-Video/blob/main/Images-Videos/Ultimate-Arp-Spoofing-Tool/Export%20Format%20Options.jpg)

*Export captured data in multiple formats: HTML, JSON, CSV, and plain text.*

### HTML Report

![HTML Report](https://github.com/paarthkaringula2004/Project-Images-Video/blob/main/Images-Videos/Ultimate-Arp-Spoofing-Tool/HTML%20Report.jpg)

*Generated HTML report providing detailed network analysis.*

---

##  Quick Start

### ⚠️ Important Precautions
Before using **Ultimate ARP Spoofing Tool**, ensure the following:

1. **Use a compatible WiFi adapter**  
   Recommended: **TP-Link Archer T2U Plus (AC600)**
   
   ![WiFi Adapter](https://github.com/paarthkaringula2004/Project-Images-Video/blob/main/Images-Videos/Ultimate-Arp-Spoofing-Tool/tp-link-adapter.jpg)
   
   - [Amazon India](https://www.amazon.in/tp-link-archer-t2u-plus/s?k=tp+link+archer+t2u+plus)  
   - [Flipkart](https://www.flipkart.com/tp-link-archer-t2u-plus-ac600-high-gain-wireless-dual-band-usb-adapter/p/itm78f701f57c630)  
   - [TP-Link Official Store](https://www.tp-link.com/in/home-networking/high-gain-adapter/archer-t2u-plus/)

2. **Change the MAC Address:**
   ```sh
   sudo ifconfig wlan1 down  
   sudo ifconfig wlan1 hw ether 00:11:22:33:44:55  
   sudo ifconfig wlan1 up  
   ```

3. **Enable Monitor Mode:**
   ```sh
   sudo airmon-ng check kill  
   sudo ifconfig wlan1 down  
   sudo iwconfig wlan1 mode monitor  
   sudo ifconfig wlan1 up  
   ```

### Installation
```bash
# Clone the repository
git clone https://github.com/paarthkaringula2004/Ultimate-Arp-Spoofing-Tool.git
cd Ultimate-Arp-Spoofing-Tool

# Install dependencies
pip install -r requirements-dev.txt
```

### Running the Tool
```bash
# Linux/macOS
sudo python -m src

# Windows (Run PowerShell/CMD as Administrator)
python -m src
```
> **Note**: Root/Administrator privileges are required for network operations.

---

##  Usage Examples

### Basic Monitoring:
```bash
sudo python -m src --target [TARGET IP]
```

### Pattern Matching:
```bash
sudo python -m src --patterns "HTTP,FTP"
```

### Exporting Data:
```bash
sudo python -m src --format json
```

### Full Example:
```bash
sudo python -m src -t [TARGET IP] -g [GATEWAY IP] -p "password" "secret" -f html
```

---

## 📋 Command Options
| Option       | Description           | Default       |
|--------------|-----------------------|---------------|
| -t, --target | Target IP address     | Auto-detect   |
| -g, --gateway| Gateway IP address    | Auto-detect   |
| -p, --patterns| Search patterns      | None          |
| -f, --format | Export format         | html          |

---

## 📁 Project Structure
```
src/
├── core/          # Core functionality
├── network/       # Network operations
├── spoofer/       # ARP spoofing implementation
├── models/        # Data models
└── utils/         # Helper functions
```

---

## 📦 Dependencies
- **scapy** - Network packet manipulation
- **rich** - Terminal UI components
- **netifaces** - Network interface handling
- **jinja2** - Report templating

---

##  Development
```bash
# Set up development environment
python -m venv venv
source venv/Scripts/activate  # Windows
pip install -r requirements-dev.txt
```

---

##  Security Notice
**This tool is intended for educational and security testing purposes only.**
Use it responsibly on networks where you have explicit permission.

---

##  Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Submit a pull request

---

##  License
**MIT License**

---

##  Author
- **Paarth Karingula**  
  - GitHub: [@paarthkaringula2004](https://github.com/paarthkaringula2004)
  - LinkedIn: [Paarth Karingula](https://www.linkedin.com/in/paarthkaringula2004)

💬 **Support**
For issues, report them on [GitHub](https://github.com/paarthkaringula2004/Ultimate-Arp-Spoofing-Tool/issues).

