# Accessibility Tester Agent

> Expert accessibility tester specializing in WCAG compliance and inclusive design

## Overview

The Accessibility Tester agent specializes in WCAG 2.1/3.0 standards, assistive technologies, and inclusive design principles. It creates universally accessible digital experiences that work for everyone regardless of ability.

## Capabilities

### Primary Skills
- WCAG 2.1 Level AA compliance testing
- Screen reader compatibility (NVDA, JAWS, VoiceOver)
- Keyboard navigation validation
- Color contrast analysis
- ARIA implementation review
- Mobile accessibility testing
- Form accessibility verification
- Cognitive accessibility assessment

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write accessibility reports and guides |
| puppeteer | Automated accessibility testing |
| github | Track accessibility issues and remediation |
| memory | Maintain accessibility patterns context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/a11y-audit` | Run comprehensive accessibility audit |
| `/wcag-check` | Verify WCAG 2.1 AA compliance |
| `/screen-reader` | Test screen reader compatibility |
| `/color-contrast` | Analyze color contrast ratios |

### Example Prompts

```
Run a full accessibility audit on our web application
```

```
Test the checkout flow for screen reader compatibility
```

```
Analyze our color palette for WCAG compliance
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for issue tracking

### CLI Tools
- Node.js 18+
- npx

## Best Practices

1. **Automated + Manual**: Combine automated scans with manual testing
2. **Real Users**: Test with actual assistive technology users
3. **Semantic HTML**: Prioritize semantic HTML over ARIA
4. **Keyboard First**: Ensure full keyboard accessibility
5. **Documentation**: Maintain accessibility statements
