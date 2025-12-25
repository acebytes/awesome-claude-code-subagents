# .NET Framework 4.8 Expert Agent

Expert .NET Framework 4.8 specialist mastering legacy enterprise applications. Specializes in Windows-based development, Web Forms, WCF services, and Windows services with focus on maintaining and modernizing existing enterprise solutions.

## Overview

This agent is a senior .NET Framework 4.8 expert with deep expertise in:
- .NET Framework 4.8 features and C# 7.3 capabilities
- ASP.NET Web Forms development and optimization
- Windows Communication Foundation (WCF) services
- Windows services architecture and deployment
- Entity Framework 6 data access patterns
- Enterprise integration and legacy modernization
- Security hardening and vulnerability remediation
- Performance optimization within framework constraints
- COM interop and Win32 API integration
- Comprehensive testing with NUnit, MSTest, and Moq

## Installation

### Prerequisites

- .NET Framework 4.8 SDK
- Node.js >= 18.0.0
- GitHub Personal Access Token (for GitHub integration)

### Environment Setup

Set the following environment variable:

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

### MCP Servers

This agent uses the following MCP servers:

1. **filesystem** - File system operations for .NET projects
2. **github** - GitHub repository integration
3. **context7** - Documentation and context retrieval for .NET Framework
4. **memory** - Persistent memory and context management

## Slash Commands

### /dotnet48-analyze

Perform comprehensive analysis of .NET Framework 4.8 codebase to identify security vulnerabilities, performance bottlenecks, and modernization opportunities.

**Example Usage:**
```
/dotnet48-analyze WebFormsApp for security issues and performance problems
```

This command will:
- Analyze code architecture and design patterns
- Identify security vulnerabilities (SQL injection, XSS, authentication issues)
- Find performance bottlenecks (memory leaks, N+1 queries, threading issues)
- Assess dependency health and version compatibility
- Recommend modernization strategies
- Generate detailed analysis report with actionable recommendations

**What to expect:**
- Security vulnerability report with severity ratings
- Performance analysis with profiling recommendations
- Code quality assessment
- Modernization roadmap
- Risk assessment for changes

### /dotnet48-refactor

Refactor legacy .NET Framework code to improve maintainability while preserving backward compatibility and enterprise integration.

**Example Usage:**
```
/dotnet48-refactor OrderProcessing module to implement repository pattern
```

This command will:
- Apply enterprise design patterns (Repository, Unit of Work, Factory)
- Improve code organization and separation of concerns
- Maintain backward compatibility with existing systems
- Enhance testability through dependency injection
- Update documentation and code comments
- Preserve existing functionality and business logic

**Common refactoring scenarios:**
- Convert data access code to Repository pattern
- Implement dependency injection with Unity or Autofac
- Separate concerns in Web Forms code-behind
- Extract business logic from WCF services
- Apply SOLID principles to legacy code

### /dotnet48-test

Create comprehensive test suite for .NET Framework applications using NUnit, MSTest, or xUnit with proper mocking and integration tests.

**Example Usage:**
```
/dotnet48-test CustomerService WCF service with unit and integration tests
```

This command will:
- Generate unit tests using NUnit or MSTest
- Create integration tests for WCF services and database operations
- Implement mocking with Moq for dependencies
- Add performance tests for critical code paths
- Include security tests for authentication and authorization
- Achieve target code coverage (75%+)
- Document test scenarios and edge cases

**Test coverage includes:**
- Business logic unit tests
- Data access integration tests
- WCF service contract tests
- Web Forms page lifecycle tests
- Security and authentication tests
- Performance and load tests

### /dotnet48-migrate

Plan and execute migration strategy for .NET Framework applications, including modernization paths and .NET Core/.NET migration assessment.

**Example Usage:**
```
/dotnet48-migrate assess WebAPI project for .NET 8 migration feasibility
```

This command will:
- Analyze migration compatibility with .NET Portability Analyzer
- Identify breaking changes and incompatible dependencies
- Recommend migration strategy (rewrite, refactor, or lift-and-shift)
- Create phased migration roadmap
- Document risks, dependencies, and prerequisites
- Provide effort estimates and resource requirements
- Generate compatibility reports

**Migration assessments:**
- .NET Framework to .NET 8 feasibility
- Web Forms to ASP.NET Core MVC/Razor Pages
- WCF to gRPC or REST APIs
- Windows services to modern hosting models
- Entity Framework 6 to EF Core

## Capabilities

### Web Forms Development
- Page lifecycle management and optimization
- ViewState optimization and reduction
- Custom server control development
- Master pages and user controls
- AJAX integration with UpdatePanel
- Security controls and membership providers
- State management strategies
- Caching implementation

### WCF Services
- Service and data contract design
- Binding configuration (BasicHttp, NetTcp, WsHttp)
- Security patterns (transport and message security)
- Fault handling and error management
- Service hosting (IIS, Windows service, self-hosted)
- Client proxy generation and management
- Performance tuning and optimization
- Duplex communication patterns

### Windows Services
- Service architecture and design
- Installation and uninstallation automation
- Configuration management with app.config
- Logging strategies (Event Log, file-based, centralized)
- Error handling and recovery
- Performance monitoring and metrics
- Security context and permissions
- Deployment automation with InstallUtil or SC.exe

### Entity Framework 6
- Code-first, database-first, and model-first approaches
- Migration strategies and version control
- Performance optimization (eager loading, compiled queries)
- Lazy loading configuration
- Change tracking optimization
- Complex types and value objects
- Stored procedure mapping
- Connection resiliency and retry logic

### Enterprise Patterns
- Layered architecture (presentation, business, data)
- Repository pattern for data access
- Unit of Work for transaction management
- Dependency injection with Unity or Autofac
- Factory patterns for object creation
- Observer pattern for event handling
- Command pattern for operations
- Strategy pattern for algorithms

### Legacy Integration
- COM interop for legacy components
- Win32 API P/Invoke calls
- Windows Registry access
- Windows services integration
- System services communication
- Network protocol handling
- File system operations
- Process management and IPC

## Quality Standards

The .NET Framework 4.8 Expert maintains high quality standards:

- **Security Score**: Target > 95 (vulnerability-free)
- **Test Coverage**: Target > 75%
- **Performance Improvement**: Target > 25%
- **Code Quality**: .NET conventions, SOLID principles
- **Backward Compatibility**: 100% preserved
- **Documentation**: Complete and current
- **Deployment**: Automated and reliable

## Example Use Cases

### 1. Modernize Legacy Web Forms Application
```
Analyze and modernize CustomerPortal Web Forms app - improve performance, fix security vulnerabilities, and add comprehensive tests
```

**Deliverables:**
- Security vulnerability report and fixes
- Performance optimization (ViewState reduction, caching, async operations)
- Test suite with 75%+ coverage
- Refactored code following enterprise patterns
- Updated documentation

### 2. WCF Service Refactoring
```
/dotnet48-refactor InventoryService WCF to implement repository pattern and improve testability
```

**Deliverables:**
- Repository pattern implementation
- Dependency injection setup
- Unit and integration tests
- Service contract optimization
- Performance improvements

### 3. Windows Service Modernization
```
Modernize OrderProcessing Windows service - implement async/await, add structured logging, and improve error handling
```

**Deliverables:**
- Async/await pattern implementation
- Structured logging with NLog
- Enhanced error handling and recovery
- Performance monitoring
- Automated deployment scripts

### 4. Entity Framework Optimization
```
/dotnet48-analyze ProductCatalog data access layer for Entity Framework performance issues
```

**Deliverables:**
- Query performance analysis
- N+1 query fixes
- Eager loading optimization
- Connection pooling configuration
- Compiled query implementation

### 5. Migration Assessment
```
/dotnet48-migrate assess OrderManagement application for .NET 8 migration
```

**Deliverables:**
- Compatibility analysis report
- Breaking changes documentation
- Migration strategy and roadmap
- Effort estimates
- Risk assessment
- Phased migration plan

### 6. Security Hardening
```
Perform security audit of PaymentProcessing WCF service and implement security best practices
```

**Deliverables:**
- Security vulnerability assessment
- Input validation implementation
- Output encoding for XSS prevention
- Authentication and authorization hardening
- Cryptography best practices
- SSL/TLS configuration
- Security testing suite

## Development Workflow

### 1. Legacy Assessment
- Review existing application architecture
- Analyze dependencies and version compatibility
- Identify security vulnerabilities
- Profile performance bottlenecks
- Assess modernization opportunities
- Document breaking change risks
- Plan migration pathways

### 2. Implementation
- Apply enterprise design patterns
- Implement security fixes
- Optimize performance
- Enhance error handling
- Add comprehensive logging
- Write unit and integration tests
- Update documentation

### 3. Quality Assurance
- Run security scans
- Verify test coverage
- Performance profiling
- Load testing
- Integration testing
- Deployment validation
- Documentation review

## Integration with Other Agents

The .NET Framework 4.8 Expert works seamlessly with:

- **csharp-developer** - C# optimization and best practices
- **enterprise-architect** - Architecture design and patterns
- **security-auditor** - Security hardening and compliance
- **database-administrator** - Entity Framework and SQL optimization
- **devops-engineer** - Deployment automation and CI/CD
- **windows-admin** - Windows integration and services
- **legacy-modernizer** - Modernization strategies and upgrades
- **performance-engineer** - Performance optimization and profiling

## Advanced Features

### Performance Optimization
- Memory management and garbage collection tuning
- Threading patterns (Thread Pool, async/await)
- Caching strategies (MemoryCache, output caching, distributed caching)
- Database optimization (connection pooling, query optimization)
- Network optimization (compression, chunking)
- Resource pooling and reuse
- Lazy initialization patterns

### Security Implementation
- Windows authentication integration
- Forms authentication with membership providers
- Role-based authorization
- Code access security (CAS)
- Cryptography (symmetric, asymmetric, hashing)
- SSL/TLS configuration
- Input validation and sanitization
- Output encoding for XSS prevention
- SQL injection prevention

### Testing Strategies
- NUnit unit testing patterns
- MSTest framework integration
- Moq for mocking dependencies
- Integration testing with databases
- Performance testing and profiling
- Load testing with Visual Studio
- Security testing
- Code coverage analysis

## Best Practices

1. **Stability First**
   - Maintain backward compatibility
   - Test thoroughly before deployment
   - Implement graceful degradation
   - Use feature flags for changes

2. **Security Hardening**
   - Validate all inputs
   - Encode all outputs
   - Use parameterized queries
   - Implement proper authentication/authorization
   - Keep dependencies updated

3. **Performance Optimization**
   - Profile before optimizing
   - Implement caching strategically
   - Use async/await for I/O operations
   - Optimize database queries
   - Monitor resource usage

4. **Code Quality**
   - Follow .NET conventions
   - Apply SOLID principles
   - Write self-documenting code
   - Maintain comprehensive documentation
   - Conduct code reviews

5. **Enterprise Integration**
   - Design for scalability
   - Implement proper logging
   - Use dependency injection
   - Apply enterprise patterns
   - Plan for disaster recovery

## Troubleshooting

### Common Issues

**Security vulnerabilities:**
```
/dotnet48-analyze <application-name> for security issues
```

**Performance problems:**
```
/dotnet48-analyze <application-name> --focus performance
```

**Migration questions:**
```
/dotnet48-migrate assess <application-name>
```

**Test coverage:**
```
/dotnet48-test <component-name> --coverage-target 80
```

**Refactoring legacy code:**
```
/dotnet48-refactor <module-name> --apply repository-pattern
```

## Support

For issues, improvements, or questions about this agent:
- Check existing documentation in CLAUDE.md
- Review example use cases above
- Consult with related specialist agents
- Reference official .NET Framework documentation
- Review Microsoft enterprise application patterns

## License

Part of the Claude Agent Marketplace - Language Specialists category.
