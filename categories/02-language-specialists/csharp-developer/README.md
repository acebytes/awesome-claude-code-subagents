# C# Developer Agent

Expert C# developer specializing in modern .NET development, ASP.NET Core, and cloud-native applications. Masters C# 12 features, Blazor, and cross-platform development with emphasis on performance and clean architecture.

## Overview

This agent is a senior C# developer with deep expertise in .NET 8+ and the Microsoft ecosystem. It specializes in building high-performance web applications, cloud-native solutions, and cross-platform development with focus on clean code, architectural patterns, and modern C# language features.

## Prerequisites

- .NET 8+ SDK installed
- Git installed for version control
- Node.js 18+ (for MCP servers)
- GitHub Personal Access Token (for GitHub integration)
- Azure credentials (optional, for Azure-specific features)

## Installation

1. Clone or download this agent directory
2. Install MCP dependencies (automatically handled by the agent)
3. Set environment variables:
   ```bash
   export GITHUB_TOKEN="your-github-token"
   ```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access and manipulate files in the project directory
- **github**: GitHub API integration for repository operations
- **context7**: Access up-to-date library documentation
- **memory**: Persistent memory for context across sessions

## Slash Commands

### `/csharp-analyze`
Performs comprehensive analysis of C# code including:
- Modern C# pattern usage (records, pattern matching, nullable reference types)
- Performance characteristics and optimization opportunities
- Code quality and StyleCop compliance
- Architecture pattern evaluation
- LINQ query optimization
- Async/await best practices

**Example usage:**
```
/csharp-analyze the UserService class for performance issues
```

### `/csharp-test`
Generates comprehensive test suites including:
- xUnit test fixtures with theories
- Integration tests using TestServer
- Mocking with Moq
- Test data builders
- Property-based tests
- Performance tests with Benchmark.NET

**Example usage:**
```
/csharp-test create integration tests for the OrderController
```

### `/csharp-refactor`
Refactors code to use modern C# patterns:
- Convert classes to record types
- Apply pattern matching expressions
- Implement primary constructors
- Use file-scoped namespaces
- Apply nullable reference types
- Optimize LINQ queries
- Implement immutable APIs

**Example usage:**
```
/csharp-refactor the PaymentProcessor to use modern C# patterns
```

### `/csharp-async`
Reviews and optimizes asynchronous code:
- ConfigureAwait usage analysis
- Cancellation token implementation
- Async streams and IAsyncEnumerable
- Task composition patterns
- Deadlock prevention
- ValueTask optimization
- Exception handling in async methods

**Example usage:**
```
/csharp-async review the data access layer for async best practices
```

## Core Capabilities

### ASP.NET Core Development
- Minimal APIs for microservices
- Middleware pipeline optimization
- Dependency injection patterns
- Authentication and authorization
- Output caching strategies
- Health checks and monitoring

### Blazor Applications
- Component architecture design
- State management patterns
- JavaScript interop
- WebAssembly vs Server-side comparison
- Real-time features with SignalR

### Entity Framework Core
- Code-first migrations
- Query optimization and compiled queries
- Complex relationship mapping
- Bulk operations
- Multi-tenancy implementation

### Performance Optimization
- Span<T> and Memory<T> usage
- ArrayPool for memory management
- SIMD operations
- Source generators
- AOT compilation readiness
- Benchmark.NET profiling

### Cloud-Native Development
- Container optimization (Docker)
- Kubernetes health probes
- Distributed caching (Redis)
- Azure SDK integration
- Service bus messaging
- Feature flags and circuit breakers

## Example Usage

### Creating a New ASP.NET Core API

```
Create a new minimal API for product management with:
- CRUD endpoints
- EF Core with SQL Server
- JWT authentication
- OpenAPI documentation
- Health checks
- Output caching
```

### Optimizing Existing Code

```
/csharp-analyze the entire API project for performance bottlenecks
/csharp-async review all async methods in the repository layer
/csharp-refactor convert DTOs to record types
```

### Building Blazor Components

```
Create a Blazor component for displaying a product catalog with:
- Pagination
- Filtering
- State management
- Form validation
- Real-time updates via SignalR
```

### Database Optimization

```
Optimize the EF Core queries in OrderRepository:
- Use compiled queries
- Implement pagination
- Add proper indexes
- Use AsNoTracking where appropriate
```

## Development Workflow

1. **Solution Analysis**: The agent reviews your .NET solution structure, project dependencies, and configuration
2. **Implementation**: Develops features using modern C# patterns and .NET best practices
3. **Quality Verification**: Ensures code quality, test coverage, and performance standards
4. **Delivery**: Provides comprehensive implementation with tests and documentation

## Quality Standards

All code produced by this agent meets these standards:

- Nullable reference types enabled
- Code analysis with .editorconfig
- StyleCop compliance
- Test coverage exceeding 80%
- API versioning implemented
- Performance profiling completed
- Security scanning passed
- XML documentation generated

## Integration with Other Agents

This agent works well with:

- **frontend-developer**: For consuming APIs
- **api-designer**: For API contract design
- **azure-specialist**: For cloud deployment
- **database-optimizer**: For EF Core tuning
- **security-auditor**: For OWASP compliance
- **devops-engineer**: For CI/CD pipelines

## Performance Targets

The agent aims for these performance benchmarks:

- API response time: p95 < 100ms
- Memory allocation: Minimal GC pressure
- Startup time: < 2 seconds
- Build time: Optimized for incremental builds
- Test execution: < 30 seconds for unit tests

## Architecture Patterns

Supports multiple architectural styles:

- Clean Architecture
- Vertical Slice Architecture
- CQRS with MediatR
- Domain-Driven Design
- Microservices patterns
- Repository pattern
- Specification pattern

## Troubleshooting

### MCP Server Issues

If MCP servers fail to start:
```bash
# Clear npm cache
npm cache clean --force

# Verify Node.js version
node --version  # Should be 18+
```

### GitHub Integration

Ensure GITHUB_TOKEN is set:
```bash
export GITHUB_TOKEN="your-token"
```

### .NET SDK Issues

Verify .NET SDK:
```bash
dotnet --version  # Should be 8.0+
dotnet --list-sdks
```

## License

MIT

## Contributing

Contributions are welcome! Please follow the C# coding standards and ensure all tests pass.

## Support

For issues or questions, please refer to the main Claude Code Agent Marketplace repository.
