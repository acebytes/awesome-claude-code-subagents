# JavaScript Pro Agent

Expert JavaScript developer specializing in modern ES2023+ features, asynchronous programming, and full-stack development. Masters both browser APIs and Node.js ecosystem with emphasis on performance and clean code patterns.

## Overview

The JavaScript Pro agent is a senior-level JavaScript developer with deep expertise in:

- Modern JavaScript ES2023+ and Node.js 20+
- Asynchronous programming patterns and event-driven architecture
- Functional and object-oriented programming paradigms
- Performance optimization and memory management
- Browser APIs, Service Workers, and PWAs
- Testing methodologies and quality assurance
- Build tooling, bundling, and optimization
- Security best practices and vulnerability prevention

## Quick Start

### Prerequisites

- Node.js 20 or higher
- GitHub Personal Access Token (for GitHub MCP server)

### Installation

1. Copy the `javascript-pro` directory to your Claude Code agents location
2. Set your `GITHUB_TOKEN` environment variable:
   ```bash
   export GITHUB_TOKEN=your_github_token_here
   ```

### Usage

Invoke the agent through Claude Code:

```
@javascript-pro Help me optimize this async function for better performance
```

## Slash Commands

### /js-analyze

Analyze JavaScript codebase for patterns, performance issues, and best practices compliance.

**Example:**
```
/js-analyze
```

This will:
- Evaluate module system usage
- Review async patterns and error handling
- Analyze bundle sizes and dependencies
- Check ESLint compliance
- Assess test coverage
- Identify performance bottlenecks
- Document technical debt

### /js-test

Set up or run JavaScript test suite with Jest, including coverage reports.

**Example:**
```
/js-test
```

This will:
- Configure Jest if not set up
- Run unit and integration tests
- Generate coverage reports
- Identify untested code paths
- Set up mocking strategies
- Configure snapshot testing

### /js-optimize

Optimize JavaScript code for performance, bundle size, and memory efficiency.

**Example:**
```
/js-optimize
```

This will:
- Analyze bundle sizes and reduce them
- Optimize memory usage and prevent leaks
- Implement code splitting
- Set up tree shaking
- Apply performance best practices
- Use Web Workers for heavy computations
- Optimize event handlers and listeners

### /js-debug

Debug JavaScript issues including async bugs, memory leaks, and runtime errors.

**Example:**
```
/js-debug
```

This will:
- Trace async execution flow
- Identify memory leaks
- Debug event loop issues
- Analyze stack traces
- Profile performance
- Check for race conditions
- Validate error handling

## Key Features

### Modern JavaScript Expertise

- ES2023+ features including top-level await, private fields, and pattern matching
- Optional chaining and nullish coalescing
- Temporal API for date/time handling
- WeakRef and FinalizationRegistry for memory management

### Asynchronous Programming

- Promise composition and error handling
- Async/await best practices
- AsyncIterator and generator patterns
- Stream processing and backpressure handling
- Event loop optimization

### Performance Optimization

- Memory leak prevention and detection
- Garbage collection optimization
- Virtual scrolling and lazy loading
- Web Worker and SharedArrayBuffer usage
- Performance API monitoring and profiling

### Testing & Quality

- Jest configuration and best practices
- 85%+ test coverage standards
- Unit, integration, and E2E testing
- Mocking and snapshot testing
- Performance benchmarking

### Build & Tooling

- Webpack, Rollup, and ESBuild expertise
- Tree shaking and code splitting
- Bundle size optimization
- Source map configuration
- Hot module replacement

### Security

- XSS and CSRF prevention
- Content Security Policy implementation
- Input sanitization
- Dependency vulnerability scanning
- Prototype pollution prevention

## MCP Servers

The agent uses four MCP servers:

1. **Filesystem** - File operations and project navigation
2. **GitHub** - Repository access, PR reviews, and issue management
3. **Context7** - Access to up-to-date JavaScript documentation
4. **Memory** - Persistent context and project knowledge

## Development Workflow

### 1. Code Analysis

The agent starts by understanding your project:
- Reviews package.json and dependencies
- Analyzes module system (ESM/CommonJS)
- Checks build configuration
- Assesses code patterns and style
- Evaluates test coverage
- Establishes performance baselines

### 2. Implementation

Development follows modern JavaScript best practices:
- Uses latest stable ES features
- Applies functional programming patterns
- Designs for testability
- Optimizes for performance
- Ensures type safety with JSDoc
- Implements comprehensive error handling
- Documents complex logic

### 3. Quality Assurance

Before delivery, the agent ensures:
- ESLint compliance with strict rules
- Prettier formatting applied
- 85%+ test coverage
- Bundle size optimization
- Performance benchmarks met
- Security vulnerabilities addressed
- Cross-browser compatibility verified

## Integration with Other Agents

The JavaScript Pro agent collaborates with:

- **typescript-pro** - Share modules and type definitions
- **frontend-developer** - Provide vanilla JS solutions
- **react-developer** - Supply utility functions and hooks
- **backend-developer** - Guide on Node.js patterns
- **webpack-specialist** - Optimize build configuration
- **performance-engineer** - Implement performance improvements
- **security-auditor** - Address security vulnerabilities
- **fullstack-developer** - Coordinate full-stack patterns

## Best Practices

The agent follows these principles:

1. **Code Quality** - Readable, maintainable, and well-documented code
2. **Performance** - Optimized for speed and memory efficiency
3. **Testing** - Comprehensive test coverage with multiple strategies
4. **Security** - Built-in protection against common vulnerabilities
5. **Modern Standards** - Uses latest stable JavaScript features
6. **Clean Architecture** - SOLID principles and design patterns
7. **Progressive Enhancement** - Works across browsers and environments
8. **Error Handling** - Graceful degradation and comprehensive error boundaries

## Example Use Cases

### Optimize Async Code

```javascript
// Agent will transform callback-based code to modern async/await
// with proper error handling and performance optimization
```

### Set Up Testing

```javascript
// Agent will configure Jest with optimal settings,
// create test files, and achieve 85%+ coverage
```

### Debug Memory Leaks

```javascript
// Agent will identify leaks, fix closures,
// and implement proper cleanup patterns
```

### Improve Bundle Size

```javascript
// Agent will analyze dependencies, implement code splitting,
// and reduce bundle size by 40%+
```

## Technical Requirements

- **Node.js**: 20.0.0 or higher
- **Environment Variables**: GITHUB_TOKEN for GitHub integration
- **Browser Targets**: Modern evergreen browsers
- **Module System**: ESM (with CommonJS compatibility where needed)

## Support

For issues, questions, or contributions related to this agent, please refer to the main marketplace repository.

## License

MIT
