# Basic Usage Examples

This page contains practical examples showing how to use SHModbus in real-world scenarios.

## Reading Sensor Data

Here's how to read temperature and humidity data from a Modbus device:

```python
from shmodbus import ModbusTCPClient
import time

def read_sensor_data():
    client = ModbusTCPClient('192.168.1.50', port=502)
    
    try:
        client.connect()
        
        # Read temperature from register 0 (assume it's in tenths of degrees)
        temp_result = client.read_holding_registers(0, 1)
        if not temp_result.isError():
            temperature = temp_result.registers[0] / 10.0
            print(f"Temperature: {temperature}°C")
        
        # Read humidity from register 1 (assume it's in tenths of percent)
        humidity_result = client.read_holding_registers(1, 1)
        if not humidity_result.isError():
            humidity = humidity_result.registers[0] / 10.0
            print(f"Humidity: {humidity}%")
            
    except Exception as e:
        print(f"Error reading sensor data: {e}")
    finally:
        client.close()

# Read data every 10 seconds
while True:
    read_sensor_data()
    time.sleep(10)
```

## Controlling Outputs

Example of controlling digital outputs and setting analog values:

```python
from shmodbus import ModbusTCPClient

def control_outputs():
    client = ModbusTCPClient('192.168.1.100')
    
    try:
        client.connect()
        
        # Turn on output 1 (coil address 0)
        result = client.write_coil(0, True)
        if result.isError():
            print("Failed to turn on output 1")
        else:
            print("Output 1 turned ON")
        
        # Turn off output 2 (coil address 1)
        result = client.write_coil(1, False)
        if result.isError():
            print("Failed to turn off output 2")
        else:
            print("Output 2 turned OFF")
        
        # Set analog output value (register address 100)
        analog_value = 2500  # Example: 2.5V represented as 2500 millivolts
        result = client.write_single_register(100, analog_value)
        if result.isError():
            print("Failed to set analog output")
        else:
            print(f"Analog output set to {analog_value}")
            
    except Exception as e:
        print(f"Error controlling outputs: {e}")
    finally:
        client.close()

control_outputs()
```

## Batch Operations

Reading multiple registers efficiently:

```python
from shmodbus import ModbusTCPClient

def read_multiple_sensors():
    client = ModbusTCPClient('192.168.1.75')
    
    try:
        client.connect()
        
        # Read 10 consecutive registers starting from address 0
        result = client.read_holding_registers(0, 10)
        
        if not result.isError():
            registers = result.registers
            
            # Process the data (example: each register represents a different sensor)
            sensors = {
                'temperature_1': registers[0] / 10.0,
                'temperature_2': registers[1] / 10.0,
                'humidity_1': registers[2] / 10.0,
                'humidity_2': registers[3] / 10.0,
                'pressure': registers[4] / 100.0,  # Pressure in Pa
                'flow_rate': registers[5] / 100.0,  # Flow rate in L/min
                'level': registers[6],  # Tank level in cm
                'ph_value': registers[7] / 100.0,  # pH value
                'conductivity': registers[8],  # Conductivity in µS/cm
                'turbidity': registers[9] / 10.0,  # Turbidity in NTU
            }
            
            for sensor, value in sensors.items():
                print(f"{sensor}: {value}")
        else:
            print(f"Error reading sensors: {result}")
            
    except Exception as e:
        print(f"Connection error: {e}")
    finally:
        client.close()

read_multiple_sensors()
```

## Error Handling and Retry Logic

Robust code with proper error handling:

```python
from shmodbus import ModbusTCPClient, ModbusConnectionError, ModbusTimeoutError
import time

class ModbusReader:
    def __init__(self, host, port=502, max_retries=3):
        self.host = host
        self.port = port
        self.max_retries = max_retries
        self.client = None
    
    def connect(self):
        """Connect with retry logic"""
        for attempt in range(self.max_retries):
            try:
                self.client = ModbusTCPClient(self.host, self.port)
                self.client.connect()
                print(f"Connected to {self.host}:{self.port}")
                return True
            except ModbusConnectionError:
                print(f"Connection attempt {attempt + 1} failed")
                if attempt < self.max_retries - 1:
                    time.sleep(2)  # Wait before retry
                else:
                    print("All connection attempts failed")
                    return False
    
    def read_with_retry(self, address, count, unit=1):
        """Read registers with retry logic"""
        for attempt in range(self.max_retries):
            try:
                result = self.client.read_holding_registers(address, count, unit)
                if not result.isError():
                    return result.registers
                else:
                    print(f"Modbus error: {result}")
            except ModbusTimeoutError:
                print(f"Timeout on attempt {attempt + 1}")
            except Exception as e:
                print(f"Unexpected error: {e}")
            
            if attempt < self.max_retries - 1:
                time.sleep(1)  # Wait before retry
        
        return None
    
    def close(self):
        if self.client:
            self.client.close()

# Usage
reader = ModbusReader('192.168.1.100')
if reader.connect():
    data = reader.read_with_retry(0, 5)
    if data:
        print(f"Successfully read data: {data}")
    else:
        print("Failed to read data after all retries")
    reader.close()
```

## Serial RTU Example

Working with Modbus RTU over serial:

```python
from shmodbus import ModbusRTUClient
import serial.tools.list_ports

def list_serial_ports():
    """List available serial ports"""
    ports = serial.tools.list_ports.comports()
    for port in ports:
        print(f"Port: {port.device}, Description: {port.description}")

def read_rtu_device():
    # List available ports first
    print("Available serial ports:")
    list_serial_ports()
    
    # Connect to RTU device
    client = ModbusRTUClient(
        port='COM3',  # Change to your port
        baudrate=9600,
        bytesize=8,
        parity='N',
        stopbits=1,
        timeout=2.0
    )
    
    try:
        client.connect()
        print("Connected to RTU device")
        
        # Read from slave device with ID 1
        result = client.read_holding_registers(0, 4, unit=1)
        
        if not result.isError():
            print(f"Registers from slave 1: {result.registers}")
        else:
            print(f"Error: {result}")
            
        # Try reading from slave device with ID 2
        result = client.read_input_registers(0, 2, unit=2)
        
        if not result.isError():
            print(f"Input registers from slave 2: {result.registers}")
        else:
            print(f"Error: {result}")
            
    except Exception as e:
        print(f"RTU communication error: {e}")
    finally:
        client.close()

read_rtu_device()
```