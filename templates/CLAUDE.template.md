# {{AGENT_NAME}}

> {{SHORT_DESCRIPTION}}

## Role Definition

{{ROLE_DEFINITION}}

## Available Tools

### Built-in Claude Code Tools
{{#each BUILTIN_TOOLS}}
- **{{this}}**
{{/each}}

### MCP Servers

{{#each MCP_SERVERS}}
#### {{this.name}}
- **Purpose**: {{this.purpose}}
- **Package**: `{{this.package}}`
{{#if this.envVars}}
- **Required Environment Variables**: {{#each this.envVars}}`{{this}}`{{#unless @last}}, {{/unless}}{{/each}}
{{/if}}
{{/each}}

## Invocation Protocol

When invoked:
{{#each INVOCATION_STEPS}}
{{@index}}. {{this}}
{{/each}}

## Slash Commands

| Command | Description | Usage |
|---------|-------------|-------|
{{#each SLASH_COMMANDS}}
| `{{this.name}}` | {{this.description}} | `{{this.usage}}` |
{{/each}}

## Capabilities Checklist

{{#each CAPABILITIES}}
- [ ] {{this}}
{{/each}}

## Domain Expertise

{{#each EXPERTISE_AREAS}}
### {{this.title}}
{{#each this.items}}
- {{this}}
{{/each}}

{{/each}}

## MCP Integration Patterns

{{#each MCP_PATTERNS}}
### {{this.server}}
**Purpose:** {{this.purpose}}

**Key Operations:**
{{#each this.operations}}
- {{this}}
{{/each}}

{{/each}}

## Communication Protocol

### Context Request
```json
{
  "requesting_agent": "{{AGENT_ID}}",
  "request_type": "get_{{DOMAIN}}_context",
  "payload": {
    "query": "{{CONTEXT_QUERY}}"
  }
}
```

## Workflow Phases

{{#each WORKFLOW_PHASES}}
### {{@index}}. {{this.name}}

{{this.description}}

{{#if this.steps}}
**Steps:**
{{#each this.steps}}
- {{this}}
{{/each}}
{{/if}}

{{/each}}

## Progress Reporting

```json
{
  "agent": "{{AGENT_ID}}",
  "status": "{{STATUS}}",
  "progress": {
    {{#each PROGRESS_METRICS}}
    "{{this.name}}": "{{this.value}}"{{#unless @last}},{{/unless}}
    {{/each}}
  }
}
```

## Collaboration Map

### Collaborates With
{{#each COLLABORATES_WITH}}
- **{{this.agent}}**: {{this.purpose}}
{{/each}}

### Delegates To
{{#each DELEGATES_TO}}
- **{{this.agent}}**: {{this.purpose}}
{{/each}}

### Receives From
{{#each RECEIVES_FROM}}
- **{{this.agent}}**: {{this.input}}
{{/each}}

## Best Practices

{{#each BEST_PRACTICES}}
- {{this}}
{{/each}}

---

*Always {{CORE_PRINCIPLES}}.*
