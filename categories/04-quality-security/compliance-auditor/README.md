# Compliance Auditor Agent

> Expert compliance auditor specializing in regulatory frameworks and security standards

## Overview

The Compliance Auditor agent specializes in regulatory compliance assessment, data privacy validation, and security certification audits. It delivers automated compliance validation with continuous monitoring capabilities.

## Capabilities

### Primary Skills
- Regulatory compliance assessment (GDPR, HIPAA, CCPA)
- Security certification audits (SOC 2, ISO 27001)
- PCI DSS compliance validation
- Data privacy impact assessments
- Compliance gap analysis
- Control mapping and testing
- Audit evidence collection
- Continuous compliance monitoring

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read compliance documentation and write audit reports |
| github | Track compliance issues and remediation progress |
| memory | Maintain compliance requirements context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/compliance-audit` | Run comprehensive compliance assessment |
| `/gdpr-check` | Verify GDPR compliance requirements |
| `/pci-validate` | PCI DSS compliance validation |
| `/soc2-assess` | SOC 2 readiness assessment |

### Example Prompts

```
Assess our data processing activities for GDPR compliance
```

```
Evaluate our readiness for SOC 2 Type II certification
```

```
Validate our payment processing system against PCI DSS requirements
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for issue tracking

### CLI Tools
- Node.js 18+
- npx

## Best Practices

1. **Know Your Scope**: Identify all applicable regulations early
2. **Map Controls**: Create clear mappings between controls and requirements
3. **Document Everything**: Maintain comprehensive audit evidence
4. **Risk-Based**: Prioritize gaps by compliance risk
5. **Continuous Monitoring**: Establish ongoing compliance validation
