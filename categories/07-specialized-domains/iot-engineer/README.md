# IoT Engineer Agent

An expert IoT engineering agent specializing in connected device architectures, edge computing, and IoT platform development with focus on scalability, security, and reliability.

## Overview

The IoT Engineer agent is designed to help you build comprehensive IoT solutions spanning device connectivity, edge computing, cloud integration, and data analytics. With expertise in IoT protocols, device management, and massive-scale deployments, this agent can guide you from device firmware to cloud platforms.

## Features

- **IoT Architecture Design**: Complete system design from device layer to cloud
- **Protocol Expertise**: MQTT, CoAP, HTTP/HTTPS, WebSocket, LoRaWAN, NB-IoT, Zigbee
- **Edge Computing**: Local processing, data filtering, ML inference, offline operation
- **Cloud Platforms**: AWS IoT Core, Azure IoT Hub, Google Cloud IoT, ThingsBoard
- **Device Management**: Provisioning, OTA updates, remote monitoring, fleet management
- **Security**: End-to-end encryption, certificate management, zero trust architecture
- **Data Pipelines**: Ingestion, stream processing, analytics, visualization
- **Power Optimization**: Sleep modes, compression, energy harvesting

## Slash Commands

### /iot-protocol
Analyze and recommend IoT communication protocols based on your specific requirements.

**Use when:**
- Selecting protocols for a new IoT project
- Evaluating protocol trade-offs
- Optimizing existing communication patterns

**Provides:**
- Protocol comparison (MQTT, CoAP, HTTP, WebSocket, LoRaWAN)
- Performance analysis (latency, bandwidth, power consumption)
- Security considerations
- Implementation guidance
- Cost implications

**Example:**
```
/iot-protocol for 10,000 battery-powered sensors sending data every 5 minutes over cellular network
```

### /sensor-config
Generate sensor configuration and integration code ready for deployment.

**Use when:**
- Integrating new sensors into your IoT system
- Configuring data acquisition parameters
- Setting up calibration procedures

**Provides:**
- Sensor initialization code
- Data acquisition configuration
- Calibration procedures
- Power management settings
- Error handling patterns
- Data validation logic

**Example:**
```
/sensor-config for DHT22 temperature/humidity sensor with ESP32, reading every 60 seconds
```

### /mqtt-setup
Configure complete MQTT infrastructure for your IoT deployment.

**Use when:**
- Setting up MQTT messaging infrastructure
- Designing topic hierarchies
- Configuring broker security

**Provides:**
- Broker selection and setup (Mosquitto, AWS IoT, Azure IoT Hub)
- Topic hierarchy design
- QoS level recommendations
- TLS/SSL configuration
- Authentication and authorization
- Client connection patterns
- Monitoring and debugging tools

**Example:**
```
/mqtt-setup for 50,000 devices with separate telemetry and command topics, using AWS IoT Core
```

### /edge-deploy
Plan and execute edge computing deployments with containerization and orchestration.

**Use when:**
- Deploying edge computing applications
- Setting up edge gateways
- Implementing offline-capable systems

**Provides:**
- Edge device selection criteria
- Application containerization (Docker)
- Deployment strategies
- OTA update mechanisms
- Resource management
- Offline operation patterns
- Monitoring and diagnostics

**Example:**
```
/edge-deploy for video analytics on NVIDIA Jetson devices with Docker containers
```

## Performance Targets

The IoT Engineer agent helps you achieve production-grade performance:

- **Device Uptime**: >99.9%
- **Message Latency**: <500ms
- **Message Throughput**: 100K+ messages/second
- **Battery Life**: >1 year for battery-powered devices
- **Scalability**: Millions of devices
- **Security**: Industry-standard encryption and authentication
- **Data Integrity**: Guaranteed message delivery

## Setup

### Prerequisites

1. **Node.js**: Required for MCP servers
2. **Git**: For version control
3. **GitHub Token**: Set `GITHUB_TOKEN` environment variable for GitHub integration

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

### MCP Servers

This agent uses three MCP servers:

1. **Filesystem**: Access to local files for configuration and code
2. **GitHub**: Integration with GitHub repositories
3. **Memory**: Context retention across sessions

Configuration is automatically loaded from `mcp-config.json`.

### Optional Tools

For enhanced functionality, consider installing:

- **Docker**: For containerized edge deployments
- **MQTT Broker**: Mosquitto for local testing
- **IoT Development Boards**: Raspberry Pi, ESP32, Arduino
- **Cloud CLIs**: AWS CLI, Azure CLI, gcloud for platform integration

## Usage Examples

### Example 1: Design IoT Architecture

```
I need to design an IoT system for monitoring 1,000 industrial machines.
Each machine has 10 sensors reporting every minute. Data needs to be
analyzed in real-time for anomaly detection.
```

The agent will:
- Analyze requirements and constraints
- Recommend device architecture and protocols
- Design edge computing strategy
- Select cloud platform and services
- Plan data pipeline and analytics
- Implement security measures

### Example 2: Implement MQTT Communication

```
/mqtt-setup for factory monitoring system with 1,000 devices,
organized by building and floor, requiring secure communication
```

The agent provides:
- Topic hierarchy: `factory/{building}/{floor}/{device_id}/{sensor_type}`
- QoS recommendations (QoS 1 for telemetry, QoS 2 for commands)
- TLS configuration with client certificates
- Broker sizing and configuration
- Client connection code examples

### Example 3: Edge Computing Deployment

```
/edge-deploy for running machine learning inference on edge gateways
processing video streams from 50 cameras per location
```

The agent delivers:
- Hardware recommendations (NVIDIA Jetson, Intel NUC)
- Containerized ML inference application
- Deployment scripts and Docker Compose configuration
- Update mechanism using Docker registry
- Resource monitoring and auto-scaling
- Offline buffering strategy

### Example 4: Sensor Integration

```
/sensor-config for integrating BMP280 pressure sensor with Raspberry Pi,
reading every 30 seconds with I2C interface
```

The agent generates:
- Python code for BMP280 initialization
- I2C configuration and error handling
- Calibration procedure
- Data validation and filtering
- Power management (sleep between readings)
- MQTT publishing code

## IoT Engineering Workflow

### 1. System Analysis
- Device assessment and selection
- Connectivity analysis (cellular, WiFi, LoRa)
- Data flow mapping
- Security requirements definition
- Scalability planning
- Cost estimation

### 2. Implementation
- Device firmware development
- Edge application deployment
- Cloud service configuration
- Data pipeline setup
- Security implementation
- Management tools integration
- Testing and validation

### 3. Deployment & Monitoring
- Device provisioning at scale
- Network connectivity validation
- Performance monitoring
- Security auditing
- Cost optimization
- Predictive maintenance
- Continuous improvement

## Integration with Other Agents

The IoT Engineer agent collaborates effectively with:

- **embedded-systems**: Firmware development and hardware integration
- **cloud-architect**: Infrastructure design and cloud platform selection
- **data-engineer**: Data pipeline development and analytics
- **security-auditor**: IoT security assessment and compliance
- **devops-engineer**: Deployment automation and orchestration
- **mobile-developer**: Mobile app integration for device control
- **ml-engineer**: Edge ML deployment and model optimization
- **business-analyst**: Business insights from IoT data

## Best Practices

### Security
- Zero trust architecture
- End-to-end encryption for all data
- Regular certificate rotation
- Network isolation and segmentation
- Comprehensive audit logging

### Scalability
- Horizontal scaling of cloud services
- Message queuing for reliability
- Database sharding for performance
- Multi-region deployment for availability
- Auto-scaling based on load

### Power Optimization
- Intelligent sleep modes
- Communication scheduling
- Data compression
- Protocol optimization (MQTT-SN, CoAP)
- Energy harvesting where applicable

### Reliability
- Guaranteed message delivery (QoS)
- Offline operation and buffering
- Automatic reconnection logic
- State management and recovery
- Health monitoring and diagnostics

## Common Use Cases

1. **Industrial IoT**: Factory automation, predictive maintenance, asset tracking
2. **Smart Cities**: Street lighting, waste management, environmental monitoring
3. **Agriculture**: Soil monitoring, irrigation control, livestock tracking
4. **Smart Buildings**: HVAC optimization, occupancy monitoring, energy management
5. **Healthcare**: Remote patient monitoring, medical device connectivity
6. **Logistics**: Fleet management, cold chain monitoring, warehouse automation
7. **Energy**: Smart meters, grid monitoring, renewable energy optimization
8. **Retail**: Inventory tracking, customer analytics, smart shelves

## Troubleshooting

### Common Issues

**Problem**: High message latency
- Check network connectivity and bandwidth
- Optimize message size and compression
- Review QoS settings
- Consider edge processing to reduce cloud traffic

**Problem**: Device connection failures
- Verify certificate validity
- Check network firewall rules
- Review authentication credentials
- Monitor broker capacity and performance

**Problem**: Battery draining quickly
- Review sleep mode implementation
- Optimize communication frequency
- Consider protocol efficiency (MQTT-SN, CoAP)
- Check for unnecessary wake events

**Problem**: Data loss
- Implement QoS 1 or 2 for critical messages
- Add local buffering on devices
- Review message retention policies
- Monitor broker and network reliability

## Resources

### Documentation
- [AWS IoT Core Documentation](https://docs.aws.amazon.com/iot/)
- [Azure IoT Hub Documentation](https://docs.microsoft.com/en-us/azure/iot-hub/)
- [MQTT Specification](https://mqtt.org/mqtt-specification/)
- [LoRaWAN Specification](https://lora-alliance.org/resource_hub/lorawan-specification-v1-1/)

### Tools
- [Mosquitto MQTT Broker](https://mosquitto.org/)
- [Eclipse Paho MQTT Clients](https://www.eclipse.org/paho/)
- [Node-RED for IoT Flows](https://nodered.org/)
- [ThingsBoard IoT Platform](https://thingsboard.io/)

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

This agent configuration is part of the Claude Code Agent Marketplace and follows the repository's license terms.
