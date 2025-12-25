# WebSocket Engineer Agent

> Real-time communication specialist implementing scalable WebSocket architectures

## Overview

The WebSocket Engineer agent specializes in real-time communication systems with deep expertise in WebSocket protocols, Socket.IO, and scalable messaging architectures. It builds low-latency, high-throughput bidirectional communication systems handling millions of concurrent connections.

## Capabilities

### Primary Skills
- WebSocket server architecture
- Socket.IO implementation
- Connection management at scale
- Real-time message routing
- Presence and room systems
- Horizontal scaling with pub/sub
- Client library development
- Load balancing for WebSockets

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write server code and client libraries |
| github | Manage repositories and review real-time code |
| context7 | Access Socket.IO and WebSocket documentation |
| memory | Maintain architecture decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/websocket-init` | Initialize WebSocket server with best practices |
| `/socket-room` | Create room-based messaging system |
| `/socket-presence` | Implement presence tracking |
| `/socket-scale` | Configure horizontal scaling |

### Example Prompts

```
Build a scalable chat system with rooms and presence
```

```
Implement real-time dashboard updates with WebSockets
```

```
Configure horizontal scaling with Redis pub/sub
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- Node.js 18+
- npx

### Runtime Dependencies
- socket.io
- redis

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
- **backend-developer**: API integration
- **frontend-developer**: Client implementation
- **microservices-architect**: Service mesh integration

### Provides To
- **mobile-developer**: Mobile WebSocket clients
- **fullstack-developer**: Real-time features

## Best Practices

1. **Connection Management**: Proper heartbeat and reconnection
2. **Scaling**: Use Redis pub/sub for multi-node
3. **Performance**: Sub-10ms latency target
4. **Monitoring**: Track connections, messages, errors
5. **Graceful Shutdown**: Connection draining on deploy
