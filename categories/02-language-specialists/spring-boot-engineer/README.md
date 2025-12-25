# Spring Boot Engineer Agent

Expert Spring Boot engineer mastering Spring Boot 3+ with cloud-native patterns. Specializes in microservices, reactive programming, Spring Cloud integration, and enterprise solutions with focus on building scalable, production-ready applications.

## Overview

This agent is a senior Spring Boot engineer with deep expertise in:
- Spring Boot 3.x and Java 17+ development
- Microservices architecture and design patterns
- Reactive programming with WebFlux
- Spring Cloud ecosystem integration
- Enterprise application development
- Cloud-native deployment strategies
- GraalVM native compilation
- Performance optimization

## Features

### Core Capabilities
- **Spring Boot 3.x Development**: Leverage latest features including auto-configuration, actuators, and native compilation
- **Microservices Architecture**: Design and implement service discovery, API gateways, circuit breakers, and distributed tracing
- **Reactive Programming**: Build non-blocking applications with WebFlux, R2DBC, and reactive streams
- **Spring Cloud Integration**: Implement config servers, service discovery, and cloud-native patterns
- **Data Access**: Work with Spring Data JPA, R2DBC, query optimization, and multi-datasource configurations
- **Security**: Implement Spring Security, OAuth2/JWT, method security, and API protection
- **Enterprise Integration**: Connect with message queues, Kafka, REST/SOAP services, and batch processing
- **Testing**: Write comprehensive unit, integration, and contract tests with Testcontainers
- **Performance**: Optimize JVM, connection pooling, caching, and achieve fast startup times
- **Cloud Deployment**: Deploy to Docker, Kubernetes with health checks, graceful shutdown, and auto-scaling

### Quality Standards
- Test coverage > 85%
- Fast startup times (< 3 seconds)
- GraalVM native compilation support
- Complete API documentation
- Security hardening
- Cloud-native readiness
- Performance optimization
- Comprehensive monitoring

## Prerequisites

### Required Environment Variables
- `GITHUB_TOKEN`: GitHub Personal Access Token for repository operations

### Required Tools
- Node.js and npm (for MCP servers)
- Java 17 or later
- Maven or Gradle
- Docker (for Testcontainers and deployment)

## Installation

1. **Copy the agent directory** to your Claude Code agents location:
   ```bash
   cp -r spring-boot-engineer ~/.config/claude-code/agents/
   ```

2. **Set up environment variables**:
   ```bash
   export GITHUB_TOKEN="your_github_personal_access_token"
   ```

3. **Install MCP servers** (happens automatically on first use):
   - filesystem: File system operations
   - github: GitHub API integration
   - context7: Documentation and context management
   - memory: Conversation and knowledge persistence

## Usage

### Starting the Agent

Invoke the agent in Claude Code:
```
@spring-boot-engineer help me build a microservices application
```

### Slash Commands

#### `/spring-service`
Generate a new Spring Boot service with complete architecture:
```
/spring-service create a user management service
```

Creates:
- REST controller with CRUD endpoints
- Service layer with business logic
- Repository interface with Spring Data
- Entity/domain model
- DTOs for request/response
- Exception handling
- Dependency injection setup
- Transaction management

#### `/spring-controller`
Create a REST controller following best practices:
```
/spring-controller create a product controller with CRUD operations
```

Generates:
- Controller with proper annotations
- Request/response DTOs
- Validation annotations
- API documentation (OpenAPI/Swagger)
- Proper HTTP status codes
- Error handling
- HATEOAS support (optional)

#### `/spring-test`
Generate comprehensive test suite:
```
/spring-test create tests for the order service
```

Creates:
- Unit tests with JUnit 5 and Mockito
- Integration tests with @SpringBootTest
- MockMvc tests for controllers
- WebTestClient for reactive endpoints
- Testcontainers for database testing
- Security testing
- Test configuration

#### `/spring-config`
Create Spring Boot configuration:
```
/spring-config setup configuration for multiple environments
```

Generates:
- Application properties (YAML/Properties)
- Profile-specific configurations
- Configuration classes with @Bean definitions
- Externalized configuration
- Custom property sources
- Configuration validation

### Example Workflows

#### Building a Microservice
```
@spring-boot-engineer I need to create an order processing microservice with:
- REST API for order management
- Kafka integration for event publishing
- PostgreSQL for data persistence
- Redis for caching
- OAuth2 security
- Docker deployment
```

#### Implementing Reactive APIs
```
@spring-boot-engineer Create a reactive WebFlux application with:
- Non-blocking REST endpoints
- R2DBC for reactive database access
- Server-sent events for real-time updates
- Backpressure handling
- Reactive security
```

#### Setting Up Spring Cloud
```
@spring-boot-engineer Set up Spring Cloud infrastructure with:
- Config server for centralized configuration
- Eureka for service discovery
- Gateway for API routing
- Circuit breaker with Resilience4j
- Distributed tracing with Zipkin
```

## MCP Servers

### Filesystem
Provides file system operations for reading and writing Spring Boot project files.

### GitHub
Enables GitHub operations for version control and collaboration:
- Repository management
- Pull request operations
- Issue tracking
- Code reviews

### Context7
Provides access to Spring Boot documentation and best practices:
- Spring Framework documentation
- Spring Boot guides
- API references
- Community patterns

### Memory
Maintains conversation history and learned preferences:
- Project context
- Architecture decisions
- Code patterns
- Development history

## Development Workflow

### 1. Architecture Planning
The agent starts by:
- Understanding application requirements
- Designing service architecture
- Planning API structure
- Defining data model
- Mapping integrations
- Setting security strategy
- Configuring testing approach
- Planning deployment pipeline

### 2. Implementation Phase
The agent implements:
- Service layers with dependency injection
- REST APIs with proper endpoints
- Data access with Spring Data
- Security with Spring Security
- Cloud configuration
- Comprehensive tests
- Performance optimizations
- Deployment configurations

### 3. Quality Assurance
The agent ensures:
- Test coverage > 85%
- API documentation complete
- Security hardened
- Performance optimized
- Cloud-ready deployment
- Monitoring configured
- Documentation updated

## Best Practices

The agent follows these principles:
- **12-Factor App**: Cloud-native application patterns
- **Clean Architecture**: Separation of concerns and layers
- **SOLID Principles**: Object-oriented design principles
- **DRY Code**: Don't repeat yourself
- **Test Pyramid**: Unit, integration, and E2E tests
- **API First**: Design APIs before implementation
- **Documentation**: Keep docs current and comprehensive
- **Code Reviews**: Thorough review process

## Integration with Other Agents

The Spring Boot Engineer agent collaborates with:
- **java-architect**: Java design patterns and architecture
- **microservices-architect**: Microservices design and patterns
- **database-optimizer**: Database performance and optimization
- **devops-engineer**: Deployment and infrastructure
- **security-auditor**: Security scanning and hardening
- **performance-engineer**: Performance tuning and optimization
- **api-designer**: API design and documentation
- **cloud-architect**: Cloud deployment strategies

## Troubleshooting

### MCP Server Issues
If MCP servers fail to start:
```bash
# Test MCP servers manually
npx -y @modelcontextprotocol/server-filesystem ${PWD}
npx -y @modelcontextprotocol/server-github
npx -y @upstash/context7-mcp
npx -y @modelcontextprotocol/server-memory
```

### GitHub Token Issues
Ensure your GitHub token has required permissions:
- `repo`: Repository access
- `read:org`: Organization access
- `workflow`: GitHub Actions access

### Memory Issues
Clear agent memory if needed:
```bash
# Reset conversation memory
rm -rf ~/.config/claude-code/agents/spring-boot-engineer/memory/*
```

## Examples

### Example 1: REST API Service
```
@spring-boot-engineer /spring-service

Create a Product Service with:
- CRUD operations for products
- Category management
- Search and filtering
- Pagination support
- Caching with Redis
- PostgreSQL database
- 90% test coverage
```

### Example 2: Reactive Microservice
```
@spring-boot-engineer Build a reactive notification service:
- WebFlux for non-blocking APIs
- R2DBC with PostgreSQL
- Kafka consumer for events
- Server-sent events for real-time notifications
- Reactive security
- Testcontainers for integration tests
```

### Example 3: Cloud-Native Application
```
@spring-boot-engineer Create a cloud-native order service:
- Spring Cloud Config for configuration
- Eureka service discovery
- Circuit breaker with Resilience4j
- Distributed tracing
- Kubernetes deployment
- Health checks and metrics
- GraalVM native image
```

## Resources

- [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Spring Framework Reference](https://docs.spring.io/spring-framework/reference/)
- [Spring Cloud Documentation](https://spring.io/projects/spring-cloud)
- [Spring Security Reference](https://docs.spring.io/spring-security/reference/)
- [Reactive Programming Guide](https://projectreactor.io/docs)

## Contributing

To enhance this agent:
1. Update `CLAUDE.md` with new instructions or patterns
2. Add new slash commands to `agent-manifest.json`
3. Update `README.md` with examples and documentation
4. Test changes thoroughly with real Spring Boot projects

## License

This agent is part of the Claude Code Agent Marketplace and follows the repository's license terms.

## Support

For issues or questions:
1. Check the troubleshooting section
2. Review Spring Boot documentation
3. Consult the Claude Code documentation
4. Open an issue in the agent marketplace repository
