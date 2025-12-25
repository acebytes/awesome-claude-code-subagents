# .NET Core Expert Agent

Expert .NET Core specialist mastering .NET 10 with modern C# features. Specializes in cross-platform development, minimal APIs, cloud-native applications, and microservices with focus on building high-performance, scalable solutions.

## Overview

This agent provides comprehensive .NET development expertise, covering everything from minimal API design to microservices architecture, with deep knowledge of .NET 10, C# 14, Entity Framework Core, and cloud-native patterns.

## Features

- **Minimal APIs**: Build lightweight, high-performance APIs with endpoint routing and OpenAPI documentation
- **Clean Architecture**: Implement domain-driven design with clear separation of concerns
- **Microservices**: Design scalable service architectures with resilience patterns and distributed tracing
- **Entity Framework Core**: Optimize database access with advanced query patterns and migrations
- **Cloud-Native**: Deploy containerized applications to Kubernetes with auto-scaling and observability
- **Performance**: Leverage Native AOT compilation, memory pooling, and async patterns for optimal performance
- **Testing**: Comprehensive test coverage with xUnit, integration tests, and test containers
- **Modern C#**: Utilize C# 14 features including record types, pattern matching, and source generators

## Installation

1. Clone this agent configuration:
```bash
cd /path/to/your/agents
cp -r /Users/d/Documents/GitHub/claude-code-agent-marketplace/categories/02-language-specialists/dotnet-core-expert .
```

2. Set up environment variables (optional):
```bash
export GITHUB_TOKEN=your_github_personal_access_token
```

3. Load the agent in Claude Code with the MCP configuration.

## Slash Commands

### /dotnet-service
Create a new .NET microservice with clean architecture, dependency injection, and minimal APIs.

**Example usage:**
```
/dotnet-service
Create a product catalog microservice with CQRS pattern and EF Core
```

### /dotnet-api
Generate minimal API endpoints with OpenAPI documentation, validation, and authentication.

**Example usage:**
```
/dotnet-api
Add REST endpoints for product management with JWT authentication
```

### /dotnet-test
Set up comprehensive test suite with xUnit, integration tests, and test containers.

**Example usage:**
```
/dotnet-test
Create integration tests for the product API using WebApplicationFactory
```

### /dotnet-deploy
Configure Docker, Kubernetes manifests, and CI/CD pipeline for cloud deployment.

**Example usage:**
```
/dotnet-deploy
Setup Kubernetes deployment with health checks and horizontal pod autoscaling
```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access and manage project files
- **github**: Interact with GitHub repositories
- **context7**: Access up-to-date .NET documentation and best practices
- **memory**: Maintain context across sessions for project continuity

## Capabilities

### Architecture & Design
- Clean architecture layers (Domain, Application, Infrastructure, Presentation)
- CQRS pattern with MediatR
- Repository and Unit of Work patterns
- Dependency injection and IoC containers
- Microservices design patterns

### Development
- Minimal API development
- ASP.NET Core middleware pipeline
- Entity Framework Core optimization
- gRPC and SignalR services
- Background and hosted services

### Performance
- Native AOT compilation
- Memory pooling and Span<T> usage
- Async/await best practices
- Response caching and compression
- Database query optimization

### Testing
- xUnit test framework
- Integration testing with WebApplicationFactory
- Test containers for database testing
- BenchmarkDotNet for performance testing
- Load and E2E testing

### Cloud & DevOps
- Docker container optimization
- Kubernetes deployment and scaling
- Health checks and graceful shutdown
- Structured logging and distributed tracing
- CI/CD pipeline configuration

## Example Workflows

### Creating a Microservice

```
I need to create a new order management microservice with:
- Clean architecture structure
- Minimal APIs for CRUD operations
- Entity Framework Core with PostgreSQL
- JWT authentication
- Integration tests
- Docker containerization
```

The agent will:
1. Set up solution structure with clean architecture layers
2. Configure dependency injection and services
3. Implement minimal API endpoints with validation
4. Set up EF Core with migrations
5. Add JWT authentication middleware
6. Create comprehensive tests
7. Generate Dockerfile and deployment manifests

### Optimizing Performance

```
Analyze and optimize the performance of our .NET API:
- Reduce startup time
- Improve response times
- Lower memory allocation
- Enable Native AOT compilation
```

The agent will:
1. Profile the application for bottlenecks
2. Implement memory pooling and Span<T> where applicable
3. Optimize database queries with compiled queries
4. Add response caching layers
5. Configure Native AOT compilation
6. Set up BenchmarkDotNet tests
7. Provide performance metrics and recommendations

### Building Cloud-Native Applications

```
Convert our monolithic .NET app to cloud-native microservices:
- Split into bounded contexts
- Add service discovery
- Implement resilience patterns
- Set up observability
```

The agent will:
1. Analyze the monolith and identify service boundaries
2. Design microservices architecture
3. Implement health checks and readiness probes
4. Add circuit breakers and retry policies
5. Configure structured logging and OpenTelemetry
6. Create Kubernetes manifests
7. Set up service mesh integration

## Best Practices

The agent enforces .NET best practices:

- **Code Quality**: SOLID principles, DRY, and C# coding standards
- **Performance**: Async/await patterns, minimal allocations, efficient algorithms
- **Security**: Authentication, authorization, data encryption, secure headers
- **Testing**: >80% code coverage, integration tests, performance benchmarks
- **Documentation**: XML documentation, OpenAPI specs, README files
- **Cloud-Ready**: Container optimization, 12-factor app principles, observability

## Integration with Other Agents

This agent works well with:

- **csharp-developer**: C# language optimization and advanced features
- **microservices-architect**: Service design and architecture patterns
- **cloud-architect**: Cloud deployment and infrastructure
- **api-designer**: API design and REST patterns
- **devops-engineer**: CI/CD and deployment automation
- **database-administrator**: Database design and EF Core optimization
- **security-auditor**: Security scanning and compliance
- **performance-engineer**: Performance testing and optimization

## Requirements

- **.NET**: 10.0 or higher
- **C#**: 14.0 or higher
- **Node.js**: 18.0 or higher (for MCP servers)

## Environment Variables

- `GITHUB_TOKEN`: GitHub personal access token for repository operations (optional)

## Troubleshooting

### MCP Servers Not Loading
Ensure Node.js 18+ is installed and npx is available in your PATH.

### Context7 Not Working
Context7 requires internet connectivity to fetch up-to-date documentation.

### GitHub Integration Issues
Verify your GITHUB_TOKEN is valid and has appropriate permissions.

## Contributing

To improve this agent:
1. Fork the repository
2. Make your changes to the CLAUDE.md instructions or configuration
3. Test with various .NET scenarios
4. Submit a pull request with detailed description

## License

MIT License - See repository root for details

## Support

For issues or questions:
- Check the Claude Code Agent Marketplace documentation
- Review .NET official documentation at https://docs.microsoft.com/dotnet
- Consult the agent manifest for capability details

---

**Note**: This agent is optimized for .NET 10 and C# 14. For older .NET Framework projects, consider using a .NET Framework specialist agent.
