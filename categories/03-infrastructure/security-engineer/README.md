# Security Engineer Agent

Expert infrastructure security engineer specializing in DevSecOps, cloud security, and compliance frameworks. Masters security automation, vulnerability management, and zero-trust architecture with emphasis on shift-left security practices.

## Overview

The Security Engineer agent is a comprehensive security automation and advisory system designed to help organizations build, maintain, and improve their security posture. With deep expertise in DevSecOps practices, cloud security architecture, compliance frameworks, and zero-trust principles, this agent transforms security from a bottleneck into an enabler of rapid, secure software delivery.

## Core Capabilities

### Infrastructure Security
- **System Hardening**: OS-level security baselines (CIS, STIG), kernel hardening, service minimization
- **Container Security**: Image scanning, runtime protection, admission controllers, pod security standards
- **Kubernetes Security**: RBAC policies, network policies, pod security admission, secrets encryption
- **Cloud Security**: Multi-cloud security architecture for AWS, Azure, and GCP
- **Network Security**: Micro-segmentation, network policies, service mesh security (mTLS)

### DevSecOps Practices
- **Shift-Left Security**: Security requirements in design, threat modeling, pre-commit checks
- **Security Testing Automation**: SAST, DAST, IAST, SCA, container scanning, IaC scanning
- **CI/CD Security**: Security gates, automated testing, vulnerability blocking, supply chain security
- **Security as Code**: Policy as code, compliance as code, security automation
- **Developer Enablement**: Security training, security champions program, secure coding standards

### Vulnerability Management
- **Automated Scanning**: Network, application, container, dependency, and IaC scanning
- **Risk-Based Prioritization**: CVSS scoring, EPSS modeling, business context
- **Patch Management**: Automated patching, virtual patching, compensating controls
- **Remediation Tracking**: SLA management, verification, metrics reporting
- **Threat Intelligence**: Integration with threat feeds, zero-day response

### Compliance Automation
- **Framework Support**: SOC 2, ISO 27001, PCI-DSS, HIPAA, GDPR, FedRAMP, CIS, NIST
- **Evidence Collection**: Automated evidence gathering, audit trail generation
- **Continuous Monitoring**: Real-time compliance checking, policy enforcement
- **Reporting**: Compliance dashboards, executive reporting, audit preparation

### Zero-Trust Architecture
- **Identity-Based Security**: IAM, RBAC, least privilege, conditional access
- **Micro-Segmentation**: Network segmentation, service mesh, API gateway security
- **Continuous Verification**: Device posture, risk-based authentication, MFA
- **Encryption**: Encryption at rest and in transit, TLS/mTLS, key management

### Incident Response
- **Detection**: SIEM rules, anomaly detection, threat hunting, security event correlation
- **Response**: Automated playbooks, containment procedures, forensics collection
- **Recovery**: Recovery procedures, business continuity, backup verification
- **Analysis**: Post-incident reviews, lessons learned, continuous improvement

## Slash Commands

### `/sec-scan [scope]`
Perform comprehensive security scan of infrastructure and applications.

**Scope Options:**
- `infrastructure` - Scan infrastructure and cloud resources
- `applications` - Scan applications and APIs
- `containers` - Scan container images and registries
- `dependencies` - Scan dependencies and libraries
- `iac` - Scan Infrastructure as Code
- `comprehensive` - Full security scan (default)

**Actions:**
- Analyze current security posture
- Run vulnerability scans across all layers
- Check compliance status against frameworks
- Review security configurations
- Scan for exposed secrets
- Assess attack surface
- Generate prioritized security report
- Provide remediation recommendations

**Examples:**
```
/sec-scan
/sec-scan infrastructure
/sec-scan applications
/sec-scan containers
```

### `/sec-harden [target]`
Harden infrastructure and implement security controls.

**Target Options:**
- `os` - Operating system hardening (CIS/STIG baselines)
- `containers` - Container security hardening
- `kubernetes` - Kubernetes security policies
- `cloud` - Cloud security configuration
- `network` - Network security controls
- `comprehensive` - Full hardening (default)

**Actions:**
- Apply security baselines (CIS, STIG)
- Implement defense-in-depth controls
- Configure encryption at rest and in transit
- Setup comprehensive security monitoring
- Enable detailed audit logging
- Implement RBAC policies
- Configure network segmentation
- Document all security configurations

**Examples:**
```
/sec-harden
/sec-harden os
/sec-harden kubernetes
/sec-harden comprehensive
```

### `/sec-audit [framework]`
Perform security audit and compliance assessment.

**Framework Options:**
- `soc2` - SOC 2 Type II audit
- `iso27001` - ISO 27001 compliance
- `pci-dss` - PCI-DSS assessment
- `hipaa` - HIPAA security evaluation
- `cis` - CIS benchmark audit
- `comprehensive` - Multi-framework audit (default)

**Actions:**
- Review compliance requirements
- Collect evidence and artifacts
- Assess security control effectiveness
- Identify compliance gaps
- Generate detailed audit report
- Create prioritized remediation plan
- Track compliance metrics
- Prepare for external audit

**Examples:**
```
/sec-audit
/sec-audit soc2
/sec-audit iso27001
/sec-audit comprehensive
```

## MCP Server Integration

### Filesystem Server (Required)
Access security configurations, compliance policies, infrastructure code, and security scanning reports.

**Use Cases:**
- Read and analyze security configuration files
- Review Infrastructure as Code for security issues
- Access compliance policy documents
- Analyze security scan results and vulnerability reports
- Manage security runbooks and incident response playbooks

### GitHub Server (Optional)
Manage security workflows, track vulnerabilities, and automate security checks in CI/CD pipelines.

**Use Cases:**
- Create and manage security scanning workflows
- Track security vulnerabilities and remediation
- Review pull requests for security issues
- Automate security gates in CI/CD
- Manage security incidents and issues
- Configure branch protection and security policies

**Setup:** Set `GITHUB_PERSONAL_ACCESS_TOKEN` with repo, security_events, and workflow permissions.

### Context7 Server (Optional)
Access security best practices, compliance frameworks, threat intelligence, and security design patterns.

**Use Cases:**
- Query security best practices and standards
- Access compliance framework requirements
- Research threat intelligence and CVE information
- Find security design patterns and architecture guidelines
- Access cloud security documentation
- Review security tool documentation

**Setup:** Set `CONTEXT7_API_KEY` from https://context7.com

## Security Targets

### Vulnerability Management
- **Critical Vulnerabilities**: 0 in production
- **High Vulnerabilities**: < 5 in production
- **Vulnerability Scan Coverage**: 100% of assets
- **Mean Time to Remediate (MTTR)**: < 7 days for critical, < 30 days for high

### Incident Response
- **Mean Time to Detect (MTTD)**: < 15 minutes
- **Mean Time to Respond (MTTR)**: < 30 minutes
- **Incident Prevention Rate**: > 90%
- **False Positive Rate**: < 5%

### Compliance
- **Compliance Score**: > 95%
- **Audit Readiness**: 100% of required controls
- **Evidence Collection**: 100% automated
- **Policy Violations**: 0 unresolved critical violations

### Security Testing
- **Security Test Coverage**: 100% of deployments
- **SAST/DAST Coverage**: 100% of applications
- **Container Scan Coverage**: 100% of images
- **IaC Scan Coverage**: 100% of infrastructure code

## Technologies and Tools

### Security Scanning
- **SAST**: Snyk, Checkmarx, Veracode, Semgrep, SonarQube
- **DAST**: OWASP ZAP, Burp Suite, Acunetix
- **SCA**: Snyk, Dependabot, WhiteSource, Black Duck
- **Container Scanning**: Trivy, Grype, Aqua, Prisma Cloud, Sysdig
- **IaC Scanning**: Checkov, tfsec, Terrascan, Bridgecrew
- **Secrets Scanning**: GitGuardian, TruffleHog, git-secrets

### Security Monitoring
- **SIEM**: Splunk, Elastic Security, Datadog Security Monitoring, Azure Sentinel
- **Cloud Security**: AWS Security Hub, Azure Defender for Cloud, GCP Security Command Center
- **Runtime Security**: Falco, Sysdig Secure, Aqua Runtime Protection
- **Vulnerability Management**: Qualys, Tenable, Rapid7 InsightVM

### Cloud Security
- **AWS**: Security Hub, GuardDuty, Inspector, Macie, IAM, KMS, CloudTrail, Config, WAF
- **Azure**: Defender for Cloud, Sentinel, Key Vault, Azure AD, Policy, Application Gateway
- **GCP**: Security Command Center, Cloud Armor, Cloud KMS, IAM, Cloud Logging, Binary Authorization

### Secrets Management
- HashiCorp Vault
- AWS Secrets Manager
- Azure Key Vault
- GCP Secret Manager
- Kubernetes Secrets (encrypted)

### Compliance Tools
- Drata
- Vanta
- Secureframe
- AuditBoard
- OneTrust

### Policy as Code
- Open Policy Agent (OPA)
- HashiCorp Sentinel
- Cloud Custodian
- Kyverno
- Gatekeeper

## Integration with Other Agents

### DevOps Engineer
- Guide on secure CI/CD pipeline design
- Implement DevSecOps practices
- Automate security testing in pipelines
- Integrate security scanning tools

### Cloud Architect
- Support security architecture design
- Review cloud security configurations
- Implement zero-trust architecture
- Design secure network topologies

### SRE Engineer
- Collaborate on incident response
- Share security monitoring and alerting
- Integrate security into reliability practices
- Joint on-call and incident management

### Kubernetes Specialist
- Implement Kubernetes security policies
- Configure pod security standards
- Setup network policies and service mesh
- Harden Kubernetes clusters

### Platform Engineer
- Design secure self-service platforms
- Implement security guardrails
- Automate security compliance
- Enable secure developer workflows

### Network Engineer
- Configure network security controls
- Implement micro-segmentation
- Setup security monitoring
- Design zero-trust network architecture

### Terraform Engineer
- Scan Infrastructure as Code for security issues
- Implement security policies in Terraform
- Automate security compliance checks
- Review and approve infrastructure changes

### Database Administrator
- Implement database encryption
- Configure access controls
- Monitor database security
- Ensure data protection compliance

## Workflow Examples

### Security Posture Assessment
1. **Discovery**: Inventory all assets and systems
2. **Scanning**: Run comprehensive security scans
3. **Analysis**: Analyze vulnerabilities and risks
4. **Prioritization**: Risk-based prioritization
5. **Remediation**: Create remediation plan
6. **Verification**: Verify fixes and rescan
7. **Reporting**: Generate executive reports

### DevSecOps Pipeline Implementation
1. **Design**: Design security-integrated CI/CD pipeline
2. **Scanning**: Integrate security scanning tools
3. **Gates**: Implement security quality gates
4. **Automation**: Automate security testing
5. **Monitoring**: Setup security monitoring
6. **Feedback**: Create developer feedback loops
7. **Training**: Train team on secure practices

### Compliance Automation
1. **Framework Selection**: Choose compliance frameworks
2. **Mapping**: Map controls to requirements
3. **Implementation**: Implement security controls
4. **Automation**: Automate evidence collection
5. **Monitoring**: Continuous compliance monitoring
6. **Reporting**: Automated compliance reporting
7. **Audit**: Prepare for external audits

### Incident Response
1. **Detection**: Detect security incident
2. **Triage**: Assess severity and impact
3. **Containment**: Contain the threat
4. **Investigation**: Forensic analysis
5. **Remediation**: Fix root cause
6. **Recovery**: Restore normal operations
7. **Post-Mortem**: Lessons learned and improvements

## Best Practices

### Security Principles
- **Security by Design**: Build security in from the start
- **Defense in Depth**: Multiple layers of security controls
- **Least Privilege**: Minimal necessary permissions
- **Zero Trust**: Never trust, always verify
- **Shift Left**: Security early in development
- **Automation**: Automate security wherever possible
- **Continuous Monitoring**: Always watch for threats
- **Assume Breach**: Plan for compromise

### Implementation Guidelines
1. Start with risk assessment and threat modeling
2. Implement preventive controls first
3. Add detective and responsive capabilities
4. Automate security testing and monitoring
5. Create feedback loops for continuous improvement
6. Document everything as code
7. Train and enable development teams
8. Measure and track security metrics

### Success Metrics
- Zero critical vulnerabilities in production
- High compliance scores (>95%)
- Fast incident response times (<30 min MTTR)
- High security test coverage (100%)
- Low false positive rates (<5%)
- High security awareness (100% training completion)

## Getting Started

1. **Setup MCP Servers**: Configure filesystem, GitHub (optional), and Context7 (optional)
2. **Initial Assessment**: Run `/sec-scan comprehensive` to assess current security posture
3. **Harden Infrastructure**: Use `/sec-harden comprehensive` to implement security controls
4. **Compliance Check**: Run `/sec-audit comprehensive` to assess compliance status
5. **Continuous Improvement**: Integrate security into CI/CD and implement continuous monitoring

## Support and Resources

- **Documentation**: See CLAUDE.md for detailed agent instructions
- **Configuration**: See mcp-config.json for MCP server setup
- **Manifest**: See agent-manifest.json for agent metadata
- **GitHub**: https://github.com/anthropics/claude-code-agent-marketplace

## License

MIT License - See LICENSE file for details

---

**Note**: This agent provides security guidance and automation capabilities. Always validate security recommendations in your specific context and ensure compliance with your organization's security policies and regulatory requirements. For production environments, consider engaging professional security assessors and penetration testers for comprehensive security validation.
