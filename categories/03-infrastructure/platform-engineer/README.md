# Platform Engineer Agent

Expert platform engineer specializing in internal developer platforms, self-service infrastructure, and developer experience. Masters platform APIs, GitOps workflows, and golden path templates with focus on empowering developers and accelerating delivery.

## Overview

The Platform Engineer agent is designed to build and maintain comprehensive internal developer platforms that maximize developer productivity through self-service capabilities, golden path templates, and excellent developer experience. It specializes in platform architecture, GitOps workflows, service catalogs, and developer portal implementation.

## Key Capabilities

### Platform Architecture
- Multi-tenant platform design with resource isolation
- RBAC implementation and cost allocation tracking
- Usage metrics collection and compliance automation
- Audit trail maintenance and disaster recovery planning

### Self-Service Infrastructure
- Environment provisioning and database creation
- Service deployment and access management
- Resource scaling and monitoring setup
- Log aggregation and cost visibility

### GitOps Workflows
- Repository structure design and branch strategies
- PR automation workflows and approval processes
- Rollback procedures and drift detection
- Secret management and multi-cluster synchronization

### Golden Path Templates
- Service scaffolding and CI/CD pipeline templates
- Testing framework setup and monitoring configuration
- Security scanning integration and documentation templates
- Best practices enforcement and compliance validation

### Developer Portal
- Backstage implementation and customization
- Plugin development and documentation hub
- API catalog and metrics dashboards
- Cost reporting and security insights

### Platform APIs
- RESTful API design and GraphQL endpoints
- Event streaming setup and webhook integration
- Rate limiting and authentication/authorization
- API versioning strategy and SDK generation

## Slash Commands

### /platform-design
Design internal developer platform architecture, including self-service capabilities, platform APIs, and developer portal structure.

**Use cases:**
- Platform architecture planning
- Self-service capability design
- Developer portal structure
- Platform API strategy

### /platform-template
Create golden path template for services, including CI/CD pipelines, monitoring, security scanning, and best practices enforcement.

**Use cases:**
- Microservice template creation
- CI/CD pipeline standardization
- Monitoring and observability setup
- Security and compliance integration

### /platform-api
Create platform API for self-service provisioning, including authentication, rate limiting, versioning, and SDK generation.

**Use cases:**
- Infrastructure provisioning APIs
- Resource management endpoints
- Platform automation interfaces
- Developer tooling integration

## MCP Servers

### Required Servers

**filesystem**
- Read/write platform configurations
- Manage template repositories
- Handle infrastructure as code files
- Store documentation and guides

**github**
- GitOps repository management
- Pull request automation
- Code review workflows
- Documentation hosting

### Optional Servers

**context7**
- Project context and history tracking
- Platform decision documentation
- Team collaboration insights
- Knowledge management

## Platform Engineering Workflow

### 1. Developer Needs Analysis
- Developer journey mapping and tool usage assessment
- Workflow bottleneck identification and feedback collection
- Adoption barrier analysis and success metric definition
- Platform gap identification and roadmap prioritization

### 2. Implementation Phase
- Design for self-service and automate everything
- Create golden paths and build platform APIs
- Implement GitOps workflows and deploy developer portal
- Enable observability and document extensively

### 3. Platform Excellence
- Meet self-service targets and achieve platform SLOs
- Complete documentation and track adoption metrics
- Activate feedback loops and prepare training materials
- Define support processes and drive continuous improvement

## Platform Metrics

### Success Indicators
- Self-service rate exceeding 90%
- Provisioning time under 5 minutes
- Platform uptime 99.9%
- API response time < 200ms
- Documentation coverage 100%
- Developer onboarding < 1 day
- Developer satisfaction > 4.5/5

### Tracked Metrics
- Adoption rates and provisioning times
- Error rates and API latency
- User satisfaction and cost per service
- Time to production and platform reliability

## Integration with Other Agents

- **devops-engineer**: Provide self-service tools and automation
- **cloud-architect**: Deliver platform abstractions and multi-cloud support
- **sre-engineer**: Collaborate on reliability and observability
- **kubernetes-specialist**: Integrate orchestration and container platforms
- **security-engineer**: Enable compliance automation and security scanning
- **backend-developer**: Offer service templates and API standards
- **frontend-developer**: Support UI standards and frontend tooling
- **database-administrator**: Provide data service provisioning

## Best Practices

1. **Developer-First Design**: Prioritize developer experience in all platform decisions
2. **Self-Service Everything**: Automate common workflows with sub-5-minute provisioning
3. **Golden Paths**: Create opinionated templates that encode best practices
4. **Measure Everything**: Track adoption, satisfaction, and platform performance
5. **Documentation Culture**: Maintain 100% documentation coverage with interactive guides
6. **Feedback Loops**: Collect and act on developer feedback continuously
7. **Incremental Delivery**: Start with high-impact services and iterate
8. **Platform Reliability**: Maintain 99.9%+ uptime with comprehensive monitoring

## Example Use Cases

### Internal Developer Platform
Design and implement comprehensive IDP with Backstage, including service catalog, software templates, API documentation, and developer portal with self-service provisioning.

### Golden Path Templates
Create standardized templates for microservices, frontend applications, data pipelines, and ML services with integrated CI/CD, monitoring, security scanning, and compliance validation.

### Platform APIs
Build RESTful APIs for infrastructure provisioning, resource management, and platform automation with authentication, rate limiting, versioning, and auto-generated SDKs.

### GitOps Workflows
Implement GitOps-based infrastructure management with automated PR workflows, approval processes, drift detection, secret management, and multi-cluster synchronization.

### Developer Portal
Deploy and customize Backstage developer portal with plugins, documentation hub, API catalog, metrics dashboards, cost reporting, and security insights.

## Getting Started

1. Install required MCP servers (filesystem, github)
2. Configure GitHub personal access token for repository access
3. Use `/platform-design` to architect your platform
4. Use `/platform-template` to create golden path templates
5. Use `/platform-api` to build platform automation APIs
6. Track metrics and gather developer feedback
7. Iterate and improve based on adoption patterns

## Advanced Features

### Infrastructure Abstraction
- Crossplane compositions and Terraform modules
- Helm chart templates and Kubernetes operators
- Resource controllers and policy enforcement
- Configuration management and state reconciliation

### Adoption Strategies
- Platform evangelism and training programs
- Migration support and success stories
- Metric tracking and feedback incorporation
- Community building and champion programs

### Developer Enablement
- Onboarding programs and workshop delivery
- Documentation portals and video tutorials
- Office hours and Slack support
- FAQ maintenance and success tracking

---

**Platform Engineering Mission**: Empower developers to move fast and ship reliably through excellent platform abstractions, self-service capabilities, and golden path templates that reduce cognitive load and accelerate software delivery.
