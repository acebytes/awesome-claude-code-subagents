# Incident Responder Agent

Expert incident responder specializing in security and operational incident management. Masters evidence collection, forensic analysis, and coordinated response with focus on minimizing impact and preventing future incidents.

## Overview

The Incident Responder agent is a senior incident responder with expertise in managing both security breaches and operational incidents. It focuses on rapid response, evidence preservation, impact analysis, and recovery coordination with emphasis on thorough investigation, clear communication, and continuous improvement of incident response capabilities.

## Core Capabilities

### Incident Response Management
- **Response time < 5 minutes** - Rapid incident activation and initial assessment
- **Classification accuracy > 95%** - Precise incident categorization and severity determination
- **Complete documentation** - Comprehensive evidence and timeline tracking throughout response
- **Evidence preservation** - Proper chain of custody and forensic evidence collection
- **Communication SLA compliance** - Consistent stakeholder updates and coordination
- **Thorough recovery verification** - Complete system validation and hardening
- **Systematic lessons learned** - Post-incident analysis and knowledge capture
- **Continuous improvement** - Ongoing process and capability enhancement

### Incident Classification
- Security breaches (unauthorized access, data exfiltration, malware)
- Service outages (system failures, infrastructure issues)
- Performance degradation (resource exhaustion, bottlenecks)
- Data incidents (corruption, loss, exposure)
- Compliance violations (regulatory breaches, policy violations)
- Third-party failures (vendor outages, supply chain issues)
- Natural disasters (environmental impacts, physical damage)
- Human errors (misconfigurations, accidental deletions)

### Evidence Collection & Forensics
- Log preservation and analysis
- System snapshots and memory dumps
- Network traffic captures
- Configuration backups
- Audit trail collection
- User activity tracking
- Timeline reconstruction
- Forensic analysis techniques

### Investigation Techniques
- Log correlation and pattern analysis
- Root cause investigation
- Attack vector reconstruction
- Impact assessment
- Data flow tracing
- Threat intelligence integration
- Malware analysis
- Lateral movement tracking

### Communication & Coordination
- Incident commander assignment
- Stakeholder identification and management
- Regular status updates
- Customer communication
- Media response coordination
- Legal and compliance liaison
- Executive briefings
- Post-incident debriefs

### Containment & Recovery
- Service isolation and access revocation
- Traffic blocking and network segmentation
- Process termination and account suspension
- Data quarantine and system shutdown
- Service restoration and data recovery
- System rebuilding and validation
- Security hardening
- Performance verification

## Available Slash Commands

### `/incident-triage`
Assess incident severity, classify type, and determine response priority. Mobilize appropriate team members and initiate containment procedures.

**Use cases:**
- Initial incident assessment
- Severity classification
- Team mobilization
- Priority determination
- Containment activation

**Example:**
```
/incident-triage
We have reports of unauthorized API access from multiple IP addresses. Users are reporting unexpected account activity.
```

### `/incident-investigate`
Perform forensic analysis to determine root cause. Collect evidence, analyze logs, reconstruct timeline, and identify attack vectors or failure points.

**Use cases:**
- Forensic analysis
- Root cause determination
- Evidence collection
- Timeline reconstruction
- Attack vector identification

**Example:**
```
/incident-investigate
Analyze the security breach from 2024-12-20. Need to determine how attackers gained initial access and what data was accessed.
```

### `/incident-remediate`
Execute remediation plan including containment, eradication, and recovery. Verify system integrity and implement preventive measures.

**Use cases:**
- Containment execution
- System eradication
- Service recovery
- Security hardening
- Preventive controls

**Example:**
```
/incident-remediate
Execute full remediation for the compromised web servers. Need to rebuild systems, restore from clean backups, and implement additional security controls.
```

## Response Workflow

### 1. Response Readiness
- Response plan review and updates
- Team training and preparedness assessment
- Tool availability verification
- Communication template preparation
- Escalation procedure definition
- Recovery capability validation
- Documentation standard establishment
- Compliance requirement mapping

### 2. Implementation Phase
- Activate response team
- Assess incident scope and impact
- Contain and isolate affected systems
- Collect and preserve evidence
- Coordinate stakeholder communication
- Execute recovery procedures
- Document all actions and findings
- Extract lessons learned

### 3. Response Excellence
- Optimize response times
- Enhance procedures and playbooks
- Improve communication effectiveness
- Validate complete recovery
- Ensure thorough documentation
- Capture and apply learnings
- Implement improvements
- Maintain team readiness

## MCP Servers

This agent uses the following MCP servers:

### filesystem
File system operations for evidence collection, log analysis, and documentation.

### github
Integration with GitHub for incident tracking, postmortem documentation, and security advisories.

### context7
Advanced context management for incident correlation, pattern analysis, and knowledge base integration.

### fetch
HTTP operations for external threat intelligence, vendor status checks, and API integrations.

## Integration with Other Agents

The Incident Responder collaborates with other specialized agents:

- **security-engineer** - Security incident investigation and remediation
- **devops-incident-responder** - Operational incident handling
- **sre-engineer** - Reliability incident response
- **cloud-architect** - Cloud infrastructure incident management
- **network-engineer** - Network-related incident response
- **database-administrator** - Data incident handling
- **compliance-auditor** - Compliance violation incidents
- **legal-advisor** - Legal aspects of incident response

## Best Practices

### First Response
1. **Initial assessment** - Quickly evaluate scope and severity
2. **Severity determination** - Classify incident criticality
3. **Team mobilization** - Activate appropriate responders
4. **Containment actions** - Immediate threat isolation
5. **Evidence preservation** - Protect forensic data
6. **Impact analysis** - Assess business and technical impact
7. **Communication initiation** - Begin stakeholder updates
8. **Recovery planning** - Develop restoration strategy

### Documentation Standards
- Maintain detailed incident timeline
- Document all evidence with chain of custody
- Log all decisions and rationale
- Record communication and updates
- Catalog recovery procedures
- Capture lessons learned
- Track action items
- Measure response metrics

### Continuous Improvement
- Analyze incident patterns and trends
- Refine response processes
- Optimize detection and tools
- Enhance team training
- Update playbooks and procedures
- Implement automation opportunities
- Benchmark against industry standards
- Share knowledge across organization

## Performance Metrics

The agent tracks and optimizes:
- **Average response time** - Target < 5 minutes
- **Resolution rate** - Target > 95%
- **Classification accuracy** - Target > 95%
- **Communication SLA compliance** - Target 100%
- **Documentation completeness** - Target 100%
- **Stakeholder satisfaction** - Target > 4.0/5.0
- **Lessons learned capture** - Target 100%
- **Improvement implementation** - Continuous

## Compliance & Legal

### Regulatory Requirements
- GDPR breach notification (72 hours)
- PCI DSS incident response
- HIPAA breach notification
- SOC 2 incident handling
- State privacy law compliance

### Evidence Management
- Proper chain of custody
- Forensic evidence preservation
- Legal hold procedures
- Audit trail maintenance
- Retention policy compliance

### Communication Requirements
- Timely breach notification
- Customer communication
- Regulatory reporting
- Insurance claim documentation
- Contract obligation fulfillment

## Getting Started

1. **Review incident response plans** - Understand existing procedures and playbooks
2. **Assess team readiness** - Verify training, tools, and communication channels
3. **Validate detection capabilities** - Ensure monitoring and alerting effectiveness
4. **Test communication templates** - Prepare stakeholder notification procedures
5. **Verify recovery capabilities** - Validate backup and restoration processes
6. **Document escalation paths** - Define clear escalation and approval workflows
7. **Establish metrics baseline** - Begin tracking response performance
8. **Conduct tabletop exercises** - Practice incident scenarios with team

## Support

For questions or issues with the Incident Responder agent, please refer to the main repository documentation or open an issue in the GitHub repository.
