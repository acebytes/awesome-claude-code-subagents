# Kotlin Specialist Agent

Expert Kotlin developer specializing in coroutines, multiplatform development, and Android applications. Masters functional programming patterns, DSL design, and modern Kotlin features with emphasis on conciseness and safety.

## Overview

This agent is a senior Kotlin developer with deep expertise in Kotlin 1.9+ and its ecosystem. It specializes in:

- **Coroutines & Concurrency**: Structured concurrency, Flow API, StateFlow/SharedFlow, and coroutine scope management
- **Kotlin Multiplatform**: Common code maximization, expect/actual patterns, and cross-platform library development
- **Android Development**: Jetpack Compose, ViewModel architecture, and modern Android best practices
- **Server-Side Development**: Ktor framework, routing DSLs, and WebSocket support
- **Functional Programming**: Arrow.kt integration, monadic patterns, and immutability
- **DSL Design**: Type-safe builders, lambda with receiver, and fluent interfaces

## Capabilities

- Idiomatic Kotlin code with null safety and type inference
- Advanced coroutine patterns and Flow transformations
- Multiplatform architecture (JVM, Android, iOS, JS, WASM)
- Jetpack Compose UI development
- Ktor server and client implementation
- Custom DSL creation
- Performance optimization and profiling
- Comprehensive testing with JUnit 5, MockK, and coroutine test support

## Installation

1. Ensure you have the required MCP servers installed:
   - `@modelcontextprotocol/server-filesystem`
   - `@modelcontextprotocol/server-github`
   - `@upstash/context7-mcp`
   - `@modelcontextprotocol/server-memory`

2. Set up environment variables:
   ```bash
   export GITHUB_TOKEN="your_github_token_here"
   ```

3. Configure the agent using the provided `mcp-config.json`

## Usage

### Basic Invocation

Invoke this agent when you need:
- Kotlin code development or refactoring
- Coroutine-based concurrent programming
- Multiplatform library or application development
- Android app development with Jetpack Compose
- Server-side development with Ktor
- Custom DSL creation
- Functional programming patterns in Kotlin

### Slash Commands

#### `/kotlin-analyze`
Performs comprehensive analysis of your Kotlin codebase:
- Evaluates idiomatic Kotlin usage
- Checks null safety patterns
- Reviews coroutine implementations
- Assesses multiplatform setup
- Analyzes performance patterns
- Reviews DSL designs
- Checks test coverage
- Generates improvement recommendations

Example:
```
/kotlin-analyze
```

#### `/kotlin-test`
Generates and executes comprehensive test suites:
- Unit tests with JUnit 5
- Coroutine tests with test dispatchers
- MockK mocking setup
- Property-based tests
- Multiplatform test configuration
- Compose UI tests
- Integration tests
- Performance benchmarks

Example:
```
/kotlin-test
```

#### `/kotlin-coroutines`
Deep dive into coroutine patterns and optimization:
- Analyzes coroutine scope usage
- Reviews Flow implementations
- Checks structured concurrency
- Evaluates dispatcher selection
- Tests exception handling
- Optimizes performance
- Debugs coroutine leaks
- Designs concurrent patterns

Example:
```
/kotlin-coroutines
```

#### `/kotlin-dsl`
Design and implement type-safe DSLs:
- Creates builder patterns
- Implements lambda with receiver
- Designs infix functions
- Sets up operator overloading
- Configures context receivers
- Controls scope visibility
- Builds fluent interfaces
- Generates Gradle plugins

Example:
```
/kotlin-dsl
```

## Development Workflow

### 1. Architecture Analysis
The agent begins by understanding your Kotlin project:
- Reviews project structure and build configuration
- Analyzes multiplatform setup (if applicable)
- Evaluates existing coroutine patterns
- Checks dependency management
- Verifies code style compliance (Detekt, ktlint)

### 2. Implementation
Develops solutions following Kotlin best practices:
- Designs with coroutines first
- Uses sealed classes for state management
- Applies functional programming patterns
- Creates expressive DSLs when appropriate
- Maximizes common code in multiplatform projects
- Implements comprehensive KDoc documentation

### 3. Quality Assurance
Ensures code quality and cross-platform compatibility:
- Runs Detekt static analysis
- Applies ktlint formatting
- Executes tests across all platforms
- Checks for coroutine leaks
- Verifies performance benchmarks
- Ensures API stability

## Quality Standards

- **Test Coverage**: Minimum 85%
- **Static Analysis**: Detekt passing, ktlint compliant
- **Null Safety**: Enforced throughout codebase
- **Documentation**: Complete KDoc for public APIs
- **Explicit API Mode**: Enabled for library projects
- **Coroutine Safety**: Proper exception handling and scope management

## Technology Stack

### Languages
- Kotlin 1.9+

### Frameworks
- Jetpack Compose (Android & Multiplatform)
- Ktor (Server & Client)
- Kotlin Multiplatform
- Android Jetpack
- Arrow.kt (Functional Programming)

### Tools
- Gradle (Kotlin DSL)
- Detekt (Static Analysis)
- ktlint (Code Formatting)
- JUnit 5 (Testing)
- MockK (Mocking)
- Android Studio / IntelliJ IDEA

## Integration with Other Agents

This agent collaborates with:
- **java-architect**: Shares JVM insights and interoperability patterns
- **mobile-developer**: Provides Android expertise
- **gradle-expert**: Collaborates on build configuration
- **frontend-developer**: Works on Compose Web projects
- **backend-developer**: Supports Ktor API development
- **ios-developer**: Guides on multiplatform iOS integration
- **rust-engineer**: Helps with native interop
- **typescript-pro**: Assists with Kotlin/JS target

## Best Practices

### Coroutines
- Always use structured concurrency
- Prefer Flow over channels for data streams
- Use appropriate dispatchers (Main, IO, Default)
- Handle exceptions with supervisorScope when needed
- Test coroutines with TestCoroutineDispatcher

### Multiplatform
- Maximize common code
- Use expect/actual only when necessary
- Create platform-specific implementations in separate source sets
- Test on all target platforms
- Document platform-specific behavior

### Android
- Follow Compose best practices
- Use ViewModel for state management
- Implement proper lifecycle handling
- Apply Material 3 design guidelines
- Optimize for performance with Baseline Profiles

### DSL Design
- Use type-safe builders
- Apply lambda with receiver appropriately
- Control scope with @DslMarker
- Make DSLs discoverable and intuitive
- Document DSL usage patterns

## Example Interactions

### Creating a Multiplatform Library
```
I need to create a multiplatform HTTP client library that works on Android, iOS, and JVM.
```

The agent will:
1. Set up Kotlin Multiplatform project structure
2. Design common API using coroutines and Flow
3. Implement platform-specific networking (OkHttp for JVM/Android, NSURLSession for iOS)
4. Create comprehensive test suite for all platforms
5. Configure Gradle build scripts
6. Generate documentation

### Implementing Coroutine Flow Pattern
```
/kotlin-coroutines
Help me implement a reactive data layer using Kotlin Flow
```

The agent will:
1. Analyze existing data layer architecture
2. Design Flow-based data streams
3. Implement proper error handling
4. Set up appropriate dispatchers
5. Create test coverage with turbine or similar
6. Optimize for performance

### Building a Type-Safe DSL
```
/kotlin-dsl
Create a type-safe DSL for building UI forms with validation
```

The agent will:
1. Design DSL structure with builders
2. Implement lambda with receiver patterns
3. Add scope control with @DslMarker
4. Create validation combinators
5. Provide usage examples
6. Document the DSL API

## Troubleshooting

### Common Issues

**Issue**: Coroutine leaks detected
- **Solution**: Review coroutine scope management, ensure proper cancellation, use structured concurrency

**Issue**: Multiplatform build fails
- **Solution**: Check source set configuration, verify platform-specific dependencies, review expect/actual declarations

**Issue**: Detekt violations
- **Solution**: Run ktlint format, review Detekt rules, refactor code to follow Kotlin idioms

**Issue**: Test failures on specific platform
- **Solution**: Check platform-specific implementations, verify test configuration, review platform constraints

## Contributing

When extending this agent:
1. Maintain focus on Kotlin idioms and best practices
2. Keep up with latest Kotlin releases and features
3. Update multiplatform strategies as ecosystem evolves
4. Add new coroutine patterns and Flow transformations
5. Include examples for new DSL patterns

## Version History

- **1.0.0**: Initial release with Kotlin 1.9+ support, coroutines, multiplatform, Android, and Ktor expertise

## License

Part of the Claude Code Agent Marketplace.
