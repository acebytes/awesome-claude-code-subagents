# Code Reviewer Agent

> Expert code reviewer specializing in code quality, security vulnerabilities, and best practices across multiple languages

## Overview

The Code Reviewer agent is a senior code reviewer with expertise in identifying code quality issues, security vulnerabilities, and optimization opportunities. It masters static analysis, design patterns, and performance optimization with focus on maintainability and technical debt reduction across all major programming languages.

## Capabilities

### Primary Skills
- **Code Quality Assessment**: Logic correctness, error handling, naming conventions, code organization
- **Security Review**: Vulnerability detection, injection prevention, authentication/authorization checks
- **Performance Analysis**: Algorithm efficiency, database optimization, memory leak detection
- **Design Patterns**: SOLID principles, DRY compliance, appropriate pattern usage
- **Test Review**: Coverage analysis, test quality, edge case validation
- **Documentation Review**: API docs, inline comments, architecture documentation
- **Dependency Analysis**: Security scanning, license compliance, version management
- **Technical Debt**: Code smell detection, refactoring priorities, modernization opportunities

### Supported Languages
JavaScript, TypeScript, Python, Java, Go, C#, Ruby, PHP, Rust, Kotlin

### MCP Server Integrations

| Server | Purpose | Required |
|--------|---------|----------|
| filesystem | Read/write code review reports and analysis | Yes |
| github | Access pull requests and create review comments | Yes |
| context7 | Understand codebase architecture and patterns | No |
| memory | Track review patterns and team preferences | No |

## Usage

### Slash Commands

| Command | Description | Example |
|---------|-------------|---------|
| `/code-review` | Comprehensive code review on current changes | `/code-review` |
| `/security-scan` | Focus on security vulnerabilities | `/security-scan` |
| `/tech-debt` | Identify technical debt items | `/tech-debt` |
| `/best-practices` | Verify coding standards | `/best-practices` |

### Example Prompts

**Security Review**
```
Review the authentication module for security issues
```
Performs security-focused review identifying vulnerabilities, injection risks, and security anti-patterns with remediation guidance.

**Performance Analysis**
```
Analyze the performance of the database query layer
```
Reviews database queries for N+1 problems, missing indexes, inefficient joins, and provides optimization recommendations.

**Design Pattern Validation**
```
Check if the new API follows REST best practices
```
Validates API design against REST principles, HTTP method usage, status codes, and resource modeling.

**Test Coverage Review**
```
Review test coverage and quality for the payment service
```
Analyzes test completeness, quality, edge cases, mock usage, and provides improvement suggestions.

**Technical Debt Analysis**
```
Identify technical debt in the legacy user management code
```
Scans for code smells, outdated patterns, refactoring needs, and provides prioritized remediation plan.

## Requirements

### API Keys

#### Required
- `GITHUB_TOKEN` - GitHub Personal Access Token for accessing repositories and creating review comments
  - Obtain at: https://github.com/settings/tokens
  - Scopes needed: `repo`, `read:org`

#### Optional
- `UPSTASH_VECTOR_REST_URL` - Upstash Vector database URL for codebase context
- `UPSTASH_VECTOR_REST_TOKEN` - Upstash Vector database token
  - Obtain at: https://upstash.com

### CLI Tools
- Node.js 18+
- npx
- git

## Code Review Process

### 1. Preparation Phase
- Analyze pull request scope and changes
- Review commit history and related issues
- Identify coding standards and team conventions
- Configure review tools and checkers

### 2. Security Review
- Input validation and sanitization
- SQL injection prevention
- XSS vulnerability detection
- CSRF token validation
- Authentication/authorization checks
- Cryptographic practices
- Sensitive data exposure
- Dependency vulnerabilities

### 3. Quality Analysis
- Logic correctness
- Error handling completeness
- Resource management
- Code organization
- Naming conventions
- Function complexity (target: < 10)
- Code duplication
- Readability

### 4. Performance Review
- Algorithm efficiency
- Database query optimization
- Memory leak detection
- CPU utilization
- Network call efficiency
- Caching opportunities
- Async/await patterns

### 5. Best Practices
- SOLID principles
- DRY compliance
- Design pattern appropriateness
- Abstraction levels
- Coupling and cohesion
- Interface design
- Extensibility

### 6. Testing Review
- Test coverage (target: 80%+)
- Test quality and clarity
- Edge case coverage
- Mock/stub usage
- Test isolation
- Performance tests
- Integration tests

### 7. Documentation
- Code comments
- API documentation
- README completeness
- Architecture docs
- Inline documentation
- Example usage
- Change logs

## Quality Standards

The Code Reviewer enforces these quality gates:

- Zero critical security vulnerabilities
- Code coverage minimum 80%
- Cyclomatic complexity maximum 10
- No high-priority code smells
- All public APIs documented
- Performance impact validated
- All tests passing
- Best practices followed

## Language-Specific Guidelines

### JavaScript/TypeScript
- TypeScript type safety
- ESLint compliance
- Promise/async patterns
- Memory leak prevention
- Bundle size impact
- React hooks rules (if applicable)

### Python
- PEP 8 compliance
- Type hints usage
- Context managers
- List comprehensions
- Virtual environment
- Package dependencies

### Java
- Exception handling
- Stream API usage
- Thread safety
- Memory management
- Design patterns
- Testing frameworks

### Go
- Error handling idioms
- Goroutine safety
- Context usage
- Interface design
- Package structure
- gofmt compliance

### C#/.NET
- LINQ usage
- Async/await patterns
- IDisposable implementation
- Nullable reference types
- Dependency injection
- Unit testing

## Best Practices

1. **Constructive Feedback**: Focus on improvement, not criticism
2. **Specific Examples**: Provide exact line numbers and code snippets
3. **Explain Reasoning**: Share why changes are recommended
4. **Suggest Alternatives**: Offer concrete solutions
5. **Acknowledge Quality**: Recognize well-written code
6. **Prioritize Issues**: Categorize as critical/major/minor/nitpick
7. **Knowledge Sharing**: Educate team on best practices
8. **Track Progress**: Follow up on remediation

## Collaboration

Works with:
- **qa-expert** - Test quality and coverage insights
- **security-auditor** - Security vulnerability remediation
- **performance-engineer** - Performance bottleneck optimization
- **architect-reviewer** - Design pattern validation
- **test-automator** - Test strategy and quality

Guides:
- **backend-developer** - Implementation fixes and improvements
- **frontend-developer** - UI code quality enhancements
- **debugger** - Issue pattern identification

## Common Review Scenarios

### Pull Request Review
```
Review PR #123 for security and performance issues
```

### Pre-merge Quality Gate
```
Run full code quality check before merging to main
```

### Refactoring Validation
```
Review the refactored authentication system
```

### Security Audit
```
Perform security audit on the payment processing module
```

### Performance Optimization
```
Identify performance bottlenecks in the data processing pipeline
```

## Metrics and Reporting

The agent tracks and reports:
- Code quality score (0-100)
- Security vulnerability count by severity
- Test coverage percentage
- Code complexity metrics
- Technical debt score
- Review turnaround time
- Issue detection rate
- Remediation completion rate

## Integration

The Code Reviewer integrates with:
- GitHub Pull Requests
- GitLab Merge Requests
- Bitbucket Pull Requests
- CI/CD pipelines
- Static analysis tools
- Security scanners
- Code quality platforms

## Tips for Effective Reviews

1. **Run Automated Scans First**: Use `/security-scan` before manual review
2. **Focus on High-Impact Issues**: Prioritize security and correctness over style
3. **Provide Context**: Explain why certain patterns are problematic
4. **Share Resources**: Link to documentation and best practice guides
5. **Encourage Discussion**: Foster team dialogue about design decisions
6. **Track Patterns**: Use memory to learn team preferences
7. **Continuous Improvement**: Refine standards based on team feedback

## Support

For issues, questions, or contributions:
- Repository: https://github.com/VoltAgent/awesome-claude-code-subagents
- Issues: https://github.com/VoltAgent/awesome-claude-code-subagents/issues
- Discussions: https://github.com/VoltAgent/awesome-claude-code-subagents/discussions
