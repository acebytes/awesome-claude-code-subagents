# GraphQL Architect Agent

> GraphQL schema architect designing efficient, scalable API graphs

## Overview

The GraphQL Architect agent specializes in schema design and distributed graph architectures with deep expertise in Apollo Federation, subscriptions, and performance optimization. It creates efficient, type-safe API graphs that scale across teams and services.

## Capabilities

### Primary Skills
- GraphQL schema design and modeling
- Apollo Federation architecture
- Subscription implementation for real-time data
- Query optimization and complexity analysis
- DataLoader pattern implementation
- Schema versioning and evolution
- Type system mastery
- Client-side integration patterns

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write schema files and resolvers |
| github | Manage schema repositories and review PRs |
| context7 | Access Apollo and GraphQL documentation |
| memory | Maintain schema design decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/graphql-schema` | Generate GraphQL schema from requirements |
| `/graphql-federate` | Create federated subgraph architecture |
| `/graphql-resolver` | Implement resolvers with DataLoader |
| `/graphql-subscription` | Set up real-time subscriptions |

### Example Prompts

```
Create a federated GraphQL architecture for an e-commerce platform
```

```
Implement real-time order status subscriptions with WebSocket
```

```
Optimize our GraphQL queries and add complexity limiting
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- Node.js 18+
- npx

### Runtime Dependencies
- @apollo/server
- graphql

## Configuration

Add to your Claude Code MCP settings:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "${PWD}"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_TOKEN}"
      }
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

## Collaboration Network

### Works With
- **backend-developer**: Resolver implementation
- **microservices-architect**: Service boundaries
- **api-designer**: API contract design

### Provides To
- **frontend-developer**: Query fragments
- **mobile-developer**: Client integration

## Best Practices

1. **Schema First**: Design schema before implementation
2. **Federation**: Use for distributed teams and services
3. **DataLoader**: Always use for relationship resolution
4. **Complexity**: Implement query complexity limits
5. **Evolution**: Plan for schema changes from the start
