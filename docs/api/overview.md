# API Reference

This section provides comprehensive documentation for all SHModbus classes and functions.

## Core Classes

### ModbusTCPClient

The `ModbusTCPClient` class provides Modbus TCP communication capabilities.

```python
class ModbusTCPClient:
    def __init__(self, host, port=502, timeout=3.0):
        """
        Initialize a Modbus TCP client.
        
        Args:
            host (str): The hostname or IP address of the Modbus server
            port (int): The port number (default: 502)
            timeout (float): Connection timeout in seconds (default: 3.0)
        """
```

#### Methods

##### connect()
Establish connection to the Modbus TCP server.

**Returns:** `bool` - True if connection successful, False otherwise

##### close()
Close the connection to the Modbus server.

##### read_coils(address, count, unit=1)
Read coils from the Modbus device.

**Parameters:**
- `address` (int): Starting address
- `count` (int): Number of coils to read
- `unit` (int): Unit ID (default: 1)

**Returns:** `ModbusResponse` - Response containing coil values

##### read_holding_registers(address, count, unit=1)
Read holding registers from the Modbus device.

**Parameters:**
- `address` (int): Starting address
- `count` (int): Number of registers to read
- `unit` (int): Unit ID (default: 1)

**Returns:** `ModbusResponse` - Response containing register values

### ModbusRTUClient

The `ModbusRTUClient` class provides Modbus RTU communication over serial.

```python
class ModbusRTUClient:
    def __init__(self, port, baudrate=9600, bytesize=8, parity='N', stopbits=1, timeout=3.0):
        """
        Initialize a Modbus RTU client.
        
        Args:
            port (str): Serial port name (e.g., 'COM1', '/dev/ttyUSB0')
            baudrate (int): Baud rate (default: 9600)
            bytesize (int): Number of data bits (default: 8)
            parity (str): Parity ('N', 'E', 'O') (default: 'N')
            stopbits (int): Number of stop bits (default: 1)
            timeout (float): Read timeout in seconds (default: 3.0)
        """
```

## Response Classes

### ModbusResponse

All read operations return a `ModbusResponse` object.

#### Properties

- `registers` (list): List of register values (for register reads)
- `bits` (list): List of bit values (for coil/discrete input reads)
- `isError()` (method): Returns True if the response contains an error

## Exception Classes

### ModbusException

Base exception class for all Modbus-related errors.

### ModbusConnectionError

Raised when connection to the Modbus device fails.

### ModbusTimeoutError

Raised when a Modbus operation times out.

## Constants

### Function Codes

- `READ_COILS = 0x01`
- `READ_DISCRETE_INPUTS = 0x02`
- `READ_HOLDING_REGISTERS = 0x03`
- `READ_INPUT_REGISTERS = 0x04`
- `WRITE_SINGLE_COIL = 0x05`
- `WRITE_SINGLE_REGISTER = 0x06`
- `WRITE_MULTIPLE_COILS = 0x0F`
- `WRITE_MULTIPLE_REGISTERS = 0x10`