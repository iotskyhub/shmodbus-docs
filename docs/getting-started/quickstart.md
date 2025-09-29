# Quick Start

This guide will get you up and running with SHModbus in just a few minutes.

## Your First Modbus TCP Client

Here's a simple example that connects to a Modbus TCP server and reads some holding registers:

```python
from shmodbus import ModbusTCPClient

# Create a client instance
client = ModbusTCPClient('192.168.1.100', port=502)

try:
    # Connect to the server
    client.connect()
    
    # Read 10 holding registers starting from address 0
    result = client.read_holding_registers(0, 10)
    
    if result.isError():
        print(f"Error: {result}")
    else:
        print(f"Registers: {result.registers}")
        
finally:
    # Always close the connection
    client.close()
```

## Your First Modbus RTU Client

Here's how to communicate with a Modbus RTU device over serial:

```python
from shmodbus import ModbusRTUClient

# Create an RTU client
client = ModbusRTUClient(
    port='COM1',  # or '/dev/ttyUSB0' on Linux
    baudrate=9600,
    bytesize=8,
    parity='N',
    stopbits=1
)

try:
    # Connect to the serial port
    client.connect()
    
    # Read input registers from slave ID 1
    result = client.read_input_registers(0, 5, unit=1)
    
    if result.isError():
        print(f"Error: {result}")
    else:
        print(f"Input registers: {result.registers}")
        
finally:
    client.close()
```

## Writing Data

You can also write data to Modbus devices:

```python
from shmodbus import ModbusTCPClient

client = ModbusTCPClient('192.168.1.100')

try:
    client.connect()
    
    # Write a single coil
    result = client.write_coil(0, True)
    
    # Write multiple holding registers
    values = [100, 200, 300]
    result = client.write_multiple_registers(0, values)
    
finally:
    client.close()
```

## Next Steps

- Explore the [API Reference](../api/overview.md) for complete documentation
- Check out more [Examples](../examples/basic.md) for advanced usage
- Learn about error handling and best practices