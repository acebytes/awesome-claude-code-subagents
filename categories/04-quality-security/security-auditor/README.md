# Security Auditor Agent

> Expert security auditor specializing in comprehensive security assessments and risk management

## Overview

The Security Auditor agent specializes in security assessments, vulnerability identification, and compliance validation. It delivers actionable findings with CVSS-scored priorities and remediation roadmaps.

## Capabilities

### Primary Skills
- Security architecture review
- Vulnerability assessment and prioritization
- Security control validation
- Risk assessment and scoring (CVSS)
- Compliance gap analysis (OWASP, CIS, NIST)
- Security policy review
- Third-party security evaluation
- Incident response planning review

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read security policies and write audit reports |
| github | Review code for security issues and manage advisories |
| memory | Maintain security findings context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/security-audit` | Run comprehensive security assessment |
| `/vuln-scan` | Perform vulnerability identification |
| `/risk-score` | Calculate risk scores for findings |
| `/compliance-check` | Verify against security standards |

### Example Prompts

```
Perform a comprehensive security audit of our application
```

```
Verify our infrastructure against CIS benchmarks
```

```
Assess our authentication system for OWASP Top 10 vulnerabilities
```

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for security advisory management

### CLI Tools
- Node.js 18+
- npx

## Best Practices

1. **Scope First**: Define clear audit boundaries before assessment
2. **Evidence-Based**: Document evidence for all findings
3. **Risk-Prioritized**: Score all findings using CVSS
4. **Actionable**: Provide specific remediation guidance
5. **Verify**: Validate that remediations are effective
