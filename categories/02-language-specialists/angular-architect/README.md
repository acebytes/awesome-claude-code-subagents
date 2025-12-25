# Angular Architect Agent

Expert Angular architect mastering Angular 15+ with enterprise patterns. Specializes in RxJS, NgRx state management, micro-frontend architecture, and performance optimization with focus on building scalable enterprise applications.

## Overview

The Angular Architect agent is a senior-level specialist in modern Angular development, designed to help you build enterprise-grade applications with best practices, optimal performance, and maintainable architecture. This agent excels at complex Angular challenges including reactive programming, state management, micro-frontends, and performance optimization.

## Capabilities

- **Angular 15+ Development**: Modern Angular features including standalone components, signals, and advanced patterns
- **RxJS Mastery**: Complex observable patterns, custom operators, memory management, and marble testing
- **NgRx State Management**: Store design, effects, selectors optimization, and entity management
- **Micro-Frontend Architecture**: Module federation, shell architecture, and remote component loading
- **Performance Optimization**: Bundle analysis, lazy loading, OnPush strategy, and runtime optimization
- **Enterprise Testing**: Unit, integration, E2E, marble testing with >85% coverage targets
- **Nx Monorepo**: Workspace management, library architecture, and build optimization
- **Signals Adoption**: Migration strategies and modern reactive patterns

## Installation

1. Copy the `angular-architect` directory to your Claude Code agents location
2. Ensure you have the required MCP servers configured (see MCP Configuration below)
3. Set up environment variables for GitHub integration (if needed)

## MCP Configuration

This agent uses the following MCP servers:

### Filesystem
Provides access to read and write files in your Angular project.

```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "${PWD}"]
}
```

### GitHub
Enables GitHub operations for repository management and collaboration.

```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-github"],
  "env": {
    "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_TOKEN}"
  }
}
```

**Setup**: Set your `GITHUB_TOKEN` environment variable with a personal access token.

### Context7
Provides access to up-to-date Angular, RxJS, and NgRx documentation.

```json
{
  "command": "npx",
  "args": ["-y", "@upstash/context7-mcp"]
}
```

### Memory
Enables conversation memory for context retention across sessions.

```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-memory"]
}
```

## Slash Commands

### `/angular-component`
Create a new Angular component following best practices:
- OnPush change detection strategy
- Strict TypeScript typing
- Proper lifecycle hooks
- WCAG accessibility attributes
- Comprehensive unit tests
- Component documentation

**Example:**
```
/angular-component user-profile with avatar, bio, and settings
```

### `/angular-service`
Generate an Angular service with enterprise patterns:
- Dependency injection setup
- RxJS observable patterns
- Comprehensive error handling
- Full testing coverage
- Interface definitions
- Service documentation

**Example:**
```
/angular-service user-api for fetching and updating user data
```

### `/angular-test`
Create comprehensive test suites for Angular code:
- Component unit tests
- Service integration tests
- RxJS marble tests
- Cypress E2E tests
- Test utilities and mocks
- Coverage reports

**Example:**
```
/angular-test for the UserProfileComponent
```

### `/angular-optimize`
Analyze and optimize Angular application performance:
- Bundle size analysis and reduction
- Lazy loading implementation
- OnPush change detection
- TrackBy functions for ngFor
- Virtual scrolling for large lists
- Preloading strategies
- Build configuration optimization

**Example:**
```
/angular-optimize the dashboard module
```

## Usage Examples

### Creating a New Feature Module

```typescript
// The agent will help create a complete feature module with:
// - Module structure with lazy loading
// - Smart and dumb components
// - Service layer with RxJS
// - NgRx state management (if needed)
// - Routing configuration
// - Comprehensive tests

"Create a products feature module with list, detail, and create views"
```

### Implementing NgRx State Management

```typescript
// The agent will implement:
// - Actions with proper typing
// - Reducers with immutable updates
// - Effects for async operations
// - Selectors with memoization
// - Entity adapters
// - DevTools integration

"Set up NgRx state management for user authentication"
```

### Performance Optimization

```typescript
// The agent will:
// - Analyze bundle size
// - Implement code splitting
// - Add lazy loading
// - Optimize change detection
// - Configure preloading
// - Set up performance budgets

"Optimize the application for faster initial load"
```

### Micro-Frontend Setup

```typescript
// The agent will configure:
// - Module federation
// - Shell application
// - Remote modules
// - Shared dependencies
// - Communication patterns
// - Build configuration

"Set up micro-frontend architecture with module federation"
```

## Best Practices

The Angular Architect agent follows these best practices:

- **Angular 15+ Features**: Utilizes latest Angular capabilities including standalone components and signals
- **Strict Mode**: TypeScript strict mode enabled for type safety
- **OnPush Strategy**: Default change detection strategy for performance
- **Bundle Budgets**: Configured and enforced size limits
- **Test Coverage**: Maintains >85% test coverage across the application
- **Accessibility**: WCAG AA compliance with proper ARIA attributes
- **Documentation**: Comprehensive inline and architectural documentation
- **Performance First**: Optimization at every level of the stack

## Architecture Patterns

### Module Structure
- **Core Module**: Singleton services and app-wide components
- **Shared Module**: Reusable components, directives, and pipes
- **Feature Modules**: Business domain modules with lazy loading
- **Barrel Exports**: Clean import paths with index.ts files

### Component Architecture
- **Smart Components**: Container components managing state and logic
- **Dumb Components**: Presentational components with inputs/outputs
- **OnPush Strategy**: Optimized change detection
- **Content Projection**: Flexible component composition

### State Management
- **NgRx Store**: Centralized state management
- **Effects**: Side effect handling
- **Selectors**: Memoized state derivation
- **Entity Adapters**: Normalized state structure

## Performance Targets

- Initial load: < 3 seconds
- Route transitions: < 200ms
- Bundle size: Optimized and tracked
- Test coverage: > 85%
- Lighthouse score: 95+
- Memory efficiency: No leaks
- CPU optimization: Minimal main thread blocking

## Integration with Other Agents

The Angular Architect works seamlessly with:

- **Frontend Developer**: UI patterns and component design
- **TypeScript Pro**: Advanced TypeScript patterns
- **Performance Engineer**: Application optimization
- **QA Expert**: Testing strategies and automation
- **DevOps Engineer**: CI/CD and deployment
- **Security Auditor**: Security best practices

## Requirements

- **Angular**: >= 15.0.0
- **TypeScript**: >= 4.8.0
- **Node.js**: >= 18.0.0
- **npm/yarn/pnpm**: Latest stable version

## Troubleshooting

### Agent Not Responding
- Verify all MCP servers are properly configured
- Check that environment variables are set (especially `GITHUB_TOKEN`)
- Ensure Angular project structure is valid

### Performance Issues
- Review bundle budgets in angular.json
- Check for common performance anti-patterns
- Use `/angular-optimize` command for analysis

### Test Coverage Low
- Use `/angular-test` to generate comprehensive tests
- Review test configuration in angular.json
- Check karma/jest setup

## Contributing

To enhance this agent:

1. Update `CLAUDE.md` with new instructions or patterns
2. Add new slash commands in both `CLAUDE.md` and `agent-manifest.json`
3. Update `README.md` with usage examples
4. Test with real Angular projects
5. Submit feedback and improvements

## License

MIT License - Part of the Claude Code Agent Marketplace

## Resources

- [Angular Official Documentation](https://angular.io/)
- [RxJS Official Guide](https://rxjs.dev/)
- [NgRx Official Documentation](https://ngrx.io/)
- [Angular Style Guide](https://angular.io/guide/styleguide)
- [Nx Documentation](https://nx.dev/)

---

**Note**: This agent is designed to work with Angular 15+ and follows the latest Angular best practices. For older Angular versions, some patterns may need adjustment.
