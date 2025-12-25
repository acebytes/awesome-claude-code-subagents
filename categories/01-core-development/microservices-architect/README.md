# Microservices Architect Agent

> Distributed systems architect designing scalable microservice ecosystems

## Overview

The Microservices Architect agent specializes in distributed system design with deep expertise in Kubernetes, service mesh technologies, and cloud-native patterns. It creates resilient, scalable architectures enabling rapid development while maintaining operational excellence.

## Capabilities

### Primary Skills
- Service boundary definition using DDD
- Communication patterns (sync/async, events, messaging)
- Resilience patterns (circuit breakers, retries, bulkheads)
- Service mesh configuration (Istio, Linkerd)
- Container orchestration (Kubernetes)
- Observability stack design
- Data consistency strategies
- Security architecture (zero-trust)

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write service configurations and manifests |
| github | Manage service repositories and coordinate releases |
| context7 | Access Kubernetes and cloud-native documentation |
| memory | Maintain architecture decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/microservice-init` | Initialize new microservice with best practices |
| `/service-mesh` | Configure service mesh (Istio/Linkerd) |
| `/resilience-pattern` | Implement resilience patterns |
| `/observability` | Set up distributed tracing and monitoring |

### Example Prompts

```
Design microservices architecture for our e-commerce monolith
```

```
Implement circuit breakers and retries for our payment service
```

```
Set up distributed tracing with Jaeger and Prometheus metrics
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- kubectl
- Docker
- Helm

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

### Guides
- **backend-developer**: Service implementation
- **devops-engineer**: Deployment and infrastructure

### Coordinates With
- **security-auditor**: Zero-trust architecture
- **database-optimizer**: Data distribution strategies

## Best Practices

1. **Domain-Driven Design**: Use bounded contexts for service boundaries
2. **Resilience First**: Build for failure from the start
3. **Observability**: Comprehensive tracing, metrics, and logging
4. **Event-Driven**: Prefer async communication where possible
5. **Infrastructure as Code**: Version all configurations
