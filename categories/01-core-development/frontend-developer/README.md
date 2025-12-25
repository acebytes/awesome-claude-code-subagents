# Frontend Developer Agent

> Expert UI engineer focused on crafting robust, scalable frontend solutions

## Overview

The Frontend Developer agent specializes in modern web applications with deep expertise in React, Vue, and Angular. It builds high-quality components prioritizing maintainability, user experience, and web standards compliance.

## Capabilities

### Primary Skills
- React component development with TypeScript
- State management (Redux, Zustand, Jotai)
- Responsive and adaptive layouts
- Accessibility (WCAG 2.1 AA compliance)
- Performance optimization
- Testing (Jest, Testing Library, Playwright)
- Build configuration (Vite, Webpack)
- Design system implementation

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write component files and configuration |
| github | Manage repositories and code reviews |
| context7 | Access React, Vue, and CSS framework documentation |
| puppeteer | Visual testing and browser automation |
| memory | Maintain component patterns context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/component` | Generate new React/Vue component with types and tests |
| `/storybook` | Create Storybook stories for component |
| `/a11y-audit` | Run accessibility audit on components |
| `/perf-analyze` | Analyze and optimize component performance |

### Example Prompts

```
Build a responsive dashboard component with charts and real-time data
```

```
Create a multi-step form with validation, error handling, and accessibility
```

```
Optimize the product list component for better performance and SEO
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for GitHub repository operations

### CLI Tools
- Node.js 18+
- npm or yarn
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
    "puppeteer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-puppeteer"]
    }
  }
}
```

## Collaboration Network

### Works With
- **ui-designer**: Receives designs and specifications
- **backend-developer**: API integration
- **websocket-engineer**: Real-time features

### Provides To
- **qa-expert**: Test IDs and testing support
- **mobile-developer**: Shared component logic

## Best Practices

1. **Accessibility First**: Build with screen readers in mind from the start
2. **Performance**: Monitor bundle size and render performance
3. **Testing**: Write tests alongside components
4. **TypeScript**: Use strict mode for type safety
5. **Documentation**: Include Storybook stories for all components
