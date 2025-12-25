# Embedded Systems Engineer Agent

Expert embedded systems engineer specializing in microcontroller programming, RTOS development, and hardware optimization. Masters low-level programming, real-time constraints, and resource-limited environments with focus on reliability, efficiency, and hardware-software integration.

## Overview

This agent is designed to assist with embedded systems development, from bare metal programming to complex RTOS implementations. It excels at working within resource constraints, optimizing for power consumption, and ensuring real-time performance requirements are met.

## Features

- **Microcontroller Programming**: Expertise across ARM Cortex-M, ESP32, STM32, Nordic nRF, PIC, AVR, and RISC-V platforms
- **RTOS Development**: Proficient in FreeRTOS, Zephyr, RT-Thread, and Mbed OS
- **Hardware Abstraction**: HAL development, driver interfaces, and board support packages
- **Communication Protocols**: I2C, SPI, UART, CAN, Modbus, MQTT, LoRaWAN, BLE, Zigbee
- **Power Management**: Sleep modes, clock gating, energy profiling, and battery optimization
- **Real-time Systems**: Task scheduling, interrupt management, and deadline handling
- **Memory Optimization**: Code size reduction, RAM minimization, and efficient data structures
- **Debugging**: JTAG/SWD, logic analyzers, profiling tools, and hardware breakpoints

## Slash Commands

### `/firmware-analyze`
Analyze existing firmware for performance, resource usage, and optimization opportunities.

**Use cases:**
- Review code size and RAM usage
- Identify power consumption bottlenecks
- Validate real-time constraints
- Find optimization opportunities
- Assess interrupt latency

**Example:**
```
/firmware-analyze
```

### `/memory-optimize`
Optimize memory usage for resource-constrained environments.

**Use cases:**
- Reduce code size
- Minimize RAM footprint
- Implement flash wear leveling
- Optimize data structures
- Configure memory pools

**Example:**
```
/memory-optimize
```

### `/driver-create`
Create hardware drivers with proper abstraction and error handling.

**Use cases:**
- Develop peripheral drivers (I2C, SPI, UART, etc.)
- Implement interrupt-driven I/O
- Add DMA support
- Create HAL abstractions
- Build sensor interfaces

**Example:**
```
/driver-create for SPI flash memory with DMA support
```

### `/rtos-config`
Configure RTOS settings for optimal real-time performance.

**Use cases:**
- Set task priorities
- Configure stack sizes
- Setup synchronization primitives
- Configure memory pools
- Optimize scheduling policies
- Define interrupt priorities

**Example:**
```
/rtos-config for FreeRTOS with 5 tasks
```

## Usage Guide

### Getting Started

1. **Installation**: Ensure you have the required MCP servers configured (filesystem, github, memory)
2. **Invocation**: Call the agent when working on embedded systems projects
3. **Context**: Provide hardware specifications, constraints, and requirements
4. **Collaboration**: The agent will analyze, implement, and optimize your embedded solution

### Typical Workflow

1. **System Analysis**
   - Review hardware specifications and datasheets
   - Assess resource constraints (flash, RAM, power)
   - Identify real-time requirements
   - Plan architecture and interfaces

2. **Implementation**
   - Configure hardware peripherals
   - Implement drivers and HAL
   - Setup RTOS (if needed)
   - Develop application logic
   - Optimize resources

3. **Validation**
   - Test real-time constraints
   - Measure power consumption
   - Verify memory usage
   - Profile performance
   - Document implementation

### Quality Checklist

The agent ensures all embedded systems meet these criteria:

- ✅ Code size optimized efficiently
- ✅ RAM usage minimized properly
- ✅ Power consumption < target achieved
- ✅ Real-time constraints met consistently
- ✅ Interrupt latency < 10µs maintained
- ✅ Watchdog implemented correctly
- ✅ Error recovery robust thoroughly
- ✅ Documentation complete accurately

## Hardware Platform Support

### Microcontrollers
- **ARM Cortex-M**: M0, M0+, M3, M4, M7, M33
- **ESP32/ESP8266**: WiFi/BLE enabled SoCs
- **STM32**: Full family support (F0-F7, H7, L0-L5, G0-G4)
- **Nordic nRF**: nRF52, nRF53, nRF91 series
- **PIC**: 8-bit, 16-bit, 32-bit microcontrollers
- **AVR**: Arduino and ATmega/ATtiny series
- **RISC-V**: Open-source processor cores
- **Custom ASICs**: Application-specific integrated circuits

### RTOS Support
- **FreeRTOS**: Industry-standard real-time kernel
- **Zephyr**: Scalable RTOS for IoT devices
- **RT-Thread**: Open-source embedded RTOS
- **Mbed OS**: ARM-based IoT operating system
- **Bare Metal**: Direct hardware programming

## Communication Protocols

- **Serial**: I2C, SPI, UART/USART
- **Automotive**: CAN bus, LIN
- **Industrial**: Modbus RTU/ASCII
- **IoT**: MQTT, CoAP, HTTP
- **Wireless**: BLE, Bluetooth Classic, Zigbee, LoRaWAN, WiFi
- **Custom**: Protocol design and implementation

## Performance Targets

- **Interrupt Latency**: < 10µs
- **Real-time Margin**: > 15%
- **Code Efficiency**: Optimized for resource-constrained devices
- **Power Consumption**: Minimized with sleep modes and power management

## Integration with Other Agents

The embedded systems agent collaborates with:

- **iot-engineer**: Connectivity and cloud integration
- **hardware-engineer**: Interface design and specifications
- **security-auditor**: Secure boot and cryptography
- **qa-expert**: Testing strategies and validation
- **devops-engineer**: Deployment and OTA updates
- **mobile-developer**: BLE and mobile app integration
- **performance-engineer**: Optimization and profiling
- **architect-reviewer**: System design and architecture

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File operations and project management
- **github**: Version control and collaboration
- **memory**: Context retention and knowledge management

## Required Tools

- Read
- Write
- Edit
- Bash
- Glob
- Grep

## Best Practices

1. **Resource Awareness**: Always consider flash, RAM, and power constraints
2. **Real-time Focus**: Ensure timing requirements are met consistently
3. **Error Handling**: Implement robust error recovery and watchdog mechanisms
4. **Modularity**: Design modular, testable code with clear interfaces
5. **Documentation**: Maintain thorough documentation of hardware interfaces and constraints
6. **Testing**: Validate on actual hardware with real-world conditions
7. **Power Optimization**: Minimize power consumption through sleep modes and efficient coding
8. **Safety**: Implement watchdogs, brownout detection, and fail-safe mechanisms

## Example Projects

### Sensor Node with BLE
```
Create a battery-powered sensor node using Nordic nRF52832 that:
- Reads temperature and humidity every 60 seconds
- Transmits data via BLE to mobile app
- Achieves < 50µA average current consumption
- Uses FreeRTOS for task management
```

### Motor Controller
```
Develop a motor controller using STM32F4 that:
- Controls brushless DC motor with FOC algorithm
- Responds to commands via CAN bus
- Maintains 10kHz control loop frequency
- Implements safety shutdown on fault conditions
```

### IoT Gateway
```
Build an IoT gateway using ESP32 that:
- Collects data from multiple I2C/SPI sensors
- Aggregates and transmits via WiFi/MQTT
- Supports OTA firmware updates
- Runs on battery with solar charging
```

## Troubleshooting

### High Power Consumption
- Review sleep mode implementation
- Check peripheral clock gating
- Verify wake source configuration
- Profile current usage by module

### Real-time Deadline Misses
- Analyze task priorities
- Review interrupt latencies
- Check for priority inversion
- Optimize critical sections

### Memory Issues
- Reduce code size with compiler flags
- Optimize data structures
- Review stack usage
- Implement memory pools

### Communication Failures
- Verify bus configuration (speed, pull-ups)
- Check timing requirements
- Review error handling
- Monitor bus with logic analyzer

## Contributing

This agent is part of the Claude Code Agent Marketplace. Contributions and feedback are welcome to improve embedded systems development capabilities.

## License

MIT
