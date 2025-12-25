# DevOps Engineer Agent

Expert DevOps engineer bridging development and operations with comprehensive automation, monitoring, and infrastructure management. Masters CI/CD, containerization, and cloud platforms with focus on culture, collaboration, and continuous improvement.

## Overview

The DevOps Engineer agent is designed to transform software delivery through automation, infrastructure as code, and cultural change. From CI/CD pipelines to container orchestration, from monitoring to incident response, this agent implements comprehensive DevOps practices that accelerate delivery while improving reliability and security.

## Key Capabilities

### Infrastructure as Code
- **Terraform**: Create modular, reusable infrastructure code with proper state management
- **CloudFormation**: Design AWS infrastructure with nested stacks and change sets
- **Ansible**: Automate configuration management and application deployment
- **Pulumi**: Leverage multi-language IaC with modern programming languages

### CI/CD Pipelines
- **Pipeline Design**: Build comprehensive CI/CD pipelines with proper stages and gates
- **Build Optimization**: Implement caching, parallelization, and incremental builds
- **Test Automation**: Integrate unit, integration, and end-to-end testing
- **Deployment Strategies**: Configure blue-green, canary, and rolling deployments

### Container Orchestration
- **Docker**: Create optimized, multi-stage Dockerfiles with security scanning
- **Kubernetes**: Deploy and manage containerized applications at scale
- **Helm**: Package applications with templated, versioned charts
- **Service Mesh**: Implement advanced networking with Istio or Linkerd

### Monitoring & Observability
- **Metrics**: Collect and visualize application and infrastructure metrics
- **Logging**: Centralize logs with ELK stack or cloud-native solutions
- **Tracing**: Implement distributed tracing for microservices
- **Alerting**: Configure intelligent alerts with proper escalation

### Cloud Platforms
- **AWS**: EC2, ECS, EKS, Lambda, RDS, S3, CloudWatch, and more
- **Azure**: VM, AKS, Azure DevOps, Cosmos DB, App Services, Monitor
- **GCP**: Compute Engine, GKE, Cloud Build, Cloud SQL, Cloud Monitoring
- **Multi-Cloud**: Design portable solutions across cloud providers

### Security Integration
- **DevSecOps**: Integrate security throughout the development lifecycle
- **Vulnerability Scanning**: Automate SAST, DAST, and container scanning
- **Compliance**: Implement automated compliance checks and reporting
- **Secret Management**: Secure secrets with Vault, AWS Secrets Manager, etc.

## Slash Commands

### /devops-pipeline
Create or optimize CI/CD pipeline configuration.

```
/devops-pipeline [platform]
```

**Platforms:**
- `github-actions` - GitHub Actions workflow
- `gitlab-ci` - GitLab CI/CD pipeline
- `jenkins` - Jenkins pipeline
- `circleci` - CircleCI configuration
- `auto` - Auto-detect from repository (default)

**Example usage:**

```bash
# Auto-detect and create optimal pipeline
/devops-pipeline

# Create GitHub Actions workflow
/devops-pipeline github-actions

# Create GitLab CI pipeline
/devops-pipeline gitlab-ci
```

**Actions performed:**
- Analyze application stack and requirements
- Design multi-stage pipeline (build, test, deploy)
- Implement caching strategies
- Configure quality gates and approvals
- Setup artifact management
- Implement deployment strategies
- Configure monitoring and notifications
- Document pipeline usage and maintenance

**Example output:**
```
CI/CD Pipeline Created
======================

Platform: GitHub Actions
File: .github/workflows/ci-cd.yml

Pipeline Stages:
1. Build
   - Dependency caching enabled
   - Multi-platform builds (linux, macos)
   - Artifact upload to GitHub Packages

2. Test
   - Unit tests with coverage (>80% required)
   - Integration tests
   - E2E tests (parallel execution)
   - Security scanning (SAST/DAST)

3. Deploy
   - Staging (auto-deploy on main)
   - Production (manual approval)
   - Blue-green deployment strategy
   - Automated rollback on failure

Features:
- Build time: ~3 minutes (with caching)
- Parallel test execution
- Secrets management with GitHub Secrets
- Slack notifications on failure
- Deployment tracking and metrics

Next Steps:
1. Configure required secrets in repository settings
2. Review and adjust deployment targets
3. Setup branch protection rules
4. Configure monitoring alerts
```

### /devops-container
Containerize application with Docker and orchestration setup.

```
/devops-container [orchestration]
```

**Orchestration:**
- `docker` - Dockerfile only (default)
- `docker-compose` - Multi-container with Docker Compose
- `kubernetes` - Kubernetes manifests
- `helm` - Helm chart package

**Example usage:**

```bash
# Create optimized Dockerfile
/devops-container docker

# Create Docker Compose setup
/devops-container docker-compose

# Create Kubernetes manifests
/devops-container kubernetes

# Create Helm chart
/devops-container helm
```

**Actions performed:**
- Analyze application requirements
- Create multi-stage Dockerfile
- Optimize image size and layers
- Configure health checks
- Implement security best practices
- Setup container orchestration
- Configure resource limits
- Document container usage

**Example output:**
```
Application Containerized
=========================

Dockerfile created with multi-stage build:
- Stage 1: Build (Node 20 Alpine)
- Stage 2: Production (distroless/nodejs20)
- Image size: 85MB (vs 1.2GB base)

Optimizations:
- Layer caching for dependencies
- Non-root user execution
- Security scanning integrated
- Health check endpoint configured
- Resource limits defined

Kubernetes Deployment:
- Deployment with 3 replicas
- Horizontal Pod Autoscaler (2-10 pods)
- Service with LoadBalancer
- ConfigMap for configuration
- Secret for sensitive data
- Ingress for external access
- Resource requests/limits set

Files created:
- Dockerfile
- .dockerignore
- k8s/deployment.yaml
- k8s/service.yaml
- k8s/hpa.yaml
- k8s/configmap.yaml
- k8s/ingress.yaml

Next Steps:
1. Build image: docker build -t app:latest .
2. Test locally: docker run -p 8080:8080 app:latest
3. Push to registry: docker push registry/app:latest
4. Deploy to k8s: kubectl apply -f k8s/
```

### /devops-monitor
Setup monitoring, logging, and observability stack.

```
/devops-monitor [stack]
```

**Stacks:**
- `prometheus` - Prometheus + Grafana
- `elk` - Elasticsearch, Logstash, Kibana
- `datadog` - Datadog integration
- `newrelic` - New Relic setup
- `comprehensive` - Full observability stack (default)

**Example usage:**

```bash
# Setup comprehensive monitoring
/devops-monitor

# Setup Prometheus monitoring
/devops-monitor prometheus

# Setup ELK logging
/devops-monitor elk

# Setup Datadog integration
/devops-monitor datadog
```

**Actions performed:**
- Design monitoring architecture
- Configure metrics collection
- Setup log aggregation
- Implement distributed tracing
- Create dashboards and visualizations
- Configure intelligent alerts
- Define SLIs and SLOs
- Document observability practices

**Example output:**
```
Observability Stack Configured
==============================

Components:
1. Metrics (Prometheus + Grafana)
   - Application metrics (RED method)
   - Infrastructure metrics (USE method)
   - Custom business metrics
   - 15 pre-built dashboards

2. Logging (Loki + Promtail)
   - Centralized log aggregation
   - Log parsing and enrichment
   - 30-day retention policy
   - Full-text search enabled

3. Tracing (Tempo + Jaeger)
   - Distributed tracing
   - Service dependency mapping
   - Performance analysis
   - Error correlation

4. Alerting (AlertManager)
   - 25 alert rules configured
   - Severity-based routing
   - Slack integration
   - PagerDuty escalation

Dashboards Created:
- Application Overview
- Request Rate, Error Rate, Duration (RED)
- Infrastructure Utilization (USE)
- Database Performance
- API Endpoint Performance
- Error Tracking
- Custom Business Metrics

SLIs/SLOs Defined:
- API Availability: 99.9% (SLO)
- Response Time P95: <500ms (SLO)
- Error Rate: <0.1% (SLO)

Alert Configuration:
- Critical: PagerDuty + Slack (immediate)
- Warning: Slack (15min delay)
- Info: Slack (aggregated hourly)

Files created:
- prometheus/prometheus.yml
- prometheus/alerts.yml
- grafana/dashboards/*.json
- loki/loki-config.yml
- tempo/tempo-config.yml
- alertmanager/config.yml

Next Steps:
1. Deploy monitoring stack: kubectl apply -f monitoring/
2. Configure applications to expose metrics
3. Review and customize alert thresholds
4. Setup runbooks for common alerts
5. Schedule team training on new tools
```

## Maturity Targets

The agent optimizes toward these DevOps maturity targets:

| Metric | Target | Industry Average |
|--------|--------|------------------|
| Infrastructure Automation | 100% | 60-70% |
| Deployment Automation | 100% | 50-60% |
| Test Automation | >80% | 40-60% |
| Mean Time to Production | <1 day | 1-4 weeks |
| Service Availability | >99.9% | 95-99% |
| Deployment Frequency | 12+/day | Weekly-Monthly |
| Mean Time to Recovery | <30 min | 1-24 hours |
| Change Failure Rate | <15% | 15-30% |

## Use Cases

### 1. Manual Deployment Process
**Problem**: Manual deployments taking hours, error-prone, blocking team productivity.

**Solution**:
```bash
/devops-pipeline github-actions
```

**Results**:
- Automated build, test, deploy pipeline
- 10 minute deployment time (from 2+ hours)
- Zero-downtime deployments
- Automated rollback on failure
- 95% reduction in deployment errors

### 2. Inconsistent Infrastructure
**Problem**: Infrastructure configured manually, difficult to reproduce, prone to drift.

**Solution**:
- Implement Infrastructure as Code with Terraform
- Version control all infrastructure
- Automated drift detection
- Multi-environment consistency

**Results**:
- 100% infrastructure as code
- Environment provisioning in 15 minutes
- Zero configuration drift
- Complete audit trail
- Easy disaster recovery

### 3. Poor Visibility
**Problem**: Limited visibility into application performance, long time to detect issues.

**Solution**:
```bash
/devops-monitor comprehensive
```

**Results**:
- Comprehensive observability stack
- Real-time metrics and dashboards
- Centralized logging
- Distributed tracing
- Mean time to detection: <2 minutes

### 4. Slow Build Times
**Problem**: 30-minute build times slowing down development and deployments.

**Solution**:
- Implement build caching
- Configure parallel execution
- Optimize Docker layers
- Setup artifact reuse

**Results**:
- Build time: 30min → 3min (90% reduction)
- Faster feedback loops
- Improved developer productivity
- Reduced CI/CD costs

### 5. Container Adoption
**Problem**: Legacy application needs containerization for cloud migration.

**Solution**:
```bash
/devops-container kubernetes
```

**Results**:
- Optimized multi-stage Dockerfile
- Kubernetes manifests for orchestration
- Auto-scaling configuration
- Health checks and monitoring
- 85% reduction in infrastructure costs

## MCP Server Configuration

The agent uses four MCP servers for comprehensive DevOps capabilities:

### Filesystem Server (Required)
Access infrastructure configs, pipeline files, and deployment scripts.

```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
  }
}
```

**Used for**:
- Reading Terraform/CloudFormation templates
- Accessing CI/CD pipeline configurations
- Reviewing Dockerfiles and Kubernetes manifests
- Analyzing deployment scripts
- Reading configuration files

### GitHub Server (Optional)
Manage CI/CD workflows and track deployments.

```json
{
  "github": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-github"],
    "env": {
      "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_PERSONAL_ACCESS_TOKEN}"
    }
  }
}
```

**Used for**:
- Creating GitHub Actions workflows
- Managing repository settings
- Tracking deployment history
- Automating releases
- Monitoring CI/CD pipeline runs

### Context7 Server (Optional)
Access DevOps best practices and documentation.

```json
{
  "context7": {
    "command": "npx",
    "args": ["-y", "@upstash/context7-mcp-server"],
    "env": {
      "UPSTASH_VECTOR_REST_URL": "${UPSTASH_VECTOR_REST_URL}",
      "UPSTASH_VECTOR_REST_TOKEN": "${UPSTASH_VECTOR_REST_TOKEN}"
    }
  }
}
```

**Used for**:
- Accessing IaC best practices
- Learning container orchestration patterns
- Understanding monitoring strategies
- Researching deployment patterns
- Reviewing security best practices

### Fetch Server (Optional)
Query cloud provider APIs and monitoring endpoints.

```json
{
  "fetch": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-fetch"]
  }
}
```

**Used for**:
- Querying cloud provider APIs
- Checking deployment status
- Monitoring endpoint health
- Accessing metrics and logs
- Retrieving configuration data

## Integration with Other Agents

### deployment-engineer
Enable with comprehensive CI/CD infrastructure and deployment automation capabilities.

### cloud-architect
Support infrastructure automation, provisioning, and cloud-native architecture patterns.

### sre-engineer
Collaborate on reliability engineering, monitoring, incident response, and SLO management.

### kubernetes-specialist
Work together on container platforms, orchestration strategies, and Kubernetes optimization.

### security-engineer
Integrate security throughout the pipeline with DevSecOps practices and automation.

### platform-engineer
Guide on self-service infrastructure, developer portals, and platform engineering.

### database-administrator
Partner on database automation, backups, migrations, and performance optimization.

### network-engineer
Coordinate on network automation, infrastructure, and security configurations.

## Best Practices

### DevOps Transformation Approach
1. **Start Small**: Begin with quick wins to build momentum
2. **Measure Everything**: Establish baseline metrics before changes
3. **Automate Incrementally**: Don't try to automate everything at once
4. **Foster Culture**: DevOps is as much about culture as tools
5. **Security First**: Integrate security from the beginning
6. **Document Continuously**: Treat documentation as code
7. **Learn from Failures**: Blameless postmortems and continuous improvement
8. **Deliver Value**: Focus on business outcomes, not just technical metrics

### Common Implementation Patterns

#### CI/CD Pipeline
1. Source control triggers pipeline
2. Build and compile application
3. Run automated tests (unit, integration, e2e)
4. Security scanning (SAST, DAST, dependencies)
5. Build and scan container image
6. Deploy to staging environment
7. Run smoke tests
8. Manual approval gate for production
9. Deploy to production (blue-green/canary)
10. Monitor deployment health
11. Automated rollback on failure

#### Infrastructure as Code
1. Define infrastructure in code (Terraform/CloudFormation)
2. Version control all IaC
3. Code review for infrastructure changes
4. Automated testing and validation
5. Plan changes before applying
6. Apply changes through CI/CD
7. Drift detection and remediation
8. State management and backups

#### Container Deployment
1. Multi-stage Dockerfile for optimization
2. Security scanning in CI/CD
3. Image tagging strategy (semantic versioning)
4. Registry with vulnerability scanning
5. Kubernetes/orchestration deployment
6. Resource limits and requests
7. Health checks and readiness probes
8. Auto-scaling configuration
9. Monitoring and logging integration

#### Monitoring Setup
1. Define SLIs based on user experience
2. Set SLOs with error budgets
3. Implement metrics collection
4. Centralize logging
5. Add distributed tracing
6. Create actionable dashboards
7. Configure intelligent alerts
8. Write runbooks for alerts
9. Regular review and refinement

## Getting Started

1. **Install the agent** in your Claude Code environment
2. **Configure MCP servers** (at minimum, filesystem server)
3. **Assess current state**: Review existing infrastructure and processes
4. **Create CI/CD pipeline**: `/devops-pipeline`
5. **Containerize applications**: `/devops-container kubernetes`
6. **Setup monitoring**: `/devops-monitor comprehensive`
7. **Implement IaC**: Convert manual infrastructure to code
8. **Measure and improve**: Track metrics and iterate

## Example Workflow

```bash
# Step 1: Create CI/CD pipeline
/devops-pipeline github-actions

# Step 2: Containerize application
/devops-container helm

# Step 3: Setup comprehensive monitoring
/devops-monitor comprehensive

# Step 4: Implement infrastructure as code
# Agent will guide through Terraform/CloudFormation setup

# Step 5: Configure auto-scaling
# Based on monitoring metrics

# Step 6: Implement security scanning
# Integrated into CI/CD pipeline

# Step 7: Setup automated backups
# For databases and critical data

# Step 8: Create disaster recovery plan
# Multi-region, automated failover
```

## Success Metrics

Track these metrics to measure DevOps transformation success:

- **Deployment Frequency**: Target 10+ deployments per day
- **Lead Time**: From commit to production in < 1 day
- **MTTR**: Recovery from incidents in < 30 minutes
- **Change Failure Rate**: < 15% of deployments cause incidents
- **Automation Coverage**: > 90% of processes automated
- **Infrastructure as Code**: 100% of infrastructure in version control
- **Test Automation**: > 80% code coverage
- **Team Satisfaction**: > 4.0/5.0 developer happiness score
- **Cost Optimization**: Ongoing reduction in infrastructure costs
- **Security Compliance**: 100% automated compliance checks

## Advanced Features

### GitOps Workflows
- Git as single source of truth
- Declarative infrastructure and applications
- Automated synchronization with clusters
- Pull-based deployment model
- Audit trail through Git history

### Platform Engineering
- Self-service developer portals
- Golden paths and templates
- Internal platform APIs
- Developer experience optimization
- Cognitive load reduction

### Chaos Engineering
- Automated failure injection
- Resilience testing
- Game days and simulations
- Continuous validation
- Incident response practice

### Cost Optimization
- Resource rightsizing automation
- Spot instance utilization
- Reserved instance optimization
- Waste elimination
- Chargeback models

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT
