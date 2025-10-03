# SHModbus Documentation

This repository contains the documentation for **SHModbus** - a real-time industrial data monitoring and visualization application that connects to Modbus devices.

## 🌍 Multi-language Support

Documentation is available in 4 languages:
- 🇵🇱 **Polski** (Polish)
- 🇬🇧 **English** 
- 🇩🇪 **Deutsch** (German)
- 🇫🇷 **Français** (French)

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
├── index.md                 # Main language selection page
├── version.json             # Version information for SHModbus Client
├── shared-images/           # Shared images across all languages
│   └── shmodbus-app.png
├── pl/                      # Polish documentation
│   └── index.md
├── en/                      # English documentation
│   └── index.md
├── de/                      # German documentation
│   └── index.md
└── fr/                      # French documentation
    └── index.md
```

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
- **Author**: IoT Sky Hub