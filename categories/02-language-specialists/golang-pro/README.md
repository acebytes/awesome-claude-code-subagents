# Golang Pro Agent

Expert Go developer specializing in high-performance systems, concurrent programming, and cloud-native microservices. Masters idiomatic Go patterns with emphasis on simplicity, efficiency, and reliability.

## Overview

The Golang Pro agent is your senior Go developer companion, bringing deep expertise in Go 1.21+ and its ecosystem. This agent specializes in building efficient, concurrent, and scalable systems with a focus on microservices architecture, CLI tools, system programming, and cloud-native applications.

## Core Expertise

- **Go 1.21+ Development**: Expert knowledge of modern Go features and best practices
- **Concurrent Programming**: Master of goroutines, channels, and synchronization patterns
- **Microservices Architecture**: Building scalable, distributed systems
- **Performance Optimization**: CPU/memory profiling, zero-allocation techniques, benchmarking
- **Cloud-Native Applications**: Kubernetes operators, service mesh integration, observability
- **Testing Excellence**: Table-driven tests, fuzzing, race detection, 80%+ coverage
- **gRPC & REST APIs**: High-performance service implementation
- **Memory Management**: Understanding escape analysis, GC tuning, efficient allocation

## Features

### Idiomatic Go Development
- Follows Go proverbs and community best practices
- Interface composition over inheritance
- Accept interfaces, return structs
- Channels for orchestration, mutexes for state
- Error values over exceptions
- Small, focused interfaces

### Concurrency Mastery
- Goroutine lifecycle management
- Channel patterns and pipelines
- Context for cancellation and deadlines
- Worker pools with bounded concurrency
- Fan-in/fan-out patterns
- Rate limiting and backpressure

### Quality Assurance
- gofmt and golangci-lint compliance
- Comprehensive error handling with wrapping
- Table-driven tests with subtests
- Benchmark critical code paths
- Race condition free code
- Documentation for all exported items

## Slash Commands

### /go-analyze
Analyze Go codebase for patterns, performance issues, and best practice violations.

**What it does:**
- Reviews code structure and package organization
- Analyzes concurrency patterns and goroutine usage
- Evaluates error handling approaches
- Assesses testing coverage and quality
- Identifies performance bottlenecks
- Checks for security vulnerabilities

**Example usage:**
```
/go-analyze
```

### /go-test
Execute comprehensive testing suite with race detector and coverage reports.

**What it does:**
- Runs all tests with race detector enabled
- Generates detailed coverage reports
- Executes table-driven tests
- Performs integration tests
- Runs fuzz testing where applicable
- Validates test quality and completeness

**Example usage:**
```
/go-test
```

### /go-benchmark
Run and analyze performance benchmarks with CPU and memory profiling.

**What it does:**
- Executes full benchmark suite
- Profiles CPU and memory usage
- Compares benchmark results over time
- Identifies allocation hotspots
- Analyzes escape analysis results
- Suggests performance optimizations

**Example usage:**
```
/go-benchmark
```

### /go-lint
Run comprehensive linting and formatting checks with golangci-lint.

**What it does:**
- Executes gofmt and goimports
- Runs golangci-lint with all enabled linters
- Checks for common mistakes
- Validates documentation completeness
- Verifies naming conventions
- Ensures Go best practices compliance

**Example usage:**
```
/go-lint
```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access and manage project files
- **github**: GitHub repository integration for code review and collaboration
- **context7**: Context-aware documentation and API reference
- **memory**: Maintain context across sessions for better development continuity

## Use Cases

### High-Performance Microservices
Build scalable microservices with gRPC/REST APIs achieving sub-millisecond p99 latency. Includes service discovery, circuit breakers, and distributed tracing.

### Concurrent Systems and Pipelines
Develop efficient concurrent systems using goroutines, channels, and synchronization primitives. Implement fan-in/fan-out patterns, worker pools, and rate limiting.

### CLI Tools and Utilities
Create professional command-line tools with clean interfaces, subcommands, and comprehensive help systems using popular frameworks.

### Cloud-Native Applications
Build container-aware applications, Kubernetes operators, and serverless functions with proper observability and configuration management.

### Performance Optimization
Profile and optimize existing Go applications for CPU, memory, and latency using pprof, benchmarking, and zero-allocation techniques.

### Production-Ready Code
Write maintainable, well-tested Go code with comprehensive error handling, graceful shutdown, and full documentation.

## Development Workflow

### 1. Project Assessment
The agent begins by understanding your Go project:
- Module structure and dependencies
- Build configuration and tooling
- Testing setup and coverage
- Deployment targets
- Performance requirements

### 2. Architecture Analysis
Reviews and evaluates:
- Package organization and interfaces
- Concurrency patterns
- Error handling strategies
- Testing approach
- Performance characteristics
- Security practices

### 3. Implementation
Develops solutions with focus on:
- Clear interface contracts
- Composition and dependency injection
- Functional options pattern
- Testable components
- Explicit error handling
- Performance optimization

### 4. Quality Assurance
Ensures production readiness:
- gofmt and golangci-lint compliance
- 80%+ test coverage
- Benchmark documentation
- Race detector clean
- Zero goroutine leaks
- Complete API documentation

## Integration Capabilities

Works seamlessly with other specialized agents:
- **Frontend Developers**: Provides well-documented REST/GraphQL APIs
- **Backend Developers**: Shares service contracts and integration patterns
- **DevOps Engineers**: Collaborates on deployment and CI/CD optimization
- **Kubernetes Specialists**: Assists with operator patterns and service mesh
- **Other Language Specialists**: Supports CGO interfaces and gRPC integration

## Best Practices

### Code Quality
- Follow effective Go guidelines
- Use golangci-lint for consistency
- Write comprehensive tests
- Document all exported items
- Handle errors explicitly

### Performance
- Profile before optimizing
- Write benchmarks for critical paths
- Use zero-allocation techniques where appropriate
- Pre-allocate slices and maps
- Leverage sync.Pool for object pooling

### Concurrency
- Propagate context through all APIs
- Use channels for orchestration
- Apply mutexes for state protection
- Implement graceful shutdown
- Prevent goroutine leaks

### Testing
- Write table-driven tests
- Use subtests for organization
- Enable race detector in CI
- Maintain 80%+ coverage
- Include integration tests

## Requirements

- Go 1.21 or higher
- gofmt (included with Go)
- golangci-lint for comprehensive linting

## Getting Started

1. Ensure Go 1.21+ is installed
2. Install golangci-lint for linting support
3. Set up your development environment
4. Invoke the agent to begin Go development

The agent will query your project context and adapt to your specific needs, whether you're building microservices, CLI tools, or cloud-native applications.

## Example Interactions

**Building a gRPC Service:**
> "Create a user authentication gRPC service with JWT token generation and refresh logic"

The agent will design clean interface contracts, implement the service with proper error handling, add comprehensive tests, and include observability hooks.

**Optimizing Performance:**
> "Profile and optimize the data processing pipeline - it's using too much memory"

The agent will profile the code, identify allocation hotspots, suggest zero-allocation techniques, and benchmark the improvements.

**Code Review:**
> "/go-analyze - review my new concurrent worker pool implementation"

The agent will analyze the concurrency patterns, check for race conditions, verify graceful shutdown, and suggest improvements following Go best practices.

---

**Always prioritize simplicity, clarity, and performance while building reliable and maintainable Go systems.**
