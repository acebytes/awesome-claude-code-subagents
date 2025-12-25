# Mobile Developer Agent

> Cross-platform mobile specialist building performant native experiences

## Overview

The Mobile Developer agent specializes in cross-platform applications with deep expertise in React Native. It delivers native-quality mobile experiences while maximizing code reuse and optimizing for performance and battery life.

## Capabilities

### Primary Skills
- React Native cross-platform development
- Platform-specific UI (iOS HIG, Material Design 3)
- Native module integration
- Offline-first architecture
- Push notification systems (FCM, APNS)
- App store deployment
- Performance optimization
- Biometric authentication

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write mobile app source code and assets |
| github | Manage repositories, releases, and app store metadata |
| context7 | Access React Native, iOS, and Android documentation |
| memory | Maintain architecture and platform decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/mobile-init` | Initialize React Native project with best practices |
| `/native-module` | Create native module bridge |
| `/push-notification` | Set up push notification system |
| `/app-store` | Prepare for app store submission |

### Example Prompts

```
Build a React Native app with authentication and push notifications
```

```
Implement offline-first architecture with conflict resolution
```

```
Create a native module for biometric authentication
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- Node.js 18+
- npx
- react-native CLI

### Runtime Dependencies
- react-native
- expo-cli (optional)

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
- **ui-designer**: Platform-specific designs
- **qa-expert**: Device testing matrix

### Receives From
- **api-designer**: API specifications
- **product-manager**: Requirements

## Best Practices

1. **Platform Excellence**: Follow iOS HIG and Material Design 3
2. **Performance**: Monitor startup time and memory usage
3. **Offline First**: Build for unreliable connectivity
4. **Accessibility**: Support VoiceOver and TalkBack
5. **Code Sharing**: Maximize shared logic (>80%)
