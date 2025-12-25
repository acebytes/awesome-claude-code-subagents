# C++ Pro - Expert C++ Development Agent

Expert C++ developer specializing in modern C++20/23, systems programming, and high-performance computing. Masters template metaprogramming, zero-overhead abstractions, and low-level optimization with emphasis on safety and efficiency.

## Overview

C++ Pro is your go-to agent for advanced C++ development, focusing on:

- Modern C++20/23 features and idioms
- High-performance computing and optimization
- Template metaprogramming and compile-time computation
- Systems programming and embedded development
- Memory safety and zero-overhead abstractions
- Concurrent and parallel programming patterns

## Features

### Core Capabilities

- **Modern C++ Mastery**: Concepts, ranges, coroutines, modules, and C++20/23 features
- **Template Metaprogramming**: Variadic templates, SFINAE, type traits, and compile-time computation
- **Performance Optimization**: SIMD, cache optimization, profile-guided optimization, and assembly inspection
- **Memory Management**: Smart pointers, custom allocators, RAII patterns, and move semantics
- **Concurrency**: Lock-free data structures, atomics, parallel STL, and thread pools
- **Systems Programming**: OS APIs, device drivers, embedded systems, and real-time constraints

### Quality Assurance

- C++ Core Guidelines compliance
- Static analysis with clang-tidy and cppcheck
- Sanitizers (AddressSanitizer, UBSanitizer)
- Valgrind memory leak detection
- Comprehensive test coverage
- Zero compiler warnings

## Slash Commands

### /cpp-analyze

Perform comprehensive C++ codebase analysis:
- Build system configuration review
- Template instantiation analysis
- Memory usage profiling
- Performance bottleneck identification
- Undefined behavior detection
- Compiler warning review
- ABI compatibility assessment

```bash
# Example usage
/cpp-analyze
```

### /cpp-memory-check

Execute thorough memory safety verification:
- AddressSanitizer test execution
- Valgrind memory leak detection
- Buffer overflow checks
- Smart pointer usage verification
- RAII pattern compliance
- Allocation pattern analysis
- UBSanitizer testing

```bash
# Example usage
/cpp-memory-check
```

### /cpp-optimize

Optimize C++ code for maximum performance:
- Performance profiling (perf/vtune)
- Cache behavior analysis
- Assembly output review
- SIMD optimization application
- Memory layout optimization
- Lock-free algorithm implementation
- Link-time optimization
- Profile-guided optimization

```bash
# Example usage
/cpp-optimize
```

### /cpp-modernize

Modernize legacy C++ code to C++20/23:
- Smart pointer migration
- constexpr conversion from macros
- Range-based for loop upgrades
- Structured binding application
- Concept-based constraints
- Ranges library migration
- Three-way comparison operators
- Designated initializers

```bash
# Example usage
/cpp-modernize
```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File system access for reading/writing C++ source files and build configurations
- **github**: GitHub integration for repository management and code collaboration
- **context7**: Access to up-to-date C++ library documentation and best practices
- **memory**: Persistent memory for project context, build configurations, and optimization history

## Requirements

### Compilers

- GCC 11+ (recommended for latest C++20/23 support)
- Clang 14+ (excellent diagnostics and tooling)
- MSVC 2022+ (Windows development)

### Build Tools

- CMake 3.20+
- Ninja (fast builds)
- Conan (package management)

### Analysis Tools

- clang-tidy (static analysis)
- cppcheck (additional static analysis)
- AddressSanitizer (memory error detection)
- UBSanitizer (undefined behavior detection)
- Valgrind (memory leak detection)

## Usage Examples

### Example 1: High-Performance Data Structure

```cpp
// Request optimization for a container
"I need a lock-free concurrent queue optimized for high throughput with
multiple producers and consumers. It should be cache-friendly and use
modern C++20 features."
```

C++ Pro will:
1. Design with concepts for type safety
2. Implement lock-free algorithms with atomics
3. Optimize memory layout for cache efficiency
4. Use C++20 coroutines if beneficial
5. Provide comprehensive tests
6. Verify with sanitizers

### Example 2: Template Metaprogramming

```cpp
// Request compile-time computation
"Create a compile-time expression template library for linear algebra
that eliminates temporary objects and supports SIMD optimization."
```

C++ Pro will:
1. Design with C++20 concepts
2. Use variadic templates and fold expressions
3. Implement CRTP for static polymorphism
4. Apply constexpr for compile-time computation
5. Enable SIMD auto-vectorization
6. Provide zero-overhead abstractions

### Example 3: Systems Programming

```cpp
// Request embedded system code
"Implement a real-time task scheduler for an embedded ARM Cortex-M4
with interrupt handling, watchdog support, and deterministic timing."
```

C++ Pro will:
1. Use static allocation only
2. Implement interrupt-safe patterns
3. Optimize for code size and speed
4. Ensure deterministic execution
5. Integrate watchdog timer
6. Provide timing analysis

## Best Practices

### Code Quality

- Follow C++ Core Guidelines
- Enable all compiler warnings (-Wall -Wextra)
- Run static analysis on every build
- Use sanitizers in testing
- Maintain zero undefined behavior
- Document complex template interfaces

### Performance

- Profile before optimizing
- Optimize for cache locality
- Use constexpr for compile-time computation
- Minimize dynamic allocation
- Prefer value semantics with move
- Use SIMD when beneficial

### Safety

- Apply RAII universally
- Use smart pointers by default
- Mark functions noexcept when appropriate
- Ensure exception safety guarantees
- Use const correctness throughout
- Leverage type system for safety

## Integration with Other Agents

C++ Pro collaborates effectively with:

- **python-pro**: Provide C APIs for Python bindings
- **rust-engineer**: Share memory safety and zero-cost abstraction techniques
- **game-developer**: Support with high-performance engine code
- **embedded-systems**: Guide on driver development and real-time systems
- **golang-pro**: Assist with CGO interfaces
- **performance-engineer**: Collaborate on optimization strategies
- **security-auditor**: Help with memory safety audits
- **java-architect**: Support JNI interface development

## Troubleshooting

### Compilation Issues

- Check compiler version supports required C++ standard
- Verify CMake configuration for correct flags
- Review template error messages carefully
- Use concepts to improve error messages

### Performance Issues

- Profile with perf or vtune first
- Check for unexpected dynamic allocation
- Review assembly output for optimization opportunities
- Ensure compiler optimizations are enabled

### Memory Issues

- Run with AddressSanitizer
- Check with Valgrind
- Review smart pointer ownership
- Verify RAII pattern compliance

## Resources

- [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)
- [cppreference.com](https://en.cppreference.com/)
- [Compiler Explorer](https://godbolt.org/)
- [Quick C++ Benchmark](https://quick-bench.com/)

## License

Part of the Claude Code Agent Marketplace.

## Contributing

Contributions welcome! Please ensure:
- Code follows C++ Core Guidelines
- All tests pass with sanitizers
- Static analysis is clean
- Documentation is updated
- Performance benchmarks are included
