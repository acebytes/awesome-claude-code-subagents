# Backend Developer Agent

> Senior backend engineer specializing in scalable API development and microservices architecture

## Overview

The Backend Developer agent specializes in server-side applications with deep expertise in Node.js, Python, and Go. It builds robust, secure, and performant backend systems focusing on scalability, security, and maintainability.

## Capabilities

### Primary Skills
- RESTful API development with proper HTTP semantics
- Database schema design and query optimization
- Authentication and authorization implementation
- Microservices architecture patterns
- Message queue integration (Redis, RabbitMQ, Kafka)
- Caching strategies for performance
- Docker containerization
- CI/CD pipeline configuration

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write source code and configuration files |
| github | Manage repositories, PRs, and code reviews |
| context7 | Access up-to-date backend framework documentation |
| postgres | Direct PostgreSQL database operations |
| memory | Maintain architecture decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/backend-init` | Initialize new backend service with best practices |
| `/api-endpoint` | Create new API endpoint with full implementation |
| `/db-migrate` | Generate database migration scripts |
| `/backend-test` | Generate comprehensive test suite |

### Example Prompts

```
Build a user authentication API with JWT and refresh tokens
```

```
Create a microservice for handling order processing with Kafka integration
```

```
Implement a caching layer for our product catalog API
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

### Works With
- **api-designer**: Receives API specifications
- **database-optimizer**: Database query optimization
- **devops-engineer**: Deployment and infrastructure
- **security-auditor**: Security reviews

### Provides To
- **frontend-developer**: API endpoints
- **mobile-developer**: Mobile API support

## Best Practices

1. **Security First**: Validate all inputs, use parameterized queries
2. **Performance**: Profile queries, implement caching layers
3. **Observability**: Include logging, metrics, and tracing
4. **Testing**: Maintain 80%+ test coverage
5. **Documentation**: Keep OpenAPI specs up-to-date
