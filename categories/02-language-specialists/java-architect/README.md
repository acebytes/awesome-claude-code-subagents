# Java Architect Agent

A senior Java architect agent specializing in enterprise-grade applications, Spring ecosystem, and cloud-native development with expertise in modern Java features, reactive programming, and microservices patterns.

## Overview

The Java Architect agent is designed to help you build scalable, maintainable, and production-ready Java applications using modern Java (17+), Spring Boot 3.x, and enterprise architecture patterns. It emphasizes clean architecture, SOLID principles, and best practices for cloud-native development.

## Features

### Core Capabilities

- **Enterprise Architecture**: Domain-Driven Design, Clean Architecture, Hexagonal Architecture
- **Spring Ecosystem**: Spring Boot 3.x, Spring Cloud, Spring Security, Spring Data, Spring WebFlux
- **Microservices**: Service design, API Gateway patterns, circuit breakers, distributed tracing
- **Reactive Programming**: Project Reactor, WebFlux, R2DBC, backpressure handling
- **Performance**: JVM tuning, GC optimization, JMH benchmarking, GraalVM native images
- **Testing**: JUnit 5, TestContainers, Mockito, REST Assured, contract testing
- **Cloud-Native**: Twelve-factor apps, Kubernetes readiness, observability, health checks

### Modern Java Features

- Records and sealed classes
- Pattern matching
- Virtual threads (Project Loom)
- Text blocks
- Switch expressions
- Stream API mastery

## Installation

1. Ensure you have Java 17+ installed (Java 21 recommended)
2. Configure the agent with your preferred build tool (Maven or Gradle)
3. Set up the required MCP servers (see Configuration section)

## Configuration

### MCP Servers

The agent uses the following MCP servers:

- **filesystem**: File system access for reading and writing code
- **github**: GitHub integration for repository management
- **context7**: Documentation and code context retrieval
- **memory**: Persistent memory for project context

### Environment Variables

Set the following environment variable for GitHub integration:

```bash
export GITHUB_TOKEN=your_github_personal_access_token
```

## Usage

### Slash Commands

#### `/java-analyze`

Performs comprehensive analysis of your Java codebase:

```
/java-analyze
```

This command will:
- Evaluate module structure and dependencies
- Review Spring configurations
- Assess design patterns usage
- Analyze data flow and transaction handling
- Check security implementation
- Measure performance baselines
- Identify technical debt

#### `/java-test`

Generates comprehensive test suites:

```
/java-test
```

Creates:
- Unit tests with JUnit 5 and Mockito
- Integration tests with TestContainers
- Performance tests with JMH
- API tests with REST Assured
- Contract tests with Pact

#### `/java-refactor`

Refactors code to improve quality and maintainability:

```
/java-refactor
```

Applies:
- SOLID principles
- Clean Architecture patterns
- Enterprise design patterns
- Code optimization
- Error handling improvements

#### `/java-patterns`

Recommends and implements enterprise patterns:

```
/java-patterns
```

Implements:
- Domain-Driven Design patterns
- CQRS and Event Sourcing
- Saga pattern for distributed transactions
- Repository and Unit of Work
- Strategy and Factory patterns

### Example Workflows

#### Creating a Spring Boot Microservice

```
Create a new Spring Boot 3.2 microservice for user management with:
- RESTful API endpoints
- PostgreSQL with R2DBC
- OAuth2 authentication
- Comprehensive test coverage
- OpenAPI documentation
```

#### Implementing DDD Patterns

```
/java-patterns

Implement Domain-Driven Design for an e-commerce order system including:
- Order aggregate with business rules
- Value objects for Money and Address
- Domain events for order lifecycle
- Repository pattern for persistence
```

#### Performance Optimization

```
/java-analyze

Analyze performance bottlenecks in the payment service and:
- Optimize JPA queries
- Implement caching strategy
- Tune connection pools
- Create JMH benchmarks
```

## Quality Standards

The agent ensures:

- **Test Coverage**: Minimum 85% code coverage
- **Static Analysis**: SpotBugs and SonarQube clean
- **Documentation**: OpenAPI specs and JavaDoc
- **Performance**: JMH benchmarks for critical paths
- **Security**: OWASP compliance and security scanning
- **Architecture**: Clean Architecture and SOLID principles

## Development Checklist

Every implementation includes:

- [ ] Clean Architecture and SOLID principles applied
- [ ] Spring Boot best practices followed
- [ ] Test coverage exceeds 85%
- [ ] SpotBugs and SonarQube analysis clean
- [ ] API documentation with OpenAPI
- [ ] JMH benchmarks for performance-critical code
- [ ] Proper exception handling hierarchy
- [ ] Database migrations versioned (Flyway/Liquibase)

## Enterprise Patterns

### Supported Patterns

- **Domain-Driven Design**: Aggregates, Entities, Value Objects, Domain Events
- **Hexagonal Architecture**: Ports and Adapters, Dependency Inversion
- **CQRS**: Command Query Responsibility Segregation
- **Event Sourcing**: Event-driven state management
- **Saga Pattern**: Distributed transaction management
- **Repository Pattern**: Data access abstraction
- **Specification Pattern**: Business rule encapsulation
- **Strategy Pattern**: Algorithmic variations
- **Factory Pattern**: Object creation

## Spring Ecosystem

### Key Technologies

- **Spring Boot 3.x**: Auto-configuration, starters, actuator
- **Spring Cloud**: Config, Gateway, Service Discovery, Circuit Breaker
- **Spring Security**: OAuth2, JWT, method-level security
- **Spring Data**: JPA, R2DBC, MongoDB, Redis
- **Spring WebFlux**: Reactive web applications
- **Spring Cloud Stream**: Event-driven microservices
- **Spring Batch**: ETL and batch processing

## Testing Strategy

### Test Pyramid

1. **Unit Tests** (70%): JUnit 5, Mockito, AssertJ
2. **Integration Tests** (20%): TestContainers, Spring Boot Test
3. **End-to-End Tests** (10%): REST Assured, Cucumber

### Testing Tools

- **JUnit 5**: Modern testing framework
- **Mockito**: Mocking and stubbing
- **TestContainers**: Integration testing with Docker
- **REST Assured**: API testing
- **JMH**: Performance benchmarking
- **ArchUnit**: Architecture testing
- **Pact**: Contract testing

## Performance Optimization

### JVM Tuning

- GC algorithm selection (G1GC, ZGC, Shenandoah)
- Heap sizing and memory management
- Thread pool configuration
- JIT compilation optimization

### Application Performance

- Query optimization with JPA/Hibernate
- Caching strategies (Redis, Caffeine)
- Connection pool tuning (HikariCP)
- Reactive programming for scalability

### Monitoring

- Micrometer metrics
- Distributed tracing (Zipkin, Jaeger)
- Structured logging (Logback, SLF4J)
- Custom health indicators

## Cloud-Native Development

### Twelve-Factor App Compliance

- Codebase tracking
- Dependency management
- Configuration externalization
- Backing services
- Build, release, run separation
- Stateless processes
- Port binding
- Concurrency
- Disposability
- Dev/prod parity
- Logs as event streams
- Admin processes

### Kubernetes Readiness

- Health checks (liveness, readiness)
- Graceful shutdown
- Resource limits
- ConfigMaps and Secrets
- Service discovery
- Horizontal scaling

## Agent Collaboration

The Java Architect agent works well with:

- **frontend-developer**: Providing backend APIs
- **api-designer**: Implementing API contracts
- **devops-engineer**: Deployment configurations
- **database-optimizer**: Query optimization
- **kotlin-specialist**: JVM patterns
- **microservices-architect**: Architecture patterns
- **security-auditor**: Vulnerability fixes
- **cloud-architect**: Cloud-native features

## Best Practices

### Code Organization

- Clean separation of concerns
- Package by feature, not layer
- Domain-centric structure
- Clear module boundaries

### Error Handling

- Proper exception hierarchy
- Global exception handling
- Meaningful error messages
- Logging best practices

### Security

- OAuth2/JWT authentication
- Method-level authorization
- CORS configuration
- Rate limiting
- Encryption at rest and in transit

### Documentation

- Comprehensive JavaDoc
- OpenAPI specifications
- Architecture Decision Records (ADRs)
- README and setup guides

## Troubleshooting

### Common Issues

**Issue**: Slow application startup
- **Solution**: Optimize component scanning, use lazy initialization, consider GraalVM native image

**Issue**: High memory consumption
- **Solution**: Analyze heap dumps, optimize object creation, tune GC settings

**Issue**: Database connection pool exhaustion
- **Solution**: Review HikariCP configuration, optimize query execution, implement connection timeouts

**Issue**: Reactive backpressure errors
- **Solution**: Implement proper backpressure strategies, buffer sizing, timeout handling

## Resources

### Official Documentation

- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Spring Framework Documentation](https://spring.io/projects/spring-framework)
- [Project Reactor Documentation](https://projectreactor.io/docs)
- [Java SE Documentation](https://docs.oracle.com/en/java/javase/)

### Recommended Reading

- "Spring in Action" by Craig Walls
- "Domain-Driven Design" by Eric Evans
- "Clean Architecture" by Robert C. Martin
- "Reactive Spring" by Josh Long
- "Effective Java" by Joshua Bloch

## Contributing

Contributions are welcome! Please follow the contribution guidelines in the main repository.

## License

MIT License - See LICENSE file for details
