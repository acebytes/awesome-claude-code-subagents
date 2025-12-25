# Rust Engineer Agent

Expert Rust developer specializing in systems programming, memory safety, and zero-cost abstractions. Masters ownership patterns, async programming, and performance optimization for mission-critical applications.

## Overview

The Rust Engineer agent is a senior Rust developer with deep expertise in Rust 2021 edition and its ecosystem. It specializes in:

- Systems programming and embedded development
- Memory safety and ownership patterns
- Zero-cost abstractions
- High-performance application development
- Async programming with tokio/async-std
- FFI and cross-language interop
- WebAssembly development

## Installation

1. Copy the `rust-engineer` directory to your Claude Code agents location
2. Ensure you have the required MCP servers installed (they will be installed automatically via npx)
3. Set the `GITHUB_TOKEN` environment variable if you want to use GitHub integration

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access to local filesystem for reading/writing Rust code
- **github**: GitHub integration for repository operations
- **context7**: Access to up-to-date Rust documentation and crate information
- **memory**: Persistent memory for project context and learned patterns

## Slash Commands

### /rust-analyze

Performs comprehensive analysis of your Rust codebase:

- Ownership patterns and lifetime analysis
- Unsafe code audit and documentation review
- Trait hierarchy and implementation review
- Memory allocation patterns identification
- Performance characteristics assessment
- Cross-platform compatibility check

**Usage:**
```
/rust-analyze
```

### /rust-test

Executes a comprehensive testing strategy:

- Runs `cargo test` with all features
- Executes doctests for documentation examples
- Performs property-based testing with proptest
- Runs fuzzing with cargo-fuzz
- Executes MIRI for undefined behavior detection
- Generates test coverage reports

**Usage:**
```
/rust-test
```

### /rust-optimize

Optimizes Rust code for maximum performance:

- Profiles code with cargo flamegraph
- Benchmarks with criterion
- Analyzes assembly output for hot paths
- Identifies allocation hotspots
- Suggests zero-cost abstractions
- Enables LTO and PGO optimizations
- Recommends SIMD opportunities

**Usage:**
```
/rust-optimize
```

### /rust-unsafe-audit

Performs comprehensive safety audit:

- Identifies all unsafe blocks in codebase
- Documents safety invariants
- Verifies soundness properties
- Checks FFI boundary safety
- Runs MIRI verification
- Reviews memory ownership patterns
- Validates thread safety guarantees

**Usage:**
```
/rust-unsafe-audit
```

## Capabilities

### Core Expertise

- **Ownership System**: Lifetime management, borrowing rules, smart pointers (Box, Rc, Arc)
- **Trait System**: Generic programming, associated types, trait objects, extension traits
- **Error Handling**: Custom error types with thiserror/anyhow, Result combinators
- **Async Programming**: tokio/async-std, Future trait, Pin semantics, async patterns
- **Performance**: Zero-allocation APIs, SIMD, const evaluation, LTO/PGO
- **Memory Management**: Custom allocators, arena allocation, no-std development

### Advanced Features

- **Macro Development**: Declarative and procedural macros with quote/syn
- **FFI**: C API design, bindgen/cbindgen, memory safety across language boundaries
- **Embedded**: no_std compliance, interrupt handlers, real-time constraints
- **WebAssembly**: wasm-bindgen, size optimization, JS interop
- **Concurrency**: Lock-free algorithms, channels, Rayon parallelism
- **Testing**: Property-based testing, fuzzing, MIRI verification

### Build and Tooling

- Cargo workspace organization
- Feature flag strategies
- Cross-compilation setup
- CI/CD integration
- Documentation generation
- Dependency auditing

## Development Workflow

1. **Architecture Analysis**
   - Reviews Cargo.toml and workspace structure
   - Analyzes ownership patterns and lifetimes
   - Audits unsafe code and FFI boundaries
   - Assesses performance characteristics

2. **Implementation Phase**
   - Designs ownership-first APIs
   - Implements zero-cost abstractions
   - Applies type state patterns
   - Minimizes allocations
   - Documents safety invariants

3. **Safety Verification**
   - Runs MIRI for undefined behavior
   - Resolves clippy warnings
   - Verifies benchmarks meet targets
   - Ensures comprehensive documentation
   - Validates cross-platform compatibility

## Quality Standards

Every Rust implementation follows these standards:

- ✅ Zero unsafe code outside of core abstractions
- ✅ clippy::pedantic compliance
- ✅ Complete documentation with examples
- ✅ Comprehensive test coverage including doctests
- ✅ Benchmark performance-critical code
- ✅ MIRI verification for unsafe blocks
- ✅ No memory leaks or data races
- ✅ Cargo.lock committed for reproducibility

## Integration with Other Agents

The Rust Engineer agent collaborates effectively with:

- **python-pro**: Provides FFI bindings for Python-Rust interop
- **golang-pro**: Shares performance techniques and patterns
- **cpp-developer**: Supports Rust/C++ interop and migration
- **java-architect**: Guides on JNI bindings
- **embedded-systems**: Collaborates on driver development
- **wasm-developer**: Works on WebAssembly bindings
- **security-auditor**: Helps with memory safety analysis
- **performance-engineer**: Assists with optimization strategies

## Example Usage

### Analyzing a Rust Project

```
/rust-analyze

The agent will review your Cargo workspace, analyze ownership patterns,
audit unsafe code, and provide a comprehensive assessment.
```

### Running Comprehensive Tests

```
/rust-test

Executes full test suite including unit tests, doctests, property-based
tests, fuzzing, and MIRI verification.
```

### Performance Optimization

```
/rust-optimize

Profiles your code, identifies bottlenecks, suggests optimizations,
and implements zero-cost abstractions.
```

### Safety Audit

```
/rust-unsafe-audit

Reviews all unsafe code, documents invariants, verifies soundness,
and ensures memory safety guarantees.
```

## Best Practices

### Memory Safety
- Minimize unsafe code to core abstractions
- Document all safety invariants
- Use MIRI for verification
- Prefer safe abstractions over raw pointers

### Performance
- Profile before optimizing
- Use zero-cost abstractions
- Leverage const evaluation
- Consider SIMD for hot paths
- Apply LTO/PGO for release builds

### Testing
- Write doctests for all public APIs
- Use property-based testing for invariants
- Fuzz parser and deserializer code
- Run MIRI regularly
- Maintain high test coverage

### Error Handling
- Use custom error types with thiserror
- Provide context with anyhow in applications
- Design fallible operations carefully
- Avoid panics in library code

## Environment Variables

- `GITHUB_TOKEN`: Required for GitHub integration
- `PWD`: Used for filesystem access (automatically set)

## Requirements

- Node.js and npx (for MCP servers)
- Rust toolchain (cargo, rustc, clippy, miri)
- Optional: cargo-fuzz, criterion, proptest for advanced testing

## Support

For issues, questions, or contributions related to this agent, please refer to the main Claude Code Agent Marketplace repository.

## License

This agent is provided as part of the Claude Code Agent Marketplace.
