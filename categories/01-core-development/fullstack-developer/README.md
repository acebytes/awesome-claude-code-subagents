# Fullstack Developer Agent

> End-to-end feature owner with expertise across the entire stack

## Overview

The Fullstack Developer agent specializes in complete feature development with expertise across backend and frontend technologies. It delivers cohesive, end-to-end solutions from database to UI with focus on seamless integration and optimal user experience.

## Capabilities

### Primary Skills
- End-to-end feature development
- Type-safe API contracts with shared types
- Database schema design aligned with frontend needs
- Authentication flows spanning all layers
- Real-time synchronization with WebSockets
- Monorepo and shared code management
- Full-stack testing strategies
- Deployment pipeline configuration

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write code across backend and frontend |
| github | Manage full-stack repositories and coordinate changes |
| context7 | Access React, Node.js, Next.js documentation |
| postgres | Direct database operations for schema design |
| memory | Maintain architecture decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/fullstack-init` | Initialize fullstack project with monorepo structure |
| `/feature` | Generate end-to-end feature across all layers |
| `/type-sync` | Synchronize types between backend and frontend |
| `/e2e-test` | Generate end-to-end test suite |

### Example Prompts

```
Build a complete user management system with authentication, profiles, and admin panel
```

```
Implement shopping cart functionality with real-time inventory updates
```

```
Create a notification system with WebSocket delivery and database persistence
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations
- `POSTGRES_URL` - Required for direct database operations

### CLI Tools
- Node.js 18+
- Docker
- npx

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
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "POSTGRES_CONNECTION_STRING": "${POSTGRES_URL}"
      }
    }
  }
}
```

## Collaboration Network

### Coordinates With
- **database-optimizer**: Schema optimization
- **api-designer**: API contract design
- **ui-designer**: Component specifications
- **devops-engineer**: Deployment configuration

### Delegates To
- **backend-developer**: Complex backend logic
- **frontend-developer**: Complex UI components

## Best Practices

1. **Type Safety**: Share types between frontend and backend
2. **Monorepo Structure**: Keep related code together
3. **E2E Testing**: Test complete user flows
4. **Performance**: Optimize at each layer
5. **Documentation**: Document integration points
