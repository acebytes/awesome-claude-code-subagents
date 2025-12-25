# Legal Advisor Agent

Expert legal advisor specializing in technology law, compliance, and risk mitigation. Masters contract drafting, intellectual property, data privacy, and regulatory compliance with focus on protecting business interests while enabling innovation and growth.

## Overview

The Legal Advisor agent provides comprehensive legal guidance for technology businesses, covering:

- **Contract Management**: Review, drafting, negotiation, and risk assessment
- **Privacy & Data Protection**: GDPR, CCPA compliance and privacy policy creation
- **Intellectual Property**: Patent, trademark, copyright, and trade secret protection
- **Compliance Frameworks**: Regulatory mapping and compliance program development
- **Risk Management**: Legal risk assessment and mitigation strategies

## Installation

1. Clone or download this agent directory
2. Ensure you have Node.js and npx installed
3. Set up required environment variables (optional):
   ```bash
   export GITHUB_TOKEN=your_github_personal_access_token
   ```

## Configuration

The agent uses three MCP servers:

### Filesystem Server
Provides access to local files for reviewing contracts, policies, and legal documents.

### GitHub Server
Enables repository access for code review, license compliance, and version control of legal documents.

**Environment Variable**: `GITHUB_TOKEN` - Personal access token for GitHub API access

### Memory Server
Maintains context about legal decisions, compliance requirements, and business constraints across conversations.

## Usage

### Starting the Agent

Load the agent with the MCP configuration:

```bash
claude-code --agent legal-advisor
```

### Slash Commands

#### /contract-review
Review and analyze contracts for legal risks, missing clauses, and areas for negotiation.

**Example**:
```
/contract-review vendor-agreement.pdf
```

**What it does**:
- Identifies legal risks and liabilities
- Highlights missing or problematic clauses
- Suggests negotiation points
- Provides risk mitigation recommendations

#### /tos-draft
Draft comprehensive Terms of Service agreements tailored to your business model.

**Example**:
```
/tos-draft for SaaS platform with user-generated content
```

**What it does**:
- Creates complete ToS documents
- Includes limitation of liability clauses
- Adds acceptable use policies
- Defines dispute resolution mechanisms
- Includes termination and warranty provisions

#### /privacy-policy
Create privacy policies that comply with GDPR, CCPA, and other relevant regulations.

**Example**:
```
/privacy-policy for mobile app collecting user location
```

**What it does**:
- Drafts compliant privacy policies
- Covers data collection and usage
- Includes user rights and consent mechanisms
- Addresses international data transfers
- Defines cookie policies and breach procedures

#### /ip-assess
Assess intellectual property portfolio and develop IP protection strategies.

**Example**:
```
/ip-assess for AI/ML startup with proprietary algorithms
```

**What it does**:
- Inventories IP assets
- Identifies protection gaps
- Recommends filing strategies
- Develops trade secret programs
- Creates licensing frameworks

## Core Capabilities

### Contract Management
- Comprehensive contract review and analysis
- Risk-based clause negotiation
- Amendment tracking and renewal management
- Dispute resolution procedures
- Template creation and standardization

### Privacy & Data Protection
- GDPR and CCPA compliance assessment
- Data processing agreement drafting
- Consent management frameworks
- Breach response procedures
- International data transfer mechanisms

### Intellectual Property
- Patent and trademark strategy
- Copyright and trade secret protection
- Licensing agreement development
- IP assignment documentation
- Infringement monitoring and defense

### Compliance Frameworks
- Regulatory requirement mapping
- Compliance program development
- Policy and procedure creation
- Audit preparation and support
- Training material development

### Risk Management
- Legal risk identification and assessment
- Mitigation strategy development
- Insurance requirement analysis
- Liability limitation frameworks
- Incident response planning

## Workflow

### 1. Assessment Phase
The agent begins by understanding your legal landscape:
- Reviews business model and operations
- Identifies legal risks and exposures
- Assesses current compliance status
- Audits existing contracts and policies
- Maps regulatory requirements

### 2. Implementation Phase
Develops legal protections and compliance:
- Drafts legal documents and policies
- Negotiates contract terms
- Implements compliance procedures
- Creates training materials
- Establishes monitoring systems

### 3. Excellence Phase
Achieves comprehensive legal protection:
- Ensures contract soundness
- Validates compliance achievement
- Confirms IP protection
- Verifies risk mitigation
- Maintains documentation

## Integration with Other Agents

The Legal Advisor collaborates with:
- **Product Manager**: Feature compliance review
- **Security Auditor**: Security compliance alignment
- **Business Analyst**: Requirement legal validation
- **HR Manager**: Employment law guidance
- **Data Engineer**: Privacy compliance support
- **CISO**: Security policy coordination

## Best Practices

### When Using This Agent

1. **Provide Context**: Share business model, jurisdictions, and risk tolerance
2. **Be Specific**: Clearly describe legal issues or requirements
3. **Review Thoroughly**: Always have qualified legal counsel review critical documents
4. **Stay Updated**: Regularly review compliance status and policy updates
5. **Document Everything**: Maintain audit trails and approval records

### Legal Excellence Standards

- Use clear, business-friendly language
- Apply risk-based approaches
- Provide practical, actionable solutions
- Enable business objectives
- Maintain comprehensive documentation
- Implement continuous monitoring
- Ensure stakeholder education

## Example Workflows

### Contract Review
```
User: Please review this vendor agreement for our SaaS platform
Agent: I'll conduct a comprehensive contract review focusing on:
       1. Liability and indemnification clauses
       2. Data protection and security requirements
       3. Termination and renewal terms
       4. Service level agreements
       5. Intellectual property rights

       [Detailed analysis follows...]
```

### Privacy Policy Creation
```
User: /privacy-policy for our mobile health app
Agent: I'll draft a HIPAA-compliant privacy policy covering:
       - Health data collection and usage
       - GDPR and CCPA compliance
       - User consent mechanisms
       - Data retention and deletion
       - Third-party sharing policies
       - Breach notification procedures

       [Complete policy document follows...]
```

### IP Strategy Development
```
User: /ip-assess our machine learning startup
Agent: Conducting IP portfolio assessment:
       1. Proprietary algorithms → Patent strategy
       2. Training datasets → Trade secret protection
       3. Brand assets → Trademark registration
       4. Code base → Copyright and licensing
       5. Employee agreements → IP assignment clauses

       [Detailed recommendations follow...]
```

## Limitations & Disclaimers

**Important**: This agent provides general legal information and guidance. It does NOT:
- Replace qualified legal counsel
- Provide jurisdiction-specific legal advice
- Create attorney-client privilege
- Guarantee legal compliance or protection

**Always consult with licensed attorneys** for:
- Jurisdiction-specific legal matters
- High-risk legal decisions
- Litigation or dispute resolution
- Regulatory filings and submissions
- Complex corporate transactions

## Support & Contribution

For issues, improvements, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

See the main repository for license information.
