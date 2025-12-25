# {{AGENT_NAME}}

[![Version](https://img.shields.io/badge/version-{{VERSION}}-blue)]()
[![Category](https://img.shields.io/badge/category-{{CATEGORY_NAME}}-green)]()
[![MCP Servers](https://img.shields.io/badge/MCP%20servers-{{MCP_COUNT}}-orange)]()

> {{SHORT_DESCRIPTION}}

## Overview

{{LONG_DESCRIPTION}}

## Quick Start

### Prerequisites

**API Keys Required:**

| Key | Environment Variable | Provider | Required | Get Key |
|-----|---------------------|----------|----------|---------|
{{#each API_KEYS}}
| {{this.name}} | `{{this.envVar}}` | {{this.provider}} | {{#if this.required}}Yes{{else}}No{{/if}} | [{{this.provider}}]({{this.obtainUrl}}) |
{{/each}}

**CLI Tools:**
{{#each CLI_TOOLS}}
- `{{this}}`
{{/each}}

### Installation

1. Copy the agent configuration to your Claude Code settings:
```bash
# Add to your .claude/settings.json or project settings
```

2. Configure environment variables:
```bash
{{#each API_KEYS}}
{{#if this.required}}
export {{this.envVar}}="your-key-here"
{{/if}}
{{/each}}
```

3. Verify MCP servers are available:
```bash
claude mcp list
```

## Capabilities

### Primary Domain
{{PRIMARY_DOMAIN}}

### Skills
{{#each SKILLS}}
- {{this}}
{{/each}}

### Supported Languages/Frameworks
{{#each LANGUAGES}}
- {{this}}
{{/each}}

### Platforms
{{#each PLATFORMS}}
- {{this}}
{{/each}}

## Slash Commands

| Command | Description | Example |
|---------|-------------|---------|
{{#each SLASH_COMMANDS}}
| `{{this.name}}` | {{this.description}} | `{{this.usage}}` |
{{/each}}

## MCP Server Integration

{{#each MCP_SERVERS}}
### {{this.name}}
- **Package**: `{{this.package}}`
- **Purpose**: {{this.purpose}}
- **Required**: {{#if this.required}}Yes{{else}}No{{/if}}
{{#if this.envVars}}
- **Environment Variables**: {{#each this.envVars}}`{{this}}`{{#unless @last}}, {{/unless}}{{/each}}
{{/if}}

{{/each}}

## Usage Examples

{{#each EXAMPLES}}
### Example {{@index}}: {{this.title}}

**Prompt:**
```
{{this.prompt}}
```

**What this demonstrates:** {{this.capability}}

{{/each}}

## Collaboration

This agent works best when combined with:

{{#each COLLABORATORS}}
- **[{{this.name}}]({{this.path}})**: {{this.reason}}
{{/each}}

## Configuration

### Customizing MCP Servers

Edit `mcp-config.json` to:
- Add additional servers for extended functionality
- Modify environment variable mappings
- Enable/disable specific servers based on your needs

### Extending Capabilities

To extend this agent's capabilities:
1. Add new MCP servers to `mcp-config.json`
2. Update `agent-manifest.json` with new server references
3. Modify `CLAUDE.md` to include new tool usage patterns

## Troubleshooting

### Common Issues

**MCP Server Connection Failed**
- Verify the required environment variables are set
- Check that the MCP package is installed: `npm list -g @modelcontextprotocol/server-*`
- Ensure network connectivity for remote servers

**Missing Permissions**
- Some operations require elevated permissions
- Check file system access for local operations
- Verify API key scopes match required operations

**Tool Not Found**
- Restart Claude Code after configuration changes
- Verify `mcp-config.json` syntax is valid JSON
- Check server logs for startup errors

## Contributing

See [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines on:
- Adding new capabilities
- Updating MCP configurations
- Improving documentation

## License

MIT License - see [LICENSE](../../LICENSE)

---

**Category**: [{{CATEGORY_NAME}}](../)
**Registry**: [agent-registry.json](../../agent-registry.json)
