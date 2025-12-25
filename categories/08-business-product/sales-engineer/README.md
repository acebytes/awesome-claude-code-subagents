# Sales Engineer Agent

Expert sales engineer specializing in technical pre-sales, solution architecture, and proof of concepts. Masters technical demonstrations, competitive positioning, and translating complex technology into business value for prospects and customers.

## Overview

The Sales Engineer agent is designed to accelerate sales cycles through technical expertise, delivering compelling demonstrations, designing effective proof of concepts, and providing technical validation that builds trust with prospects. This agent bridges the gap between product capabilities and customer needs, ensuring technical wins that drive business outcomes.

## Features

- **Technical Demonstrations**: Design and deliver compelling product demos tailored to prospect needs
- **Proof of Concept Development**: Create successful POCs with clear success criteria and measurable outcomes
- **Solution Architecture**: Design scalable, secure solutions that address customer requirements
- **RFP/RFI Responses**: Craft comprehensive technical responses to formal procurement processes
- **Technical Objection Handling**: Address performance, security, integration, and scalability concerns
- **Integration Planning**: Plan and document API integrations, authentication, and data flows
- **Performance Benchmarking**: Conduct load testing, stress testing, and performance analysis
- **Security Assessments**: Evaluate security architecture, compliance, and vulnerability concerns
- **Competitive Positioning**: Develop differentiation strategies and competitive analysis
- **Partner Enablement**: Train and enable partner sales engineers and technical teams

## Installation

1. Create the agent directory structure:
```bash
mkdir -p sales-engineer
cd sales-engineer
```

2. Copy the agent files:
- `CLAUDE.md` - Main agent instructions
- `mcp-config.json` - MCP server configuration
- `agent-manifest.json` - Agent metadata
- `README.md` - This file

3. Configure environment variables:
```bash
export GITHUB_TOKEN="your_github_personal_access_token"  # Optional, for GitHub integration
```

## MCP Servers

This agent uses the following MCP servers:

### Filesystem
- **Purpose**: Access project files, documentation, and technical materials
- **Command**: `npx -y @modelcontextprotocol/server-filesystem ${PWD}`
- **Use Cases**: Reading solution documentation, accessing demo scripts, managing POC files

### GitHub
- **Purpose**: Access repositories, manage code samples, and track technical issues
- **Command**: `npx -y @modelcontextprotocol/server-github`
- **Environment**: Requires `GITHUB_TOKEN` environment variable
- **Use Cases**: Sharing code examples, tracking POC progress, managing technical documentation

### Memory
- **Purpose**: Store and recall prospect context, technical requirements, and sales history
- **Command**: `npx -y @modelcontextprotocol/server-memory`
- **Use Cases**: Remembering prospect pain points, tracking demo outcomes, maintaining competitive intelligence

## Slash Commands

### /demo-prep
Prepare for a product demonstration.

**What it does:**
- Analyzes prospect requirements and pain points
- Sets up demo environment and scenarios
- Creates backup plans for common issues
- Develops feature-to-benefit talking points
- Prepares Q&A responses

**Example usage:**
```
/demo-prep for enterprise customer focused on security and compliance
```

### /poc-design
Design a proof of concept.

**What it does:**
- Defines clear success criteria
- Scopes realistic deliverables
- Plans environment setup and integration points
- Creates timeline and milestones
- Documents expected outcomes and measurement approach

**Example usage:**
```
/poc-design for API integration with customer's CRM system
```

### /rfp-response
Create technical RFP/RFI response.

**What it does:**
- Analyzes technical requirements
- Maps capabilities to requirements
- Creates architecture diagrams
- Documents security and compliance
- Provides performance specifications
- Includes integration details and reference architectures

**Example usage:**
```
/rfp-response for government procurement focused on data sovereignty
```

### /technical-proposal
Generate comprehensive technical proposal.

**What it does:**
- Documents solution architecture
- Outlines implementation approach
- Provides integration roadmap
- Estimates timeline and resources
- Includes risk mitigation strategies
- Calculates ROI and TCO
- Adds success metrics and KPIs

**Example usage:**
```
/technical-proposal for cloud migration and modernization project
```

## Usage Examples

### Example 1: Preparing a Demo
```
I have a demo tomorrow with a fintech company. They're concerned about:
- Real-time transaction processing
- PCI compliance
- Integration with legacy systems
- High availability requirements

Can you help me prepare?
```

The agent will:
1. Review the prospect's requirements
2. Design demo scenarios showcasing relevant capabilities
3. Prepare talking points mapping features to business value
4. Create backup plans for potential technical issues
5. Develop Q&A responses for common objections

### Example 2: Designing a POC
```
We need to create a POC for a large retailer evaluating our platform.
Their success criteria:
- Process 10K transactions/second
- 99.99% uptime
- Integration with Shopify and Salesforce
- 2-week timeline

/poc-design
```

The agent will:
1. Define measurable success criteria
2. Scope realistic deliverables within timeline
3. Plan environment provisioning
4. Document integration approach
5. Create milestone schedule
6. Define measurement methodology

### Example 3: RFP Response
```
/rfp-response for healthcare system RFP requiring:
- HIPAA compliance
- Multi-tenant architecture
- SSO integration
- Audit logging
- Disaster recovery plan
```

The agent will:
1. Map requirements to product capabilities
2. Create detailed architecture diagrams
3. Document compliance approach
4. Provide security specifications
5. Include reference architectures
6. Add performance benchmarks

## Performance Metrics

The Sales Engineer agent tracks key performance indicators:

| Metric | Target | Description |
|--------|--------|-------------|
| Demo Success Rate | > 80% | Percentage of successful demonstrations |
| POC Conversion | > 70% | Percentage of POCs converting to sales |
| Technical Accuracy | 100% | Accuracy of technical information |
| Response Time | < 24 hours | Average response time to questions |

## Integration with Other Agents

The Sales Engineer agent collaborates with:

- **product-manager**: Roadmap discussions and feature requests
- **solution-architect**: Detailed architecture design
- **customer-success-manager**: Post-sale handoffs
- **technical-writer**: Documentation creation
- **security-engineer**: Security assessments
- **devops-engineer**: Deployment planning
- **project-manager**: Implementation coordination

## Best Practices

1. **Always Lead with Discovery**
   - Understand business and technical requirements first
   - Map pain points before demonstrating solutions
   - Validate decision criteria and timeline

2. **Focus on Business Value**
   - Connect technical features to business outcomes
   - Demonstrate ROI and TCO benefits
   - Use customer's language and metrics

3. **Maintain Technical Accuracy**
   - Never overcommit on capabilities
   - Be honest about limitations
   - Document assumptions and dependencies

4. **Document Everything**
   - Create follow-up materials after every interaction
   - Maintain detailed POC documentation
   - Track competitive intelligence

5. **Build Trust Through Expertise**
   - Respond promptly to technical questions
   - Proactively identify and address risks
   - Collaborate effectively with account teams

## Workflow Phases

### 1. Discovery Analysis
- Gather business and technical requirements
- Assess current architecture and pain points
- Identify success criteria and decision process
- Analyze competition and timeline

### 2. Implementation Phase
- Prepare demo scenarios and environments
- Build POC infrastructure
- Create custom demonstrations
- Develop integrations and conduct benchmarks
- Address technical objections

### 3. Technical Excellence
- Validate requirements and architect solution
- Demonstrate value and resolve objections
- Ensure POC success
- Deliver proposals and complete handoff

## Troubleshooting

### Demo Issues
- Always have backup demo environment ready
- Test all scenarios before customer demos
- Prepare offline capabilities for network issues
- Have sample data readily available

### POC Challenges
- Set realistic scope and timelines upfront
- Maintain regular communication with stakeholders
- Document all issues and resolutions
- Have escalation path for blockers

### Integration Problems
- Validate API access and credentials early
- Create detailed integration documentation
- Test error handling scenarios
- Plan rollback strategies

## Support and Feedback

For questions, issues, or suggestions:
- Review the agent instructions in `CLAUDE.md`
- Check the agent manifest in `agent-manifest.json`
- Consult with other business-product agents
- Provide feedback to improve agent capabilities

## Version History

- **1.0.0** (2025-12-24): Initial release
  - Technical demonstrations
  - POC development
  - RFP/RFI responses
  - Technical proposals
  - Integration planning
  - Performance benchmarking
  - Security assessments
  - Competitive positioning

## License

Part of the Claude Code Agent Marketplace.
