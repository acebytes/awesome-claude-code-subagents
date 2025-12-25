# Network Engineer Agent

Expert network engineer specializing in cloud and hybrid network architectures, security, and performance optimization. Masters network design, troubleshooting, and automation with focus on reliability, scalability, and zero-trust principles.

## Overview

This agent is a senior network engineer with expertise in designing and managing complex network infrastructures across cloud and on-premise environments. It focuses on network architecture, security implementation, performance optimization, and troubleshooting with emphasis on high availability, low latency, and comprehensive security.

## Key Features

### Network Architecture
- **Topology design**: Hub-spoke, mesh, multi-tier architectures
- **Segmentation strategy**: Logical isolation and micro-segmentation
- **Routing protocols**: BGP, OSPF, static routing optimization
- **Multi-region design**: Global network with regional redundancy
- **SDN implementation**: Software-defined networking for agility

### Cloud Networking
- **VPC architecture**: Subnet design, route tables, NAT gateways
- **VPC peering**: Inter-VPC connectivity and transit gateways
- **Hybrid connectivity**: Direct Connect, ExpressRoute, Cloud Interconnect
- **VPN solutions**: Site-to-site and client VPN configurations
- **Multi-cloud networking**: Unified network across cloud providers

### Security Implementation
- **Zero-trust architecture**: Identity-based access and micro-segmentation
- **Firewall rules**: Next-gen firewalls and security groups
- **IDS/IPS deployment**: Intrusion detection and prevention systems
- **DDoS protection**: Layer 3/4/7 DDoS mitigation
- **WAF configuration**: Web application firewall policies
- **Network ACLs**: Stateless traffic filtering

### Performance Optimization
- **Bandwidth management**: Traffic shaping and QoS policies
- **Latency reduction**: Route optimization and edge computing
- **Load balancing**: Layer 4/7 load balancing with health checks
- **CDN integration**: Content delivery network placement
- **Caching strategies**: Strategic cache deployment

### Network Automation
- **Infrastructure as Code**: Terraform, CloudFormation for networks
- **Configuration management**: Automated device configuration
- **Compliance checking**: Automated security and policy validation
- **Self-healing networks**: Automated remediation and failover
- **Testing procedures**: Continuous network testing

## Slash Commands

### `/net-design`
Design network architecture for cloud/hybrid environments.

**Usage:**
```
/net-design Design a multi-region VPC architecture with hub-spoke topology for 50 microservices
```

**Capabilities:**
- VPC/VNet architecture design
- Subnet and CIDR planning
- Routing table configuration
- NAT gateway and internet gateway setup
- VPC peering and transit gateway design
- Network segmentation strategy
- Multi-region topology
- Disaster recovery networking

### `/net-secure`
Implement network security and zero-trust architecture.

**Usage:**
```
/net-secure Implement zero-trust network security with micro-segmentation for PCI-DSS compliance
```

**Capabilities:**
- Zero-trust architecture design
- Security group and firewall rule configuration
- Network ACL implementation
- Micro-segmentation strategy
- VPN security hardening
- DDoS protection setup
- IDS/IPS deployment
- Compliance validation (PCI-DSS, HIPAA, SOC2)

### `/net-troubleshoot`
Diagnose and resolve network performance issues.

**Usage:**
```
/net-troubleshoot Investigate high latency between us-east-1 and eu-west-1 regions
```

**Capabilities:**
- Flow log analysis
- Packet capture and protocol analysis
- Latency and bandwidth testing
- Route path analysis
- DNS resolution troubleshooting
- Load balancer health check diagnosis
- Network bottleneck identification
- Root cause analysis and remediation

## Use Cases

### Multi-Region Cloud Network
Design and implement global network infrastructure with:
- Hub-spoke VPC topology across multiple regions
- Transit gateway for centralized routing
- Direct Connect/ExpressRoute for on-premises connectivity
- Multi-region load balancing with health checks
- Low-latency inter-region communication
- Disaster recovery with automatic failover

### Zero-Trust Security Implementation
Build zero-trust network security with:
- Identity-based access controls
- Micro-segmentation of network zones
- East-west traffic inspection
- Least privilege network policies
- Encrypted communication (TLS/IPsec)
- Continuous monitoring and validation
- Threat detection and response

### Hybrid Cloud Connectivity
Connect on-premises and cloud environments with:
- Site-to-site VPN with redundancy
- Direct Connect/ExpressRoute/Cloud Interconnect
- SD-WAN deployment for multi-cloud
- Routing optimization for hybrid workloads
- Bandwidth allocation and QoS
- Unified monitoring and management

### High-Performance Networking
Optimize network performance with:
- Layer 7 load balancing with SSL termination
- GeoDNS for global traffic distribution
- CDN integration for content delivery
- Route optimization and multipath routing
- Traffic prioritization and QoS
- Edge computing and caching

## Network Patterns

### VPC Design Patterns
- **Hub-spoke topology**: Centralized shared services
- **Mesh networking**: Full connectivity between VPCs
- **Shared services VPC**: Common resources for all environments
- **DMZ architecture**: Public-facing and private zones
- **Multi-tier design**: Web, app, and data tier separation
- **Availability zones**: Multi-AZ for high availability
- **Transit gateway**: Scalable VPC connectivity

### Security Architecture
- **Perimeter security**: Edge protection with WAF and DDoS
- **Internal segmentation**: Isolate workloads and data
- **East-west security**: Inter-service traffic inspection
- **Zero-trust implementation**: Never trust, always verify
- **Encryption everywhere**: Data in transit and at rest
- **Access control**: Identity-based network policies
- **Threat detection**: Real-time monitoring and alerts

### Load Balancing Strategies
- **Layer 4 load balancing**: TCP/UDP traffic distribution
- **Layer 7 load balancing**: HTTP/HTTPS with content routing
- **Health checks**: Active monitoring of backend health
- **SSL termination**: Offload SSL/TLS processing
- **Session persistence**: Sticky sessions for stateful apps
- **Geographic routing**: Route based on user location
- **Auto-scaling integration**: Dynamic backend registration

## Integration with Other Agents

The network-engineer agent collaborates with:

- **cloud-architect**: Network architecture for cloud platforms
- **security-engineer**: Network security and compliance
- **kubernetes-specialist**: Container networking (CNI, service mesh)
- **devops-engineer**: Network automation in CI/CD
- **sre-engineer**: Network reliability and SLO management
- **platform-engineer**: Platform networking and developer experience
- **terraform-engineer**: Network Infrastructure as Code
- **incident-responder**: Network incident investigation

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read/write network diagrams, configurations, and documentation
- **github**: Access network infrastructure repositories
- **context7**: Maintain context about network topology and requirements
- **fetch**: Retrieve network documentation and vendor specifications

## Environment Variables

### Required
- `GITHUB_PERSONAL_ACCESS_TOKEN`: For accessing GitHub repositories

### Optional
None

## Best Practices

### Network Engineering Checklist
- [ ] Network uptime 99.99% achieved
- [ ] Latency < 50ms regional maintained
- [ ] Packet loss < 0.01% verified
- [ ] Security compliance enforced
- [ ] Change documentation complete
- [ ] Monitoring coverage 100% active
- [ ] Automation implemented thoroughly
- [ ] Disaster recovery tested quarterly

### Network Design Principles
1. **Design for redundancy**: No single points of failure
2. **Implement defense in depth**: Multiple security layers
3. **Optimize for performance**: Minimize latency and maximize throughput
4. **Monitor comprehensively**: Full visibility into network health
5. **Automate repetitive tasks**: Infrastructure as Code
6. **Document everything**: Architecture diagrams and runbooks
7. **Test failure scenarios**: Chaos engineering for networks
8. **Plan for growth**: Scalable and flexible design

### Security Best Practices
- Implement zero-trust network architecture
- Use micro-segmentation for workload isolation
- Encrypt all network traffic (TLS, IPsec)
- Apply least privilege access controls
- Deploy IDS/IPS for threat detection
- Regular security audits and penetration testing
- Automated compliance validation
- Incident response procedures

## Example Workflows

### Workflow 1: Multi-Region VPC Design
```
/net-design Design multi-region VPC architecture for global SaaS application with 99.99% availability

Agent will:
1. Design VPC topology (hub-spoke or mesh)
2. Plan CIDR blocks and subnet allocation
3. Configure routing tables and gateways
4. Set up VPC peering or transit gateway
5. Implement multi-region load balancing
6. Configure DNS with GeoDNS
7. Design disaster recovery failover
8. Document network architecture
```

### Workflow 2: Zero-Trust Security Implementation
```
/net-secure Implement zero-trust network security for microservices architecture

Agent will:
1. Design micro-segmentation strategy
2. Configure security groups per service
3. Implement network ACLs for layers
4. Set up service mesh for mTLS
5. Deploy IDS/IPS sensors
6. Configure WAF for web traffic
7. Enable flow logs and monitoring
8. Validate compliance requirements
```

### Workflow 3: Network Performance Troubleshooting
```
/net-troubleshoot Diagnose intermittent high latency in production VPC

Agent will:
1. Analyze VPC flow logs for patterns
2. Check routing table configurations
3. Test latency between availability zones
4. Review security group and ACL rules
5. Inspect load balancer health checks
6. Analyze DNS query response times
7. Identify bottlenecks and misconfigurations
8. Implement remediation and optimization
```

## Communication Protocol

### Network Assessment
The agent queries context for network requirements:

```json
{
  "requesting_agent": "network-engineer",
  "request_type": "get_network_context",
  "payload": {
    "query": "Network context needed: topology, traffic patterns, performance requirements, security policies, compliance needs, and growth projections."
  }
}
```

### Progress Tracking
The agent reports network implementation progress:

```json
{
  "agent": "network-engineer",
  "status": "optimizing",
  "progress": {
    "sites_connected": 47,
    "uptime": "99.993%",
    "avg_latency": "23ms",
    "security_score": "A+"
  }
}
```

## Monitoring and Troubleshooting

### Key Metrics
- **Uptime**: 99.99% availability target
- **Latency**: < 50ms regional, < 100ms global
- **Packet loss**: < 0.01%
- **Bandwidth utilization**: < 80% of capacity
- **Security events**: Real-time threat detection
- **Compliance score**: 100% policy adherence

### Troubleshooting Tools
- Flow log analysis for traffic patterns
- Packet capture for protocol analysis
- Path analysis for routing verification
- Latency measurement and testing
- Bandwidth testing and optimization
- Security scanning and vulnerability assessment
- Log aggregation and analysis
- Traffic simulation for capacity planning

## Getting Started

1. **Install the agent** using Claude Code CLI
2. **Configure MCP servers** in your environment
3. **Set environment variables** (GITHUB_PERSONAL_ACCESS_TOKEN)
4. **Start with design**: Use `/net-design` to architect network
5. **Implement security**: Use `/net-secure` for zero-trust implementation
6. **Monitor and optimize**: Use `/net-troubleshoot` for ongoing maintenance
7. **Automate operations**: Implement network Infrastructure as Code
8. **Continuous improvement**: Regular architecture reviews

## Success Metrics

- **Availability**: 99.99% network uptime
- **Performance**: < 50ms regional latency, < 0.01% packet loss
- **Security**: Zero security incidents, 100% compliance
- **Automation**: 80%+ network changes automated
- **Cost**: 40% reduction in operational costs
- **Scalability**: Support 10x traffic growth
- **Recovery**: < 5 minute failover time

## Learn More

- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/)
- [Azure Virtual Network](https://docs.microsoft.com/azure/virtual-network/)
- [Google Cloud VPC](https://cloud.google.com/vpc/docs)
- [Zero Trust Architecture (NIST)](https://www.nist.gov/publications/zero-trust-architecture)
- [SD-WAN Architecture](https://www.cisco.com/c/en/us/solutions/enterprise-networks/sd-wan/what-is-sd-wan.html)

---

**Version:** 1.0.0
**Category:** Infrastructure
**Maintained by:** Claude Agent Marketplace
