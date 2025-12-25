# UI Designer Agent

> Expert visual designer creating intuitive, beautiful, and accessible user interfaces

## Overview

The UI Designer agent specializes in visual design, interaction design, and design systems. It creates beautiful, functional interfaces that delight users while maintaining consistency, accessibility, and brand alignment across all touchpoints.

## Capabilities

### Primary Skills
- Design system creation and management
- Component library design
- Visual hierarchy and typography
- Color theory and theming
- Interaction design patterns
- Motion design principles
- Accessibility compliance (WCAG 2.1 AA)
- Cross-platform consistency

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write design tokens and component specs |
| github | Manage design system repositories |
| puppeteer | Visual testing and component screenshots |
| memory | Maintain design decisions context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/design-system` | Create or extend design system tokens |
| `/component-spec` | Generate component specifications |
| `/color-palette` | Design accessible color palette |
| `/design-audit` | Audit existing designs for consistency |

### Example Prompts

```
Create a design system with tokens for colors, typography, and spacing
```

```
Design button component with all states, variants, and accessibility
```

```
Audit our current UI for consistency and accessibility issues
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
    "puppeteer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-puppeteer"]
    }
  }
}
```

## Collaboration Network

### Provides To
- **frontend-developer**: Component specifications
- **mobile-developer**: Platform patterns

### Works With
- **ux-researcher**: User insights
- **accessibility-tester**: Compliance validation

## Best Practices

1. **Token-Based**: Use design tokens for consistency
2. **Accessibility First**: WCAG 2.1 AA minimum
3. **Documentation**: Comprehensive component specs
4. **States**: Cover all interactive states
5. **Dark Mode**: Design for both themes
