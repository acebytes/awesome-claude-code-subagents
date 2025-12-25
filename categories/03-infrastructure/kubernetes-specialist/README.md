# Kubernetes Specialist Agent

Expert Kubernetes specialist mastering container orchestration, cluster management, and cloud-native architectures. Specializes in production-grade deployments, security hardening, and performance optimization with focus on scalability and reliability.

## Overview

The Kubernetes Specialist agent is designed to manage production Kubernetes clusters with enterprise-grade reliability. From cluster architecture to workload orchestration, from security hardening to performance optimization, this agent implements comprehensive Kubernetes best practices that ensure scalability, security, and operational excellence.

## Key Capabilities

### Cluster Architecture
- **Control Plane Design**: Multi-master setup with HA, etcd clustering, API server load balancing
- **Node Management**: Node pools, taints/tolerations, affinity rules, auto-provisioning
- **Network Topology**: CNI selection, multi-zone distribution, service mesh integration
- **Storage Architecture**: CSI drivers, storage classes, dynamic provisioning, backup strategies

### Workload Orchestration
- **Deployments**: Rolling updates, blue-green, canary releases, progressive delivery
- **StatefulSets**: Persistent identity, ordered operations, volume claim templates
- **Jobs & CronJobs**: Batch processing, scheduled tasks, parallel execution
- **DaemonSets**: Node-level services, monitoring agents, network plugins

### Security Hardening
- **Pod Security**: Pod Security Standards (PSS), security contexts, capabilities control
- **Access Control**: RBAC configuration, service accounts, authentication mechanisms
- **Network Security**: Network policies, micro-segmentation, zero-trust networking
- **Policy Enforcement**: OPA/Gatekeeper, admission controllers, compliance automation

### Resource Management
- **Autoscaling**: HPA (Horizontal Pod Autoscaler), VPA (Vertical Pod Autoscaler), Cluster Autoscaler
- **Resource Optimization**: Requests/limits, QoS classes, resource quotas, rightsizing
- **Performance Tuning**: Pod priority, preemption, scheduling optimization
- **Cost Management**: Resource efficiency, spot instances, chargeback models

### Observability
- **Metrics**: Prometheus integration, custom metrics, SLI/SLO definition
- **Logging**: Centralized aggregation (ELK, Loki), audit logging, retention policies
- **Tracing**: Distributed tracing (Jaeger, Tempo), service dependency mapping
- **Monitoring**: Grafana dashboards, alerting, capacity planning, troubleshooting

### GitOps Workflows
- **ArgoCD**: Application deployment automation, multi-cluster management, progressive delivery
- **Flux**: GitOps toolkit, Kustomize/Helm support, image automation
- **Configuration Management**: Helm charts, Kustomize overlays, secret management
- **Environment Promotion**: Multi-environment workflows, rollback procedures, change tracking

## Slash Commands

### /k8s-deploy
Deploy application to Kubernetes with best practices.

```
/k8s-deploy [strategy]
```

**Strategies:**
- `rolling` - Rolling update deployment
- `blue-green` - Blue-green deployment
- `canary` - Canary deployment with traffic splitting
- `auto` - Auto-detect best strategy (default)

**Example usage:**

```bash
# Auto-detect and deploy with best strategy
/k8s-deploy

# Deploy with rolling update
/k8s-deploy rolling

# Deploy with blue-green strategy
/k8s-deploy blue-green

# Deploy with canary release
/k8s-deploy canary
```

**Actions performed:**
- Analyze application architecture and requirements
- Create optimized Kubernetes manifests (Deployment, Service, Ingress)
- Configure resource requests and limits
- Implement liveness, readiness, and startup probes
- Setup Horizontal Pod Autoscaler
- Configure Pod Security Standards
- Apply network policies for security
- Document deployment and operational procedures

**Example output:**
```
Kubernetes Deployment Created
==============================

Application: web-api
Namespace: production
Strategy: Rolling Update

Manifests Created:
- deployment.yaml (3 replicas, HPA 2-10)
- service.yaml (ClusterIP with session affinity)
- ingress.yaml (HTTPS with cert-manager)
- hpa.yaml (CPU 70%, memory 80%)
- network-policy.yaml (restricted egress/ingress)
- pdb.yaml (minAvailable: 2)

Resource Configuration:
- Requests: 500m CPU, 512Mi memory
- Limits: 1000m CPU, 1Gi memory
- QoS Class: Burstable
- Priority Class: high-priority

Security:
- Pod Security Standard: Restricted
- runAsNonRoot: true
- readOnlyRootFilesystem: true
- allowPrivilegeEscalation: false
- seccompProfile: RuntimeDefault

Health Checks:
- Liveness: /health/live (initialDelay: 30s)
- Readiness: /health/ready (initialDelay: 10s)
- Startup: /health/startup (failureThreshold: 30)

Autoscaling:
- Min replicas: 2
- Max replicas: 10
- Target CPU: 70%
- Target Memory: 80%

Network:
- Ingress: https://web-api.example.com
- Service Type: ClusterIP
- Network Policy: Deny all, allow ingress from frontend

Next Steps:
1. Apply manifests: kubectl apply -f k8s/
2. Verify deployment: kubectl rollout status deployment/web-api
3. Test endpoints: curl https://web-api.example.com/health
4. Monitor metrics in Grafana dashboard
```

### /k8s-scale
Configure autoscaling for Kubernetes workloads.

```
/k8s-scale [type]
```

**Types:**
- `hpa` - Horizontal Pod Autoscaler
- `vpa` - Vertical Pod Autoscaler
- `cluster` - Cluster Autoscaler
- `comprehensive` - All autoscaling types (default)

**Example usage:**

```bash
# Configure all autoscaling types
/k8s-scale

# Configure only HPA
/k8s-scale hpa

# Configure only VPA
/k8s-scale vpa

# Configure cluster autoscaling
/k8s-scale cluster
```

**Actions performed:**
- Analyze workload patterns and resource usage
- Configure HPA with CPU, memory, and custom metrics
- Setup VPA for resource optimization recommendations
- Configure Cluster Autoscaler for node scaling
- Define scaling policies and behaviors
- Set appropriate min/max replicas and thresholds
- Configure metrics collection and monitoring
- Document autoscaling behavior and tuning

**Example output:**
```
Autoscaling Configured
======================

Horizontal Pod Autoscaler (HPA):
- Name: web-api-hpa
- Min replicas: 2
- Max replicas: 10
- Metrics:
  * CPU: 70% (current: 45%)
  * Memory: 80% (current: 52%)
  * Custom: http_requests_per_second > 100
- Behavior:
  * Scale up: 4 pods/60s (max)
  * Scale down: 1 pod/300s (stabilization: 300s)

Vertical Pod Autoscaler (VPA):
- Name: web-api-vpa
- Mode: Recommendations (safe)
- Update policy: Auto
- Resource policy:
  * CPU: min 100m, max 2000m
  * Memory: min 128Mi, max 4Gi
- Current recommendations:
  * CPU request: 650m (from 500m)
  * Memory request: 768Mi (from 512Mi)

Cluster Autoscaler:
- Node pools: 3 (general, compute, memory)
- Min nodes per pool: 2
- Max nodes per pool: 20
- Scale-down enabled: true
- Scale-down delay: 10m
- Utilization threshold: 70%
- Skip nodes with local storage: true

Metrics Collection:
- Metrics Server: installed
- Custom Metrics API: enabled
- Prometheus adapter: configured
- Collection interval: 30s

Monitoring:
- Grafana dashboard: "Autoscaling Overview"
- Alerts configured for:
  * HPA at max replicas
  * VPA unable to apply recommendations
  * Cluster autoscaler failures
  * Node pool capacity limits

Expected Behavior:
- HPA will scale based on CPU, memory, and request rate
- VPA will optimize resource requests over time
- Cluster will auto-scale nodes based on pending pods
- Cost optimization through efficient resource usage

Next Steps:
1. Monitor autoscaling in action
2. Review VPA recommendations after 24 hours
3. Adjust thresholds based on traffic patterns
4. Test scale-up/down scenarios
```

### /k8s-secure
Implement Kubernetes security hardening and compliance.

```
/k8s-secure [framework]
```

**Frameworks:**
- `cis` - CIS Kubernetes Benchmark
- `pss` - Pod Security Standards
- `opa` - Open Policy Agent policies
- `comprehensive` - Full security hardening (default)

**Example usage:**

```bash
# Implement comprehensive security hardening
/k8s-secure

# Apply CIS Kubernetes Benchmark
/k8s-secure cis

# Configure Pod Security Standards
/k8s-secure pss

# Setup OPA policies
/k8s-secure opa
```

**Actions performed:**
- Audit current security posture and vulnerabilities
- Implement Pod Security Standards (Restricted level)
- Configure comprehensive RBAC policies
- Create network policies for micro-segmentation
- Setup admission controllers (ValidatingWebhook, MutatingWebhook)
- Implement OPA/Gatekeeper policies
- Configure secret management (External Secrets, Sealed Secrets)
- Document security controls and compliance status

**Example output:**
```
Kubernetes Security Hardening Complete
======================================

CIS Kubernetes Benchmark Compliance:
- Control Plane: 98% compliant (2/100 findings)
- Worker Nodes: 100% compliant
- Policies: 100% compliant
- Overall Score: 99/100

Pod Security Standards:
- Enforcement level: Restricted
- Audit level: Restricted
- Warning level: Restricted
- Exemptions: kube-system namespace only

Security Policies Applied:

1. Pod Security Policies:
   - runAsNonRoot: required
   - allowPrivilegeEscalation: false
   - readOnlyRootFilesystem: true
   - seccompProfile: RuntimeDefault
   - capabilities: drop ALL, add only NET_BIND_SERVICE

2. Network Policies:
   - Default deny all ingress/egress
   - Explicit allow rules per service
   - Namespace isolation enforced
   - 45 network policies created

3. RBAC Configuration:
   - Least privilege principle applied
   - 23 roles created (namespace-scoped)
   - 8 cluster roles created
   - No wildcard permissions
   - Service accounts per workload
   - Regular access reviews enabled

4. Admission Control:
   - ValidatingWebhook: image policy
   - MutatingWebhook: sidecar injection
   - Pod Security admission enabled
   - Resource quota admission enabled

5. OPA/Gatekeeper Policies:
   - Require resource limits (enforced)
   - Require labels (enforced)
   - Block latest tag (enforced)
   - Require readOnlyRootFilesystem (enforced)
   - Require non-root user (enforced)
   - 15 constraint templates created

6. Secret Management:
   - External Secrets Operator installed
   - Integration with AWS Secrets Manager
   - Automatic rotation enabled
   - Sealed Secrets for GitOps
   - Secret encryption at rest enabled

7. Image Security:
   - Image scanning in CI/CD (Trivy)
   - Policy: no critical vulnerabilities
   - Image signing required (Cosign)
   - Private registry authentication
   - Allowed registries whitelist

8. Audit Logging:
   - API server audit enabled
   - Audit policy: metadata + request/response
   - Log retention: 30 days
   - SIEM integration configured
   - Audit log analysis automated

Security Monitoring:
- Falco runtime security installed
- Alert on suspicious activity
- Compliance dashboard in Grafana
- Daily security scan reports
- Automated remediation for common issues

Compliance Status:
✓ CIS Benchmark: 99%
✓ Pod Security Standards: Restricted
✓ Network Segmentation: Complete
✓ RBAC: Least Privilege
✓ Secret Management: Encrypted
✓ Image Security: Scanning + Signing
✓ Audit Logging: Comprehensive

Vulnerabilities Remediated:
- 12 high-severity findings fixed
- 34 medium-severity findings fixed
- 67 low-severity findings fixed
- 0 critical findings remaining

Outstanding Items:
1. Update etcd to latest patch version (scheduled)
2. Rotate service account tokens (in progress)

Security Hardening Guide:
- Location: docs/security-hardening.md
- Incident response runbook: docs/security-incident-response.md
- Security review checklist: docs/security-checklist.md

Next Steps:
1. Review and approve security policies
2. Train team on security best practices
3. Schedule monthly security audits
4. Test incident response procedures
5. Enable automated compliance reporting
```

## Maturity Targets

The agent optimizes toward these Kubernetes excellence targets:

| Metric | Target | Industry Average |
|--------|--------|------------------|
| CIS Benchmark Compliance | 100% | 60-80% |
| Cluster Uptime | 99.95% | 99.0-99.5% |
| Pod Startup Time | <30s | 30-120s |
| Resource Utilization | >70% | 40-60% |
| Security Policy Coverage | 100% | 50-70% |
| RBAC Coverage | 100% | 60-80% |
| Network Policy Enforcement | 100% | 40-60% |
| Disaster Recovery (RTO) | <15min | 1-4 hours |

## Use Cases

### 1. Production Cluster Setup
**Problem**: Need to deploy production-grade Kubernetes cluster with enterprise requirements.

**Solution**:
- Design multi-master control plane across availability zones
- Implement comprehensive security hardening (CIS benchmark)
- Configure autoscaling (HPA, VPA, Cluster Autoscaler)
- Setup monitoring with Prometheus and Grafana
- Implement GitOps with ArgoCD

**Results**:
- 99.97% uptime achieved
- Sub-30 second pod startup times
- 78% resource utilization
- Zero security incidents
- 100% CIS benchmark compliance

### 2. Security Hardening
**Problem**: Cluster failing security audits, multiple compliance violations.

**Solution**:
```bash
/k8s-secure comprehensive
```

**Results**:
- 99% CIS benchmark compliance (from 45%)
- All workloads using Pod Security Standards (Restricted)
- Network policies enforced for all namespaces
- Zero-trust networking implemented
- Passed SOC 2 audit

### 3. Autoscaling Implementation
**Problem**: Manual scaling causing performance issues and high costs.

**Solution**:
```bash
/k8s-scale comprehensive
```

**Results**:
- HPA handling 10x traffic spikes automatically
- VPA optimizing resource requests (30% cost reduction)
- Cluster autoscaler managing node pools efficiently
- P95 latency maintained under 200ms
- 45% reduction in cloud costs

### 4. GitOps Migration
**Problem**: Manual deployments error-prone, no audit trail, difficult rollbacks.

**Solution**:
- Implement ArgoCD for application deployments
- Create Helm charts for all applications
- Setup multi-environment promotion workflow
- Configure automated sync policies

**Results**:
- 100% deployments through GitOps
- Complete audit trail in Git history
- Rollback time: <2 minutes
- Zero deployment errors
- Deployment frequency: 25+/day

### 5. Multi-Tenancy Platform
**Problem**: Multiple teams sharing cluster, need isolation and resource guarantees.

**Solution**:
- Implement namespace-based tenant isolation
- Configure resource quotas per tenant
- Apply network policies for segmentation
- Setup RBAC per tenant
- Enable cost allocation and chargeback

**Results**:
- 50 tenants on single cluster
- Complete isolation achieved
- Resource guarantees honored
- Per-tenant monitoring and alerting
- 60% reduction in infrastructure costs

## MCP Server Configuration

The agent uses three MCP servers for comprehensive Kubernetes capabilities:

### Filesystem Server (Required)
Access Kubernetes manifests, Helm charts, and cluster configurations.

```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
  }
}
```

**Used for**:
- Reading Kubernetes YAML manifests
- Accessing Helm charts and values files
- Reviewing Kustomize overlays
- Analyzing cluster configurations
- Reading policy definitions

### GitHub Server (Optional)
Manage GitOps workflows and track deployments.

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
- Managing ArgoCD application definitions
- Tracking deployment history
- Automating GitOps workflows
- Managing Helm chart repositories
- Coordinating environment promotions

### Context7 Server (Optional)
Access Kubernetes documentation and best practices.

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
- Accessing Kubernetes documentation
- Learning cloud-native patterns
- Understanding security best practices
- Researching deployment strategies
- Reviewing operator patterns

## Integration with Other Agents

### devops-engineer
Support with comprehensive container orchestration and Kubernetes platform management.

### cloud-architect
Collaborate on cloud-native architecture design and multi-cloud Kubernetes strategies.

### security-engineer
Work together on container security, compliance automation, and zero-trust networking.

### platform-engineer
Guide on building internal Kubernetes platforms and developer self-service portals.

### sre-engineer
Help with reliability engineering, SLO management, and incident response automation.

### deployment-engineer
Assist with Kubernetes deployment strategies and progressive delivery implementations.

### network-engineer
Partner on cluster networking, CNI selection, and network policy implementation.

### terraform-engineer
Coordinate on Kubernetes cluster provisioning and infrastructure as code.

## Best Practices

### Cluster Management
1. **High Availability**: Multi-master control plane across availability zones
2. **Regular Updates**: Keep Kubernetes version current (n-2 supported versions)
3. **Backup Strategy**: Regular etcd backups, test restoration procedures
4. **Monitoring**: Comprehensive observability with metrics, logs, and traces
5. **Security**: CIS benchmark compliance, Pod Security Standards, network policies
6. **Resource Management**: Define requests/limits, implement autoscaling
7. **GitOps**: All changes through version control, automated deployments
8. **Documentation**: Maintain runbooks, architecture diagrams, operational guides

### Deployment Patterns
1. **Rolling Updates**: Default for stateless applications
2. **Blue-Green**: Zero-downtime for critical services
3. **Canary**: Progressive rollout for risk mitigation
4. **Health Checks**: Implement liveness, readiness, startup probes
5. **Resource Limits**: Always define requests and limits
6. **Pod Disruption Budgets**: Ensure availability during updates
7. **Graceful Shutdown**: Use preStop hooks for clean termination
8. **Rollback Plan**: Test rollback procedures regularly

### Security Hardening
1. **Pod Security Standards**: Use Restricted level by default
2. **RBAC**: Implement least privilege access control
3. **Network Policies**: Default deny, explicit allow
4. **Secret Management**: External Secrets, encryption at rest
5. **Image Security**: Scan for vulnerabilities, sign images
6. **Admission Control**: Enforce policies at deployment time
7. **Audit Logging**: Enable comprehensive API audit logs
8. **Runtime Security**: Use Falco or similar for threat detection

## Getting Started

1. **Install the agent** in your Claude Code environment
2. **Configure MCP servers** (at minimum, filesystem server)
3. **Assess current cluster**: Review architecture and security posture
4. **Deploy workloads**: `/k8s-deploy` for applications
5. **Configure autoscaling**: `/k8s-scale comprehensive`
6. **Harden security**: `/k8s-secure comprehensive`
7. **Setup monitoring**: Prometheus, Grafana, and alerting
8. **Implement GitOps**: ArgoCD or Flux for deployments

## Example Workflow

```bash
# Step 1: Deploy application with best practices
/k8s-deploy rolling

# Step 2: Configure comprehensive autoscaling
/k8s-scale comprehensive

# Step 3: Implement security hardening
/k8s-secure comprehensive

# Step 4: Setup monitoring and observability
# Agent will guide through Prometheus/Grafana setup

# Step 5: Implement GitOps workflow
# Configure ArgoCD for automated deployments

# Step 6: Test disaster recovery
# Verify backup/restore procedures

# Step 7: Performance optimization
# Analyze and optimize resource usage

# Step 8: Documentation
# Create runbooks and operational guides
```

## Success Metrics

Track these metrics to measure Kubernetes excellence:

- **Cluster Uptime**: Target > 99.95% (4.38 hours downtime/year)
- **Pod Startup Time**: < 30 seconds for fast scaling
- **Resource Utilization**: > 70% for cost efficiency
- **Security Compliance**: 100% CIS benchmark coverage
- **Deployment Frequency**: 10+ deployments per day
- **Mean Time to Recovery**: < 15 minutes
- **Failed Deployment Rate**: < 5% of deployments
- **Cost per Workload**: Ongoing reduction through optimization
- **Security Incidents**: Zero critical vulnerabilities
- **Team Satisfaction**: > 4.5/5.0 developer happiness

## Advanced Features

### Custom Resources and Operators
- Define Custom Resource Definitions (CRDs)
- Implement Kubernetes operators with controller patterns
- Automated lifecycle management
- Domain-specific abstractions

### Service Mesh
- Istio or Linkerd implementation
- Traffic management and routing
- Mutual TLS (mTLS) encryption
- Observability integration
- Circuit breaking and retries

### Multi-Cluster Management
- Cluster federation for disaster recovery
- Cross-cluster service discovery
- Global load balancing
- Policy propagation
- Centralized monitoring

### Advanced Networking
- Multi-CNI configurations
- Network performance optimization
- Service mesh integration
- Ingress controller customization
- DNS customization and optimization

## Troubleshooting Guide

### Common Issues

**Pod CrashLoopBackOff**
- Check pod logs: `kubectl logs <pod>`
- Review events: `kubectl describe pod <pod>`
- Verify resource limits and requests
- Check health probe configurations

**ImagePullBackOff**
- Verify image name and tag
- Check registry authentication
- Review image pull secrets
- Validate network connectivity

**Pending Pods**
- Check node resources: `kubectl describe nodes`
- Review pod resource requests
- Verify node selectors and affinity
- Check taints and tolerations

**Network Connectivity Issues**
- Review network policies
- Check service endpoints
- Verify DNS resolution
- Validate ingress configuration

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT
