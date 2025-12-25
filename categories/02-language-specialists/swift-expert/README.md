# Swift Expert Agent

Expert Swift developer specializing in Swift 5.9+ with async/await, SwiftUI, and protocol-oriented programming. Masters Apple platforms development, server-side Swift, and modern concurrency with emphasis on safety and expressiveness.

## Overview

This agent provides comprehensive Swift development expertise across all Apple platforms (iOS, macOS, watchOS, tvOS) and server-side Swift applications. It emphasizes modern Swift features, type safety, protocol-oriented design, and performance optimization.

## Features

### Core Capabilities

- **Modern Swift Development**: Swift 5.9+ features including async/await, actors, and structured concurrency
- **SwiftUI Expertise**: Declarative UI development with state management, animations, and custom layouts
- **Protocol-Oriented Programming**: Advanced protocol design, associated types, and type erasure patterns
- **Concurrency Mastery**: Actor isolation, task groups, AsyncSequence, and race condition prevention
- **Memory Management**: ARC optimization, reference cycle prevention, and value semantics design
- **Server-Side Swift**: Vapor framework patterns, async route handlers, and microservices architecture
- **Performance Optimization**: Instruments profiling, launch time optimization, and energy efficiency
- **Testing Excellence**: XCTest best practices, async tests, UI testing, and performance benchmarks

### Quality Standards

- SwiftLint strict mode compliance
- 100% API documentation coverage
- 80%+ test coverage
- Zero memory leaks
- Sendable compliance verification
- Thread safety validation
- API design guidelines adherence

## Slash Commands

### `/swift-analyze`
Analyze Swift codebase for architecture patterns, concurrency usage, protocol design, and potential improvements.

**Usage:**
```
/swift-analyze
```

**Features:**
- Architecture pattern review
- Concurrency model assessment
- Protocol design analysis
- Type safety evaluation
- Memory management audit
- Performance baseline check
- Swift best practices verification

### `/swift-test`
Generate comprehensive test suites using XCTest including unit, async, UI, and performance tests.

**Usage:**
```
/swift-test
```

**Features:**
- Unit test generation
- Async test patterns
- UI testing strategies
- Performance benchmarks
- Mock object design
- Test doubles creation
- Coverage analysis

### `/swift-concurrency`
Review and optimize async/await patterns, actor isolation, structured concurrency, and Sendable compliance.

**Usage:**
```
/swift-concurrency
```

**Features:**
- Async/await pattern review
- Actor isolation verification
- Sendable compliance checking
- Race condition detection
- Task group optimization
- MainActor usage analysis
- Concurrency safety improvements

### `/swift-optimize`
Analyze and optimize Swift code for performance, memory management, launch time, and energy efficiency.

**Usage:**
```
/swift-optimize
```

**Features:**
- Instruments profiling setup
- Memory allocation analysis
- Launch time optimization
- Binary size reduction
- Energy efficiency improvements
- ARC optimization
- Whole module optimization configuration

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File system operations for reading and writing Swift code
- **github**: GitHub integration for repository management and collaboration
- **context7**: Documentation and API reference lookup for Swift and Apple frameworks
- **memory**: Conversation context and learning from previous interactions

## Usage Examples

### iOS App Development

```swift
// The agent helps with SwiftUI declarative UI
struct ContentView: View {
    @StateObject private var viewModel = ContentViewModel()

    var body: some View {
        NavigationStack {
            List(viewModel.items) { item in
                ItemRow(item: item)
            }
            .navigationTitle("Items")
            .task {
                await viewModel.loadItems()
            }
        }
    }
}
```

### Async/Await Concurrency

```swift
// The agent ensures proper concurrency patterns
actor DataManager {
    private var cache: [String: Data] = [:]

    func fetchData(for key: String) async throws -> Data {
        if let cached = cache[key] {
            return cached
        }

        let data = try await networkFetch(key)
        cache[key] = data
        return data
    }
}
```

### Protocol-Oriented Design

```swift
// The agent promotes protocol-first API design
protocol Identifiable {
    associatedtype ID: Hashable
    var id: ID { get }
}

protocol Repository {
    associatedtype Entity: Identifiable

    func fetch(id: Entity.ID) async throws -> Entity
    func save(_ entity: Entity) async throws
}
```

### Server-Side Swift with Vapor

```swift
// The agent helps with Vapor framework patterns
func routes(_ app: Application) throws {
    app.get("users", ":id") { req async throws -> User in
        guard let id = req.parameters.get("id", as: UUID.self) else {
            throw Abort(.badRequest)
        }

        return try await User.find(id, on: req.db)
            .unwrap(or: Abort(.notFound))
    }
}
```

## Development Workflow

1. **Architecture Analysis**
   - Platform target evaluation
   - Dependency analysis
   - Architecture pattern review
   - Concurrency model assessment

2. **Implementation Phase**
   - Protocol-first API design
   - Value types emphasis
   - Async/await throughout
   - Comprehensive documentation

3. **Quality Verification**
   - SwiftLint compliance
   - Test coverage validation
   - Instruments profiling
   - Sendable compliance checking
   - Memory leak detection

## Integration with Other Agents

The Swift Expert agent collaborates with:

- **mobile-developer**: Share iOS/macOS development insights
- **frontend-developer**: Provide SwiftUI patterns and approaches
- **react-native-dev**: Collaborate on native module bridges
- **backend-developer**: Coordinate API design and contracts
- **kotlin-specialist**: Support Kotlin Multiplatform integration
- **rust-engineer**: Assist with Swift/Rust FFI patterns

## Advanced Features

### SwiftUI Advanced Patterns
- Custom layouts protocol
- GeometryReader usage
- PreferenceKey system
- Metal shaders integration
- Canvas rendering

### Concurrency Patterns
- Distributed actors
- AsyncSequence implementation
- Continuation patterns
- Task priority management
- Structured concurrency

### Performance Optimization
- Instruments profiling workflows
- Time Profiler analysis
- Allocations tracking
- Launch time optimization
- Binary size reduction strategies

### Testing Strategies
- Snapshot testing
- UI automation
- Performance benchmarks
- Mock and stub patterns
- CI/CD integration

## Environment Variables

For GitHub integration, set:
```bash
export GITHUB_TOKEN="your-github-personal-access-token"
```

## Best Practices

The agent enforces:

- **Type Safety**: Leverage Swift's strong type system
- **Value Semantics**: Prefer value types over reference types
- **Protocol Composition**: Use protocols for flexibility
- **Async/Await**: Modern concurrency patterns throughout
- **Error Handling**: Comprehensive error propagation
- **Documentation**: Complete API documentation with markup
- **Testing**: High test coverage with multiple test types
- **Memory Safety**: ARC optimization and leak prevention

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

This agent configuration is part of the Claude Code Agent Marketplace project.
