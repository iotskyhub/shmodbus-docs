# Installation

This guide will help you install SHModbus and get it ready for use.

## Requirements

- Python 3.7 or higher
- pip (Python package installer)

## Installation Methods

### Install from PyPI (Recommended)

```bash
pip install shmodbus
```

### Install from Source

If you want the latest development version:

```bash
git clone https://github.com/pjdgsolutions/shmodbus.git
cd shmodbus
pip install -e .
```

## Verify Installation

To verify that SHModbus is installed correctly, run:

```python
import shmodbus
print(shmodbus.__version__)
```

## Dependencies

SHModbus automatically installs the following dependencies:

- `pyserial` - For serial communication (Modbus RTU)
- `socket` - For TCP communication (built-in with Python)

## Next Steps

Once installed, head over to the [Quick Start](quickstart.md) guide to create your first SHModbus application.