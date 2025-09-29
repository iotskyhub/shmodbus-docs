# Contributing

We welcome contributions to SHModbus! This document provides guidelines for contributing to the project.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/yourusername/shmodbus.git
   cd shmodbus
   ```
3. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. **Install development dependencies**:
   ```bash
   pip install -e ".[dev]"
   ```

## Development Workflow

### 1. Create a Branch

Create a new branch for your feature or bug fix:

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

### 2. Make Your Changes

- Write clear, concise code
- Follow the existing code style
- Add tests for new functionality
- Update documentation as needed

### 3. Run Tests

Before submitting your changes, make sure all tests pass:

```bash
# Run all tests
pytest

# Run tests with coverage
pytest --cov=shmodbus

# Run specific test file
pytest tests/test_tcp_client.py
```

### 4. Code Style

We use several tools to maintain code quality:

```bash
# Format code with black
black shmodbus tests

# Sort imports with isort
isort shmodbus tests

# Check code style with flake8
flake8 shmodbus tests

# Type checking with mypy
mypy shmodbus
```

### 5. Commit Your Changes

Write clear commit messages:

```bash
git add .
git commit -m "Add support for Modbus exception handling

- Implement proper exception classes
- Add timeout handling for TCP connections
- Update tests for new exception types"
```

### 6. Push and Create Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a pull request on GitHub.

## Code Style Guidelines

### Python Code Style

- Follow [PEP 8](https://pep8.org/) style guidelines
- Use [Black](https://black.readthedocs.io/) for code formatting
- Use [isort](https://isort.readthedocs.io/) for import sorting
- Maximum line length: 88 characters (Black default)

### Documentation Style

- Use [Google style docstrings](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings)
- Include type hints for all public functions
- Write clear, concise documentation

Example:

```python
def read_holding_registers(
    self, 
    address: int, 
    count: int, 
    unit: int = 1
) -> ModbusResponse:
    """Read holding registers from the Modbus device.
    
    Args:
        address: Starting register address (0-based)
        count: Number of registers to read (1-125)
        unit: Unit ID of the target device (default: 1)
    
    Returns:
        ModbusResponse containing the register values or error information
        
    Raises:
        ModbusConnectionError: If not connected to the device
        ModbusTimeoutError: If the operation times out
        ValueError: If address or count is out of valid range
    """
```

## Testing Guidelines

### Writing Tests

- Write tests for all new functionality
- Use descriptive test names
- Include both positive and negative test cases
- Test error conditions and edge cases

Example:

```python
def test_read_holding_registers_success():
    """Test successful reading of holding registers."""
    client = ModbusTCPClient('localhost', 502)
    # ... test implementation

def test_read_holding_registers_invalid_address():
    """Test error handling for invalid register address."""
    client = ModbusTCPClient('localhost', 502)
    # ... test implementation
```

### Test Categories

- **Unit tests**: Test individual functions and methods
- **Integration tests**: Test component interactions
- **End-to-end tests**: Test complete workflows

## Documentation

### API Documentation

- All public classes and methods must have docstrings
- Include examples in docstrings when helpful
- Use type hints consistently

### User Documentation

- Update relevant documentation pages for new features
- Include code examples for new functionality
- Keep the README.md up to date

## Reporting Issues

When reporting bugs or requesting features:

1. **Check existing issues** first to avoid duplicates
2. **Use issue templates** when available
3. **Provide detailed information**:
   - Python version
   - SHModbus version
   - Operating system
   - Complete error messages
   - Minimal code example to reproduce the issue

## Pull Request Guidelines

### Before Submitting

- [ ] All tests pass
- [ ] Code follows style guidelines
- [ ] Documentation is updated
- [ ] Commit messages are clear
- [ ] Branch is up to date with main

### Pull Request Description

Include in your PR description:

- **What**: Brief description of changes
- **Why**: Reason for the changes
- **How**: Implementation approach (if complex)
- **Testing**: How you tested the changes

### Review Process

1. **Automated checks** must pass (CI/CD)
2. **Code review** by maintainers
3. **Discussion** and iteration if needed
4. **Merge** once approved

## Release Process

Releases are handled by maintainers and follow semantic versioning:

- **Major version** (1.0.0): Breaking changes
- **Minor version** (0.1.0): New features, backward compatible
- **Patch version** (0.0.1): Bug fixes, backward compatible

## Questions?

If you have questions about contributing:

- Open an issue for discussion
- Check existing documentation
- Contact the maintainers

Thank you for contributing to SHModbus!