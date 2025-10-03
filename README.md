# SHModbus Documentation

This repository contains the comprehensive documentation for **SHModbus** - a real-time industrial Modbus TCP/IP client application for monitoring and controlling Modbus devices.

## 📖 Documentation Content

- **Complete Getting Started Guide**: Step-by-step installation, setup, and configuration
- **Visual Interface Documentation**: Screenshots and detailed UI explanations
- **Platform Support**: Windows and Linux installation guides
- **Connection Management**: Modbus TCP/IP device connectivity
- **Device Configuration**: Network point setup and data collection
- **Troubleshooting**: Diagnostics and problem resolution

## 🚀 Live Documentation

Visit the live documentation: [https://iotskyhub.github.io/shmodbus-docs/](https://iotskyhub.github.io/shmodbus-docs/)

## 🛠️ Running Locally

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Setup and Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/iotskyhub/shmodbus-docs.git
   cd shmodbus-docs
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Serve the documentation locally**:
   ```bash
   mkdocs serve
   ```

4. **Open in browser**:
   Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your web browser

### Alternative Setup with Virtual Environment

1. **Create virtual environment**:
   ```bash
   python -m venv venv
   ```

2. **Activate virtual environment**:
   - **Windows**: `venv\Scripts\activate`
   - **macOS/Linux**: `source venv/bin/activate`

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the documentation**:
   ```bash
   mkdocs serve
   ```

## 📁 Project Structure

```
docs/
├── index.md                     # Main documentation homepage
├── en/
│   └── getting-started.md       # Comprehensive Getting Started guide
├── shared-images/               # Screenshots and visual guides
│   ├── linux-console.png
│   ├── linux-install.png
│   ├── shmodbus-add-connection.png
│   ├── shmodbus-add-device.png
│   ├── shmodbus-add-network-point.png
│   ├── shmodbus-login.png
│   ├── windows-app-host.png
│   ├── windows-console.png
│   └── windows-shortcuts.png
├── stylesheets/
│   └── extra.css               # Custom styling for images and layout
└── version.json                # Version information for SHModbus Client
```

## 📋 Getting Started Guide Features

The comprehensive Getting Started documentation includes:

### Installation & Setup
- **Platform-specific installers**: Windows (.exe) and Linux (.deb) packages
- **Visual installation guides**: Step-by-step screenshots for both platforms
- **Desktop shortcuts setup**: GUI and Console application options
- **Command-line arguments**: Advanced configuration options for ports and URLs

### Application Configuration
- **Web interface access**: Browser-based configuration and monitoring
- **User authentication**: Default login credentials and security setup
- **Connection management**: Modbus TCP/IP device connectivity
- **Device configuration**: Adding and managing multiple Modbus devices
- **Network points setup**: Register mapping and data collection configuration

### Advanced Features
- **Port configuration**: Custom ports, network interfaces, and accessibility
- **Data collection**: Real-time monitoring and automatic data polling
- **Diagnostics**: Connection testing and troubleshooting tools
- **Visual interface**: Screenshots for every configuration step

## 🔧 Version Information

The documentation includes a `version.json` file that SHModbus Client can read to get version information:

**URL**: `https://iotskyhub.github.io/shmodbus-docs/version.json`

**Local**: `http://127.0.0.1:8000/version.json`

## 🚀 Deployment

The documentation is automatically deployed to GitHub Pages using GitHub Actions when changes are pushed to the `main` branch.

### Manual Build

To build the documentation manually:

```bash
mkdocs build
```

This creates a `site/` directory with the static HTML files.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally with `mkdocs serve`
5. Submit a pull request

## 📄 License

This documentation is licensed under the MIT License.

## 📞 Support

- **Repository**: [https://github.com/iotskyhub/shmodbus-docs](https://github.com/iotskyhub/shmodbus-docs)
- **Issues**: [Report a bug or request a feature](https://github.com/iotskyhub/shmodbus-docs/issues)
- **Email**: contact@iotskyhub.com
- **Author**: IoT Sky Hub