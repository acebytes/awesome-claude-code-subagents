# Electron Pro Agent

> Desktop application specialist building secure cross-platform solutions

## Overview

The Electron Pro agent specializes in cross-platform desktop applications with deep expertise in Electron 27+ and native OS integrations. It builds secure, performant desktop apps that feel native across Windows, macOS, and Linux.

## Capabilities

### Primary Skills
- Secure Electron application architecture
- Native OS integration (menus, tray, notifications)
- IPC communication patterns
- Auto-update system implementation
- Multi-window management
- Code signing and notarization
- Performance optimization
- Cross-platform build configuration

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write application source code and assets |
| github | Manage repositories, releases, and distribution |
| context7 | Access Electron and Node.js documentation |
| memory | Maintain architecture decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/electron-init` | Initialize secure Electron app with best practices |
| `/electron-ipc` | Create secure IPC channel with validation |
| `/electron-menu` | Generate native menu configuration |
| `/electron-update` | Implement auto-update system |

### Example Prompts

```
Build a secure Electron app with system tray and native notifications
```

```
Implement auto-update functionality with differential updates and rollback
```

```
Create a multi-window document editor with file associations
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub releases and distribution

### CLI Tools
- Node.js 18+
- npm
- npx

### Runtime Dependencies
- electron
- electron-builder

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
- **frontend-developer**: UI components
- **backend-developer**: API integration
- **security-auditor**: Security hardening

### Receives From
- **ui-designer**: Native UI patterns
- **product-manager**: Requirements

## Security Best Practices

1. **Context Isolation**: Always enabled for renderer processes
2. **Node Integration**: Disabled in renderers
3. **CSP**: Strict Content Security Policy
4. **IPC Validation**: Validate all IPC messages
5. **Code Signing**: Required for distribution
