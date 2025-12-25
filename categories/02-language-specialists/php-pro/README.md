# PHP Pro Agent

Expert PHP developer specializing in modern PHP 8.3+ with strong typing, async programming, and enterprise frameworks. Masters Laravel, Symfony, and modern PHP patterns with emphasis on performance and clean architecture.

## Overview

The PHP Pro agent is designed to help you build enterprise-grade PHP applications using the latest PHP 8.3+ features, modern frameworks like Laravel and Symfony, and industry best practices. This agent emphasizes type safety, PSR standards compliance, async programming, and performance optimization.

## Features

- **Modern PHP 8.3+ Development**: Leverages readonly properties, enums, union types, attributes, and other cutting-edge features
- **Framework Expertise**: Deep knowledge of Laravel and Symfony architectures and patterns
- **Type Safety**: Enforces strict typing, PHPStan level 9 compliance, and comprehensive type declarations
- **Async Programming**: Implements ReactPHP, Swoole, and Fiber patterns for concurrent processing
- **Performance Optimization**: OpCache tuning, query optimization, caching strategies, and profiling
- **Security First**: Input validation, SQL injection prevention, authentication best practices
- **Testing Excellence**: PHPUnit, integration testing, mutation testing, 80%+ coverage targets
- **API Development**: RESTful APIs, GraphQL, authentication (OAuth/JWT), OpenAPI documentation

## Installation

1. Copy the `php-pro` directory to your Claude Code agents folder
2. Ensure the MCP servers are configured in your environment
3. Set the `GITHUB_TOKEN` environment variable for GitHub integration

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File system operations for reading and writing code
- **github**: GitHub integration for repository operations
- **context7**: Access to PHP framework and library documentation
- **memory**: Persistent memory for project context and preferences

## Slash Commands

### /php-analyze

Comprehensive codebase analysis:
- Type coverage and strict typing usage
- PSR-12 coding standards compliance
- Framework patterns and best practices
- Security vulnerability scanning
- Performance bottleneck identification
- Code quality metrics (PHPStan level)
- Dependency health check

**Usage:**
```
/php-analyze
```

### /php-test

Execute comprehensive testing suite:
- Run PHPUnit test suite with configuration
- Generate code coverage reports
- Perform PHPStan static analysis
- Run mutation testing for test quality
- Verify integration and feature tests
- Display coverage statistics

**Usage:**
```
/php-test
```

### /php-security

Security audit and vulnerability assessment:
- Scan for common PHP vulnerabilities
- Review authentication and authorization
- Check input validation and sanitization
- Audit Composer dependencies
- Review session handling security
- Check file upload safety
- Analyze SQL injection risks
- Review CSRF protection

**Usage:**
```
/php-security
```

### /php-optimize

Performance optimization analysis:
- Profile application performance
- Analyze and optimize database queries
- Review and enhance caching strategies
- Optimize autoloading configuration
- Check and tune OpCache settings
- Analyze memory usage patterns
- Review lazy loading implementation
- Identify N+1 query problems

**Usage:**
```
/php-optimize
```

## Usage Examples

### Starting a New Laravel Project

```
I need to create a new Laravel API project with:
- PHP 8.3 strict typing
- JWT authentication
- RESTful API for user management
- Redis caching
- PHPStan level 9 compliance
```

The agent will:
1. Analyze requirements and project structure
2. Set up Laravel with proper configuration
3. Implement type-safe controllers and services
4. Create repository patterns for data access
5. Set up JWT authentication
6. Implement caching strategies
7. Write comprehensive tests
8. Configure PHPStan for static analysis

### Optimizing Existing Symfony Application

```
/php-optimize

Please analyze my Symfony application for performance issues.
Focus on database queries and caching.
```

The agent will:
1. Profile the application performance
2. Identify slow database queries
3. Suggest eager loading strategies
4. Recommend caching improvements
5. Analyze OpCache configuration
6. Provide specific optimization recommendations

### Security Audit

```
/php-security

Audit my Laravel application for security vulnerabilities,
especially authentication and API endpoints.
```

The agent will:
1. Scan for common vulnerabilities
2. Review authentication implementation
3. Check API endpoint security
4. Verify input validation
5. Audit dependencies
6. Provide detailed security report

## Development Workflow

The PHP Pro agent follows a systematic development approach:

### 1. Architecture Analysis
- Review project structure and framework setup
- Analyze dependencies and composer.json
- Evaluate database schema and migrations
- Assess current code quality and patterns

### 2. Implementation
- Use strict types and comprehensive type declarations
- Design service classes with dependency injection
- Implement repository patterns for data access
- Create value objects for domain logic
- Apply SOLID principles
- Write comprehensive PHPDoc comments

### 3. Quality Assurance
- Ensure PHPStan level 9 compliance
- Verify PSR-12 coding standards
- Achieve 80%+ test coverage
- Pass security scans
- Validate performance benchmarks
- Complete documentation

## Best Practices

The agent enforces and promotes:

- **Type Safety**: Strict types, return type declarations, property type hints
- **PSR Standards**: PSR-12 coding style, PSR-4 autoloading
- **Testing**: PHPUnit, integration tests, mutation testing
- **Security**: Input validation, prepared statements, CSRF protection
- **Performance**: Query optimization, caching, lazy loading
- **Documentation**: PHPDoc blocks, OpenAPI specs
- **Modern Features**: Readonly classes, enums, attributes, match expressions

## Integration with Other Agents

The PHP Pro agent works seamlessly with:

- **api-designer**: Share API specifications and endpoint design
- **frontend-developer**: Provide API documentation and endpoints
- **mysql-expert**: Collaborate on query optimization
- **devops-engineer**: Support deployment and infrastructure
- **docker-specialist**: Configure containerization
- **security-auditor**: Address security vulnerabilities
- **redis-expert**: Implement caching strategies

## Configuration

### Customizing Development Standards

You can customize the agent's behavior by modifying the CLAUDE.md file:

- Adjust PHPStan level requirements
- Modify test coverage thresholds
- Add custom PSR rules
- Configure framework-specific patterns

### Environment Variables

Required environment variables:
- `GITHUB_TOKEN`: For GitHub integration (optional)

## Troubleshooting

### PHPStan Analysis Fails

Ensure you have PHPStan installed:
```bash
composer require --dev phpstan/phpstan
```

### Test Coverage Too Low

The agent targets 80%+ coverage. Use:
```
/php-test
```
to identify untested code paths.

### Performance Issues

Run optimization analysis:
```
/php-optimize
```

## Requirements

- PHP 8.3 or higher
- Composer package manager
- PHPUnit for testing
- PHPStan for static analysis
- Laravel or Symfony framework (optional)

## Contributing

Improvements and suggestions are welcome. Consider:
- Adding new slash commands
- Enhancing analysis capabilities
- Updating for new PHP versions
- Adding framework-specific patterns

## License

Part of the Claude Code Agent Marketplace.

## Support

For issues or questions:
1. Check the CLAUDE.md file for detailed agent instructions
2. Review the agent-manifest.json for capabilities
3. Consult the MCP server documentation
4. Refer to PHP 8.3+ documentation for language features
