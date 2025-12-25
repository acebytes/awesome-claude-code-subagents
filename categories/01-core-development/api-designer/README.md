# API Designer Agent

> API architecture expert designing scalable, developer-friendly interfaces

## Overview

The API Designer agent specializes in creating intuitive, scalable API architectures with expertise in REST and GraphQL design patterns. It focuses on delivering well-documented, consistent APIs that developers love to use while ensuring performance and maintainability.

## Capabilities

### Primary Skills
- REST API design following RESTful principles
- GraphQL schema design and federation architecture
- OpenAPI 3.1 specification development
- API versioning and deprecation strategies
- Authentication pattern design (OAuth 2.0, JWT, API keys)
- Rate limiting and throttling configuration
- Pagination and filtering design patterns
- Webhook specification development

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write API specifications and OpenAPI documents |
| github | Manage API documentation repositories and review PRs |
| context7 | Access up-to-date REST/GraphQL framework documentation |
| fetch | Test API endpoints and validate external integrations |
| memory | Maintain context about API design decisions |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/api-spec` | Generate OpenAPI 3.1 specification from requirements |
| `/graphql-schema` | Design GraphQL schema with types and resolvers |
| `/api-review` | Review existing API design for best practices |
| `/api-version` | Plan API versioning and migration strategy |

### Example Prompts

```
Design a REST API for a user management system with authentication
```

```
Create a GraphQL schema for an e-commerce product catalog with cart functionality
```

```
Review our current API design and suggest improvements for developer experience
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- Node.js 18+
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
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

## Collaboration Network

### Works With
- **backend-developer**: Implements designed APIs
- **frontend-developer**: Consumes API contracts
- **security-auditor**: Reviews authentication patterns
- **mobile-developer**: Mobile-specific API optimizations
- **documentation-engineer**: API documentation generation

### Receives Input From
- **product-manager**: Business requirements
- **fullstack-developer**: End-to-end integration needs

## Best Practices

1. **Design First**: Always start with API specification before implementation
2. **Consistency**: Maintain consistent naming conventions across all endpoints
3. **Documentation**: Include comprehensive examples for all operations
4. **Versioning**: Plan for API evolution from the start
5. **Security**: Design authentication and authorization into every endpoint
