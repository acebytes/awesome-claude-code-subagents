# Cloud Architect Agent

Expert cloud architect specializing in multi-cloud strategies, scalable architectures, and cost-effective solutions. Masters AWS, Azure, and GCP with focus on security, performance, and compliance while designing resilient cloud-native systems.

## Overview

This agent is a senior cloud architect with expertise in designing and implementing scalable, secure, and cost-effective cloud solutions across AWS, Azure, and Google Cloud Platform. It focuses on multi-cloud architectures, migration strategies, and cloud-native patterns with emphasis on the Well-Architected Framework principles, operational excellence, and business value delivery.

## Key Features

### Multi-Cloud Expertise
- **AWS, Azure, GCP**: Deep knowledge across all major cloud providers
- **Cloud provider selection**: Strategic workload placement decisions
- **Vendor lock-in mitigation**: Design portable, multi-cloud architectures
- **Cost arbitrage**: Optimize costs across cloud providers
- **Unified monitoring**: Implement consistent observability across clouds

### Architecture Excellence
- **Well-Architected Framework**: Operational excellence, security, reliability, performance, cost optimization
- **High availability**: Design for 99.99% uptime with multi-region resilience
- **Scalability**: Auto-scaling strategies for dynamic workload management
- **Security by design**: Zero-trust principles and compliance automation
- **Infrastructure as Code**: Terraform, CloudFormation, ARM templates

### Cost Optimization
- **Resource right-sizing**: Optimize compute, storage, and network resources
- **Reserved instances**: Strategic capacity planning and commitment management
- **Spot/preemptible instances**: Leverage cheaper compute options
- **FinOps practices**: Financial operations and cost accountability
- **Storage lifecycle policies**: Automated data tiering and archival

### Cloud Migration
- **6Rs framework**: Rehost, replatform, refactor, repurchase, retire, retain
- **Application discovery**: Inventory and dependency mapping
- **Migration waves**: Phased approach with risk mitigation
- **Testing procedures**: Comprehensive validation and rollback planning
- **Cutover planning**: Minimize downtime and business impact

## Slash Commands

### `/cloud-design`
Design cloud architecture for scalability, security, and cost-effectiveness.

**Usage:**
```
/cloud-design Design a multi-region e-commerce platform supporting 100K concurrent users
```

**Capabilities:**
- Landing zone and account structure design
- Network topology (VPC/VNet, subnets, routing)
- Compute patterns (containers, serverless, VMs)
- Storage solutions (object, block, file systems)
- Database selection and data architecture
- Security architecture and compliance controls
- Monitoring and observability setup
- Disaster recovery planning

### `/cloud-cost`
Analyze and optimize cloud infrastructure costs.

**Usage:**
```
/cloud-cost Analyze current AWS spend and identify optimization opportunities
```

**Capabilities:**
- Cost breakdown analysis
- Resource right-sizing recommendations
- Reserved instance planning
- Spot instance opportunities
- Storage optimization (lifecycle policies, tiering)
- Network cost reduction
- License optimization
- FinOps implementation

### `/cloud-migrate`
Plan and execute cloud migration strategy.

**Usage:**
```
/cloud-migrate Plan migration of on-premises datacenter to AWS with minimal downtime
```

**Capabilities:**
- 6Rs assessment (rehost, replatform, refactor, etc.)
- Application discovery and dependency mapping
- Migration wave planning
- Risk assessment and mitigation
- Testing and validation procedures
- Cutover planning and execution
- Rollback strategies
- Post-migration optimization

## Use Cases

### Enterprise Cloud Transformation
Design and implement enterprise-wide cloud transformation with:
- Multi-account/subscription architecture
- Centralized identity and access management
- Network hub-and-spoke topology
- Shared services and landing zones
- Governance and compliance framework
- Cost allocation and chargeback

### High-Performance Applications
Build scalable, high-performance systems with:
- Auto-scaling compute clusters
- Content delivery networks (CDN)
- Edge computing and regional distribution
- Caching strategies (Redis, Memcached)
- Database optimization (read replicas, sharding)
- Load balancing and traffic management

### Data & Analytics Platforms
Design modern data platforms with:
- Data lake architecture (S3, ADLS, GCS)
- Stream processing (Kinesis, Event Hub, Pub/Sub)
- Data warehousing (Redshift, Synapse, BigQuery)
- ETL/ELT pipelines
- ML/AI infrastructure
- Real-time analytics

### Disaster Recovery & Business Continuity
Implement robust DR/BC solutions with:
- RTO/RPO definition and planning
- Multi-region active-active or active-passive
- Automated failover mechanisms
- Data replication strategies
- Backup and restore procedures
- DR testing and runbook creation

## Architecture Patterns

### Serverless Architectures
- Function as a Service (Lambda, Azure Functions, Cloud Functions)
- Event-driven design patterns
- API Gateway integration
- Step Functions/Logic Apps/Cloud Workflows
- Serverless databases (DynamoDB, Cosmos DB, Firestore)

### Container Orchestration
- Kubernetes (EKS, AKS, GKE)
- Container services (ECS, Container Instances, Cloud Run)
- Service mesh (Istio, Linkerd)
- CI/CD for containers
- Image registry management

### Hybrid Cloud
- VPN and Direct Connect/ExpressRoute/Interconnect
- Identity federation (AD, SSO, SAML)
- Workload placement strategies
- Data synchronization
- Unified management and monitoring

## Integration with Other Agents

The cloud-architect agent collaborates with:

- **devops-engineer**: Cloud automation and CI/CD pipelines
- **sre-engineer**: Reliability patterns and SLO management
- **security-engineer**: Cloud security and compliance controls
- **network-engineer**: Cloud networking and connectivity
- **kubernetes-specialist**: Container platform design
- **terraform-engineer**: Infrastructure as Code implementation
- **database-administrator**: Cloud database optimization
- **platform-engineer**: Platform engineering and developer experience

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read/write architecture diagrams, documentation, and IaC code
- **github**: Access cloud infrastructure repositories and collaborate on designs
- **context7**: Maintain context about architecture decisions and requirements
- **fetch**: Retrieve cloud provider documentation and pricing information

## Environment Variables

### Required
- `GITHUB_PERSONAL_ACCESS_TOKEN`: For accessing GitHub repositories

### Optional
None

## Best Practices

### Well-Architected Principles
1. **Operational Excellence**: Automation, monitoring, continuous improvement
2. **Security**: Defense in depth, least privilege, encryption
3. **Reliability**: Multi-AZ/region, auto-scaling, fault tolerance
4. **Performance Efficiency**: Right-sizing, caching, CDN
5. **Cost Optimization**: Reserved capacity, spot instances, lifecycle policies
6. **Sustainability**: Efficient resource usage, renewable energy regions

### Architecture Checklist
- [ ] 99.99% availability design achieved
- [ ] Multi-region resilience implemented
- [ ] Cost optimization > 30% realized
- [ ] Security by design enforced
- [ ] Compliance requirements met
- [ ] Infrastructure as Code adopted
- [ ] Architectural decisions documented
- [ ] Disaster recovery tested

### Security Architecture
- Implement zero-trust security model
- Use identity federation and SSO
- Encrypt data at rest and in transit
- Network segmentation and microsegmentation
- Automated compliance scanning
- Security monitoring and SIEM integration
- Incident response procedures

## Example Workflows

### Workflow 1: Cloud Migration Assessment
```
/cloud-migrate Assess our 200-server on-premises datacenter for AWS migration

Agent will:
1. Discover applications and dependencies
2. Categorize workloads using 6Rs framework
3. Estimate cloud costs and ROI
4. Plan migration waves
5. Identify risks and mitigation strategies
6. Create detailed migration roadmap
```

### Workflow 2: Multi-Cloud Architecture Design
```
/cloud-design Design multi-cloud architecture with AWS primary and Azure DR

Agent will:
1. Design landing zones on both platforms
2. Plan network connectivity and integration
3. Define workload distribution strategy
4. Implement unified identity management
5. Set up cross-cloud monitoring
6. Document architecture decisions
7. Create disaster recovery procedures
```

### Workflow 3: Cost Optimization Review
```
/cloud-cost Analyze our monthly $500K cloud spend and reduce by 30%

Agent will:
1. Analyze current resource utilization
2. Identify idle and underutilized resources
3. Recommend right-sizing opportunities
4. Plan reserved instance purchases
5. Implement storage lifecycle policies
6. Optimize network data transfer
7. Set up cost monitoring and alerts
8. Track savings over time
```

## Communication Protocol

### Architecture Assessment
The agent queries context for architecture requirements:

```json
{
  "requesting_agent": "cloud-architect",
  "request_type": "get_architecture_context",
  "payload": {
    "query": "Architecture context needed: business requirements, current infrastructure, compliance needs, performance SLAs, budget constraints, and growth projections."
  }
}
```

### Progress Tracking
The agent reports implementation progress:

```json
{
  "agent": "cloud-architect",
  "status": "implementing",
  "progress": {
    "workloads_migrated": 24,
    "availability": "99.97%",
    "cost_reduction": "42%",
    "compliance_score": "100%"
  }
}
```

## Getting Started

1. **Install the agent** using Claude Code CLI
2. **Configure MCP servers** in your environment
3. **Set environment variables** (GITHUB_PERSONAL_ACCESS_TOKEN)
4. **Start with assessment**: Use `/cloud-design` or `/cloud-migrate` to begin
5. **Review recommendations**: Analyze architecture proposals and cost estimates
6. **Implement incrementally**: Start with pilot workloads
7. **Monitor and optimize**: Continuous improvement based on metrics

## Success Metrics

- **Availability**: 99.99% uptime achieved
- **Cost Optimization**: >30% reduction in cloud spend
- **Security**: Zero security incidents, 100% compliance
- **Performance**: SLAs met or exceeded
- **Migration**: On-time, on-budget delivery
- **Scalability**: Auto-scaling handles 10x traffic spikes
- **Recovery**: RTO < 1 hour, RPO < 5 minutes

## Learn More

- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [Azure Architecture Center](https://docs.microsoft.com/azure/architecture/)
- [Google Cloud Architecture Framework](https://cloud.google.com/architecture/framework)
- [FinOps Foundation](https://www.finops.org/)
- [Cloud Native Computing Foundation](https://www.cncf.io/)

---

**Version:** 1.0.0
**Category:** Infrastructure
**Maintained by:** Claude Agent Marketplace
