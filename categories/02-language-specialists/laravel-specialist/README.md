# Laravel Specialist Agent

Expert Laravel specialist mastering Laravel 10+ with modern PHP practices. Specializes in elegant syntax, Eloquent ORM, queue systems, and enterprise features with focus on building scalable web applications and APIs.

## Overview

This agent is a senior Laravel specialist with deep expertise in Laravel 10+ and modern PHP development. It focuses on Laravel's elegant syntax, powerful ORM, extensive ecosystem, and enterprise features, building applications that are both beautiful in code and powerful in functionality.

## Expertise Areas

### Core Laravel Development
- Laravel 10.x features and best practices
- PHP 8.2+ modern features
- Type-safe development
- PSR compliance and Laravel conventions

### Eloquent ORM
- Model design and relationships
- Query optimization and eager loading
- Scopes, mutators, and accessors
- Model events and transactions
- N+1 query prevention

### API Development
- RESTful API design
- API resources and collections
- Authentication (Sanctum, Passport)
- Rate limiting and versioning
- Comprehensive API testing

### Queue Systems
- Job design and implementation
- Queue drivers and configuration
- Job batching and chaining
- Horizon setup and monitoring
- Performance optimization

### Testing
- Feature and unit tests
- Pest PHP integration
- Database testing strategies
- API and browser testing
- Achieving 85%+ test coverage

### Performance Optimization
- Query optimization
- Cache strategies
- Laravel Octane setup
- Database indexing
- Route and view caching

## Slash Commands

### /laravel-model
Generate or modify Laravel Eloquent models with relationships, scopes, and best practices.

**Example usage:**
```
/laravel-model Create a User model with roles relationship and email verification
```

### /laravel-controller
Create Laravel controllers with resource methods, validation, and proper structure.

**Example usage:**
```
/laravel-controller Build a ProductController with CRUD operations and API resources
```

### /laravel-test
Write comprehensive Laravel tests using Pest or PHPUnit with proper test coverage.

**Example usage:**
```
/laravel-test Write feature tests for the authentication system
```

### /laravel-artisan
Help with Laravel Artisan commands, custom command creation, and task scheduling.

**Example usage:**
```
/laravel-artisan Create a custom command for data import with scheduling
```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File system access for reading and writing Laravel application files
- **github**: GitHub integration for repository operations and collaboration
- **context7**: Documentation and library context for Laravel and PHP ecosystem
- **memory**: Persistent memory for project context and patterns

## Installation

1. Ensure you have the Claude Code CLI installed
2. Clone this repository or copy the agent directory
3. Set up required environment variables:
   ```bash
   export GITHUB_TOKEN="your-github-token"
   ```
4. Navigate to the agent directory and activate it in Claude Code

## Usage Examples

### Building a New Laravel Application
```
I need to build a multi-tenant SaaS application with:
- User authentication with roles
- Subscription management
- API for mobile apps
- Real-time notifications
- Background job processing

Use Laravel best practices and achieve high test coverage.
```

### Optimizing Existing Code
```
Review my Laravel application's performance. The API endpoints are slow and I'm seeing N+1 queries. Help me optimize the Eloquent queries and implement proper caching.
```

### API Development
```
/laravel-controller Create a RESTful API controller for managing blog posts with:
- Pagination
- Filtering and sorting
- API resources
- Rate limiting
- Comprehensive validation
```

### Queue Implementation
```
I need to implement a job queue for processing CSV imports. The jobs should:
- Handle large files in batches
- Retry on failure
- Send notifications on completion
- Be monitored via Horizon
```

## Best Practices

This agent follows and enforces:

- **Laravel Standards**: Official Laravel conventions and patterns
- **PSR Compliance**: PSR-1, PSR-12 coding standards
- **Type Safety**: Strict typing with PHP 8.2+ features
- **SOLID Principles**: Clean, maintainable architecture
- **Test Coverage**: Minimum 85% test coverage
- **Security**: Laravel security best practices
- **Performance**: Optimized queries and caching strategies
- **Documentation**: Comprehensive PHPDoc and API documentation

## Integration with Other Agents

Works seamlessly with:
- **php-pro**: For advanced PHP optimization
- **fullstack-developer**: For full-stack Laravel applications
- **database-optimizer**: For complex database optimizations
- **api-designer**: For API architecture and design
- **devops-engineer**: For deployment and infrastructure
- **security-auditor**: For security reviews and hardening
- **frontend-developer**: For Livewire/Inertia.js integration

## Target Framework Versions

- Laravel 10.x and above
- PHP 8.2 and above

## Package Ecosystem Support

Expert knowledge of:
- Laravel Sanctum (API authentication)
- Laravel Passport (OAuth)
- Laravel Echo (WebSockets)
- Laravel Horizon (Queue monitoring)
- Laravel Nova (Admin panel)
- Laravel Livewire (Full-stack framework)
- Laravel Inertia (Modern monolith)
- Laravel Octane (Performance)

## Output Expectations

When working with this agent, expect:

- **Elegant Code**: Beautiful, readable Laravel code
- **Comprehensive Tests**: High test coverage with meaningful assertions
- **Proper Documentation**: Clear PHPDoc and inline comments
- **Performance Focus**: Optimized queries and caching
- **Security First**: Following Laravel security best practices
- **Type Safety**: Strict typing throughout
- **PSR Compliance**: Following PHP standards

## Contributing

To improve this agent:
1. Update CLAUDE.md for instruction changes
2. Modify agent-manifest.json for metadata updates
3. Adjust mcp-config.json for MCP server configuration
4. Update README.md for documentation improvements

## License

Part of the Claude Code Agent Marketplace.
