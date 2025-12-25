# Vue Expert Agent

A senior Vue specialist with expertise in Vue 3 Composition API and the modern Vue ecosystem. This agent specializes in reactivity mastery, component architecture, performance optimization, and full-stack development with Nuxt 3.

## Overview

The Vue Expert agent helps you build elegant, performant, and maintainable Vue applications by leveraging deep knowledge of Vue 3's Composition API, reactivity system, and ecosystem tools.

## Capabilities

- **Vue 3 Development**: Modern component development with Composition API
- **Reactivity Mastery**: Deep understanding of Vue's reactivity system and optimization
- **Nuxt 3**: Full-stack application development with SSR/SSG
- **State Management**: Pinia store design and implementation
- **Performance**: Bundle optimization, lazy loading, and render optimization
- **TypeScript**: Full type safety across components, composables, and stores
- **Testing**: Comprehensive testing with Vue Test Utils and Vitest
- **Enterprise Patterns**: Micro-frontends, design systems, and component libraries

## Installation

### Prerequisites

- Claude Code CLI installed
- Node.js 18+ for MCP servers
- Git access (optional, for GitHub integration)

### Setup

1. Copy the agent directory to your Claude agents folder:
```bash
cp -r vue-expert ~/.config/claude/agents/
```

2. Set up environment variables (optional):
```bash
export GITHUB_TOKEN="your_github_token_here"
```

3. The agent will automatically load the MCP configuration when invoked.

## Usage

### Invoking the Agent

```bash
# Start the Vue expert agent
claude --agent vue-expert
```

### Slash Commands

#### `/vue-component`
Create a new Vue 3 component with best practices:
```bash
/vue-component
```
Creates a component with:
- Composition API setup
- TypeScript prop validation
- Proper event emitting
- Component testing boilerplate

#### `/vue-composable`
Design and implement a reusable composable:
```bash
/vue-composable
```
Generates:
- Composable function with TypeScript
- Reactive state management
- Lifecycle hooks
- Unit tests

#### `/vue-test`
Generate comprehensive tests:
```bash
/vue-test
```
Creates:
- Component unit tests
- Composable tests
- Integration tests
- Test utilities

#### `/vue-optimize`
Analyze and optimize performance:
```bash
/vue-optimize
```
Analyzes:
- Bundle size and splitting
- Reactivity patterns
- Render performance
- Memory usage

## MCP Servers

The agent uses the following MCP servers:

### Filesystem
Access to read and write files in your project directory.

### GitHub
Repository operations, pull requests, and issue management.
- **Required**: `GITHUB_TOKEN` environment variable

### Context7
Access to up-to-date Vue, Nuxt, and ecosystem documentation.

### Memory
Stores project context, patterns, and development history.

## Configuration

### MCP Configuration

The agent's MCP servers are configured in `mcp-config.json`. You can customize:

- File system access paths
- GitHub organization/repository access
- Memory storage preferences

### Agent Manifest

The `agent-manifest.json` contains metadata about the agent's capabilities, integrations, and requirements.

## Workflow

### 1. Architecture Planning
- Design component hierarchy
- Plan state management approach
- Define routing structure
- Set performance goals

### 2. Implementation
- Create components with Composition API
- Implement composables
- Setup Pinia stores
- Add Vue Router
- Write comprehensive tests

### 3. Optimization
- Optimize reactivity patterns
- Minimize bundle size
- Implement lazy loading
- Profile performance
- Ensure accessibility

## Best Practices

The agent follows Vue community best practices:

- **Composition API First**: Prefer Composition API over Options API
- **TypeScript Strict Mode**: Full type safety
- **Testing**: Minimum 85% code coverage
- **Performance**: Lighthouse score 90+
- **Accessibility**: WCAG 2.1 AA compliance
- **Code Quality**: ESLint + Prettier

## Examples

### Creating a Reactive Dashboard Component

```bash
/vue-component

# Agent will ask for:
# - Component name
# - Props requirements
# - State management needs
# - Testing requirements
```

### Building a Data Fetching Composable

```bash
/vue-composable

# Agent will create:
# - useDataFetch.ts with TypeScript
# - Reactive state management
# - Error handling
# - Unit tests
```

### Optimizing Application Performance

```bash
/vue-optimize

# Agent will analyze:
# - Current bundle size
# - Component render patterns
# - Reactivity efficiency
# - Provide optimization recommendations
```

## Integration with Other Agents

The Vue Expert works seamlessly with:

- **frontend-developer**: UI/UX implementation
- **fullstack-developer**: Nuxt integration
- **typescript-pro**: Type safety enhancement
- **javascript-pro**: Modern JavaScript patterns
- **performance-engineer**: Performance optimization
- **qa-expert**: Testing strategies
- **devops-engineer**: Deployment and CI/CD

## Troubleshooting

### MCP Server Issues

If MCP servers fail to start:
```bash
# Verify Node.js version
node --version  # Should be 18+

# Test MCP servers individually
npx -y @modelcontextprotocol/server-filesystem ${PWD}
```

### GitHub Integration

If GitHub operations fail:
```bash
# Verify token is set
echo $GITHUB_TOKEN

# Test token permissions
gh auth status
```

### Context7 Documentation

If documentation lookup fails:
```bash
# Clear cache and retry
npx -y @anthropic/context7-mcp --clear-cache
```

## Support

For issues or questions:
- Check the [main documentation](../../../README.md)
- Review Vue 3 best practices in CLAUDE.md
- Consult the agent manifest for capabilities

## License

Part of the Claude Code Agent Marketplace.
