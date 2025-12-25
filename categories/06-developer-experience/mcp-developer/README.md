# MCP Developer Agent

Expert MCP developer specializing in Model Context Protocol server and client development with production-ready integrations.

## Overview

The MCP Developer agent is a senior-level specialist in building Model Context Protocol (MCP) servers and clients that connect AI systems with external tools and data sources. This agent provides comprehensive expertise in protocol implementation, SDK usage, integration patterns, and production deployment with a strong emphasis on security, performance, and developer experience.

## What is MCP?

The Model Context Protocol (MCP) is an open protocol that standardizes how AI applications connect to external data sources and tools. It enables:

- **AI systems** (like Claude) to access external resources through a unified interface
- **Developers** to build reusable integrations that work across different AI applications
- **Organizations** to securely expose their data and tools to AI assistants

MCP uses JSON-RPC 2.0 for message exchange and supports multiple transport mechanisms (stdio, HTTP, Server-Sent Events).

## Capabilities

### Core Expertise

- **Protocol Implementation**: JSON-RPC 2.0 compliant MCP servers and clients
- **Server Development**: Build production-ready MCP servers with tools and resources
- **Client Development**: Implement robust MCP clients with error handling
- **SDK Mastery**: TypeScript and Python MCP SDK implementation
- **Security**: Authentication, authorization, input validation, rate limiting
- **Performance**: Optimization for low latency and high throughput
- **Testing**: Comprehensive protocol compliance and integration testing
- **Deployment**: Container configuration, monitoring, and production readiness

### Supported Languages & Frameworks

- **Languages**: TypeScript, Python, JavaScript
- **MCP SDKs**: @modelcontextprotocol/sdk (TypeScript/JavaScript), mcp (Python)
- **Validation**: Zod (TypeScript), Pydantic (Python)
- **Platforms**: Node.js 18+, Python 3.10+, Docker, Claude Desktop

## Prerequisites

### Required Tools

1. **Node.js 18+**: For TypeScript/JavaScript development
   ```bash
   node --version  # Should be 18.0.0 or higher
   ```

2. **npm/npx**: For package management and running MCP servers
   ```bash
   npm --version
   ```

3. **git**: For version control and accessing repositories
   ```bash
   git --version
   ```

4. **Python 3.10+**: For Python MCP development (optional)
   ```bash
   python --version  # Should be 3.10.0 or higher
   ```

### Required API Keys

1. **GitHub Personal Access Token** (Required)
   - Used by the `github` MCP server to access repositories
   - Create at: https://github.com/settings/tokens
   - Scopes needed: `repo` (for private repos) or `public_repo` (for public repos only)
   - Set environment variable:
     ```bash
     export GITHUB_PERSONAL_ACCESS_TOKEN='ghp_your_token_here'
     ```

2. **Context7 API Key** (Optional)
   - Used by the `context7` MCP server for protocol documentation queries
   - Sign up at: https://context7.ai
   - Set environment variable:
     ```bash
     export CONTEXT7_API_KEY='your_context7_key_here'
     ```

### MCP Servers

This agent uses the following MCP servers:

| Server | Package | Purpose | Required |
|--------|---------|---------|----------|
| **filesystem** | @modelcontextprotocol/server-filesystem | Read/write MCP server code | Yes |
| **github** | @modelcontextprotocol/server-github | Access MCP repositories | Yes |
| **context7** | @uplink-online/mcp-server-context7 | Query protocol docs | No |
| **fetch** | @modelcontextprotocol/server-fetch | Test HTTP endpoints | Yes |

## Setup Instructions

### 1. Install Node.js

Download and install Node.js 18+ from https://nodejs.org/

### 2. Configure Environment Variables

Create a `.env` file or add to your shell profile:

```bash
# Required
export GITHUB_PERSONAL_ACCESS_TOKEN='ghp_your_token_here'

# Optional (for enhanced documentation access)
export CONTEXT7_API_KEY='your_context7_key_here'
```

### 3. Test MCP Server Connections

Use the MCP Inspector to verify your servers are working:

```bash
npx -y @modelcontextprotocol/inspector
```

This will start an interactive inspector where you can test connecting to MCP servers.

### 4. Configure Claude Desktop (Optional)

To use these MCP servers with Claude Desktop, add the configuration to your Claude Desktop config file:

**macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`

**Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/your/project"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_your_token_here"
      }
    },
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

## Usage Examples

### Example 1: Initialize a New MCP Server

Create a new TypeScript MCP server with best practices scaffolding:

```
/mcp-init typescript weather-server
```

The agent will:
1. Create project directory structure
2. Initialize package.json with MCP SDK dependencies
3. Create TypeScript configuration
4. Generate server scaffold with example tools
5. Add testing framework setup
6. Create comprehensive README

### Example 2: Add a Tool to Existing Server

Add a new tool function to your MCP server:

```
/mcp-tool search-database "Search the database for user records"
```

The agent will:
1. Read your existing server implementation
2. Define the tool schema with input validation
3. Implement the tool handler function
4. Register the tool in server handlers
5. Add unit tests for the new tool
6. Update documentation

### Example 3: Add a Resource Endpoint

Expose data through a resource endpoint:

```
/mcp-resource user-profile "user://{userId}/profile"
```

The agent will:
1. Define the resource schema
2. Implement the resource handler
3. Add URI template support
4. Implement pagination if needed
5. Add caching layer
6. Write resource tests

### Example 4: Test MCP Server

Test your MCP server implementation:

```
/mcp-test ./src/index.ts
```

The agent will:
1. Start the server in test mode
2. Connect a test client
3. List available tools and resources
4. Test each tool with sample inputs
5. Validate protocol compliance
6. Report test results with coverage

### Example 5: Full Server Implementation

Create a complete MCP server from scratch:

```
Create a new MCP server that exposes my PostgreSQL database as resources
and provides query tools. Include:
- Connection pooling
- Input validation and SQL injection prevention
- Rate limiting (100 queries/minute)
- Comprehensive error handling
- Full test coverage
```

The agent will:
1. Query for database requirements
2. Create TypeScript MCP server project
3. Implement database connection with pooling
4. Create resource endpoints for tables
5. Add query tools with validation
6. Implement security controls
7. Add rate limiting middleware
8. Write comprehensive tests
9. Create Docker configuration
10. Generate complete documentation

### Example 6: Debug and Fix Issues

Debug protocol compliance issues:

```
My MCP server tools are failing with validation errors. The client
receives error code -32602 (Invalid params). Help me debug and fix this.
```

The agent will:
1. Read your server implementation
2. Review tool schemas and handlers
3. Test with protocol compliance suite
4. Identify validation issues
5. Fix schema definitions
6. Update error handling
7. Verify fixes with tests

## Slash Commands

### /mcp-init

Initialize a new MCP server project with best practices.

**Syntax**: `/mcp-init <language> <server-name>`

**Parameters**:
- `language`: `typescript` or `python`
- `server-name`: Name for your new server

**Example**:
```
/mcp-init typescript weather-api-server
```

### /mcp-tool

Add a new tool function to an existing MCP server.

**Syntax**: `/mcp-tool <tool-name> <description>`

**Parameters**:
- `tool-name`: Name of the tool (kebab-case)
- `description`: Brief description of what the tool does

**Example**:
```
/mcp-tool send-email "Send an email via SendGrid API"
```

### /mcp-resource

Add a new resource endpoint to expose data sources.

**Syntax**: `/mcp-resource <resource-name> <uri-template>`

**Parameters**:
- `resource-name`: Name of the resource
- `uri-template`: URI template with optional parameters

**Example**:
```
/mcp-resource user-data "user://{userId}/profile"
```

### /mcp-test

Test an MCP server implementation locally.

**Syntax**: `/mcp-test [server-path]`

**Parameters**:
- `server-path`: Path to server entry point (optional, defaults to current directory)

**Example**:
```
/mcp-test ./build/index.js
```

## Development Workflow

### Phase 1: Protocol Analysis

The agent starts by understanding your requirements:

- What data sources need to be exposed?
- What actions should be available as tools?
- Who will use this MCP server (client applications)?
- What transport mechanism is needed (stdio, HTTP, SSE)?
- What security requirements exist?
- What performance targets must be met?

### Phase 2: Implementation

The agent builds your MCP solution:

1. **Setup**: Create project structure with MCP SDK
2. **Protocol Handlers**: Implement initialize, list, and call handlers
3. **Resources**: Create endpoints to expose data
4. **Tools**: Build functions to enable actions
5. **Security**: Add validation, authentication, rate limiting
6. **Error Handling**: Implement comprehensive error handling
7. **Logging**: Add structured logging and monitoring
8. **Testing**: Write unit and integration tests

### Phase 3: Production Excellence

The agent ensures production readiness:

- Protocol compliance testing
- Security audit and penetration testing
- Performance optimization (<100ms p95 latency)
- Complete documentation (API docs, examples)
- Monitoring and alerting setup
- Deployment configuration (Docker, K8s)
- Scaling strategy planning

## Best Practices

The MCP Developer agent follows these principles:

1. **Protocol Compliance**: Strict adherence to JSON-RPC 2.0 and MCP specifications
2. **Security First**: Input validation, output sanitization, authentication from day 1
3. **Developer Experience**: Clear documentation, helpful error messages, examples
4. **Performance**: Optimize for low latency and high throughput
5. **Reliability**: Comprehensive error handling and graceful degradation
6. **Observability**: Structured logging, metrics, and monitoring
7. **Scalability**: Design for growth from the start
8. **Testing**: >90% test coverage with unit, integration, and compliance tests

## Common Use Cases

### Database Integration

Create MCP servers that expose databases as resources:
- List tables as resources
- Provide query tools with SQL injection prevention
- Implement connection pooling
- Add caching for frequently accessed data

### API Wrapper

Wrap external APIs as MCP tools:
- OAuth/API key authentication
- Rate limiting and retry logic
- Request/response transformation
- Error handling and logging

### File System Access

Provide secure file operations:
- Read/write files with path validation
- Directory listing and search
- File upload/download
- Access control and sandboxing

### Authentication Provider

Integrate authentication systems:
- OAuth 2.0 flow implementation
- JWT token validation
- API key management
- Session handling

## Troubleshooting

### Server Not Starting

**Issue**: MCP server fails to start

**Solutions**:
1. Check Node.js version: `node --version` (must be 18+)
2. Verify dependencies are installed: `npm install`
3. Check for syntax errors: `npm run build`
4. Review error logs for specific issues

### Protocol Compliance Errors

**Issue**: Error code -32600, -32601, -32602

**Solutions**:
1. Validate message format (must be valid JSON-RPC 2.0)
2. Check method names match specification
3. Verify parameters match schema definitions
4. Use MCP Inspector to test: `npx @modelcontextprotocol/inspector`

### Authentication Failures

**Issue**: GitHub or Context7 server not connecting

**Solutions**:
1. Verify environment variables are set
2. Check token has correct permissions
3. Test token validity manually
4. Review server logs for specific error

### Performance Issues

**Issue**: High latency or timeout errors

**Solutions**:
1. Implement connection pooling
2. Add caching layer (Redis, in-memory)
3. Use batch processing for multiple requests
4. Profile code to identify bottlenecks
5. Consider horizontal scaling

## Resources

### Official Documentation

- [MCP Specification](https://spec.modelcontextprotocol.io/)
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk)
- [JSON-RPC 2.0 Specification](https://www.jsonrpc.org/specification)

### Community Resources

- [Awesome MCP](https://github.com/modelcontextprotocol/awesome-mcp)
- [MCP Servers Repository](https://github.com/modelcontextprotocol/servers)
- [Community Discord](https://discord.gg/modelcontextprotocol)

### Tools

- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) - Test and debug MCP servers
- [Claude Desktop](https://claude.ai/download) - Use MCP servers with Claude

## Agent Collaboration

The MCP Developer agent collaborates with:

- **api-designer**: Design external API integrations for MCP tools
- **backend-developer**: Implement server infrastructure
- **security-engineer**: Implement security controls and auditing
- **performance-engineer**: Optimize server performance
- **devops-engineer**: Deploy and scale MCP servers
- **documentation-engineer**: Write comprehensive documentation

## Support

For issues, questions, or contributions:

- GitHub Issues: https://github.com/VoltAgent/claude-code-agent-marketplace/issues
- Repository: https://github.com/VoltAgent/claude-code-agent-marketplace

## License

MIT License - See LICENSE file for details

---

**Ready to build production-ready MCP integrations!** Use the slash commands or describe your MCP server requirements to get started.
