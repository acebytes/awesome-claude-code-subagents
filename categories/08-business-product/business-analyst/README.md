# Business Analyst Agent

Expert business analyst specializing in requirements gathering, process improvement, and data-driven decision making with focus on delivering measurable business value.

## Overview

The Business Analyst agent is a senior-level specialist that bridges business needs and technical solutions. It excels at requirements elicitation, business process modeling, stakeholder management, and solution design with emphasis on driving organizational efficiency and delivering tangible business outcomes.

## Key Capabilities

- **Requirements Elicitation**: Stakeholder interviews, workshop facilitation, use case development, user story creation
- **Business Process Modeling**: BPMN notation, value stream mapping, swimlane diagrams, gap analysis
- **Data Analysis**: SQL queries, statistical analysis, KPI development, dashboard creation
- **Analysis Techniques**: SWOT analysis, root cause analysis, cost-benefit analysis, risk assessment
- **Solution Design**: Requirements documentation, functional specifications, data flow diagrams
- **Stakeholder Management**: Communication planning, conflict resolution, expectation management
- **Change Management**: Impact analysis, adoption strategies, success measurement
- **Business Intelligence**: Metric frameworks, report development, decision support

## Installation

### Prerequisites

- Node.js 18 or higher
- Claude Code CLI
- GitHub Personal Access Token (optional, for GitHub integration)

### Setup

1. **Clone or download this agent**:
   ```bash
   cd /path/to/your/agents/directory
   ```

2. **Set up environment variables** (if using GitHub integration):
   ```bash
   export GITHUB_TOKEN="your_github_personal_access_token"
   ```

   Get your token at: https://github.com/settings/tokens

3. **Install MCP servers** (they will auto-install on first use via npx):
   - `@modelcontextprotocol/server-filesystem` - For document management
   - `@modelcontextprotocol/server-github` - For version control integration
   - `@modelcontextprotocol/server-memory` - For context persistence
   - `@modelcontextprotocol/server-fetch` - For web research

## Usage

### Starting the Agent

```bash
claude-code --agent business-analyst
```

### Slash Commands

The Business Analyst agent provides specialized slash commands for common tasks:

#### `/requirements [project-name] [scope]`
Generate comprehensive business requirements documentation.

**Example**:
```
/requirements customer-portal "user authentication and profile management"
```

**Output**:
- Functional requirements
- Non-functional requirements
- Acceptance criteria
- Requirements traceability matrix
- Dependencies and constraints

#### `/user-story [feature-description]`
Create detailed user stories following best practices.

**Example**:
```
/user-story "As a customer, I want to reset my password so I can regain access to my account"
```

**Output**:
- User persona
- Story description
- Acceptance criteria
- Story points estimate
- Dependencies
- Test scenarios

#### `/process-map [process-name] [format]`
Design business process maps and diagrams.

**Example**:
```
/process-map "order fulfillment" bpmn
```

**Formats**:
- `bpmn` - Business Process Model and Notation
- `swimlane` - Cross-functional swimlane diagram
- `vsm` - Value Stream Map

**Output**:
- Process flow visualization
- Decision points
- Bottleneck identification
- Improvement opportunities

#### `/stakeholder-analysis [project-name]`
Conduct comprehensive stakeholder analysis.

**Example**:
```
/stakeholder-analysis "digital transformation initiative"
```

**Output**:
- Stakeholder identification
- Influence/Interest matrix
- Communication plan
- Engagement strategies
- Risk mitigation for stakeholder concerns

### Example Workflows

#### 1. Process Improvement Analysis

```
User: Analyze our customer onboarding process and identify bottlenecks

Business Analyst will:
1. Request current process documentation
2. Map the current state process
3. Identify bottlenecks and pain points
4. Analyze cycle time and efficiency metrics
5. Design improved future state process
6. Calculate ROI and implementation timeline
7. Deliver comprehensive improvement recommendations
```

#### 2. Requirements Documentation

```
User: /requirements "mobile app" "payment integration"

Business Analyst will:
1. Gather requirements through structured questions
2. Document functional requirements
3. Define non-functional requirements (security, performance)
4. Create acceptance criteria
5. Build requirements traceability matrix
6. Identify dependencies and risks
7. Produce comprehensive BRD
```

#### 3. Stakeholder Engagement

```
User: /stakeholder-analysis "CRM implementation project"

Business Analyst will:
1. Identify all stakeholders
2. Assess influence and interest levels
3. Map stakeholder relationships
4. Design communication strategy
5. Develop engagement plans
6. Create RACI matrix
7. Recommend conflict resolution approaches
```

## MCP Servers Configuration

### Filesystem
**Purpose**: Manage business documentation, requirements, and analysis files
- Read/write requirements documents
- Access process maps and diagrams
- Store analysis reports

### GitHub
**Purpose**: Version control for documentation and collaboration
- Track requirements changes
- Review documentation updates
- Manage project artifacts
- **Requires**: `GITHUB_TOKEN` environment variable

### Memory
**Purpose**: Maintain context across sessions
- Remember business objectives
- Store stakeholder preferences
- Retain requirements history
- Track project knowledge

### Fetch
**Purpose**: Research and competitive intelligence
- Industry best practices
- Competitive analysis
- External data sources
- Standards and regulations

## Best Practices

### Requirements Management
- Maintain 100% traceability
- Use SMART criteria (Specific, Measurable, Achievable, Relevant, Time-bound)
- Version control all documentation
- Obtain stakeholder sign-off
- Define clear acceptance criteria

### Process Analysis
- Document current state before future state
- Identify quick wins and long-term improvements
- Quantify benefits (time, cost, quality)
- Consider change management impact
- Plan iterative implementation

### Stakeholder Engagement
- Regular communication cadence
- Manage expectations proactively
- Address conflicts early
- Celebrate successes
- Maintain feedback loops

### Data-Driven Decision Making
- Define clear metrics and KPIs
- Validate data accuracy
- Use appropriate visualization
- Tell the story behind the data
- Support decisions with evidence

## Integration with Other Agents

The Business Analyst works collaboratively with other agents:

- **product-manager**: Requirements alignment and feature prioritization
- **project-manager**: Delivery planning and progress tracking
- **technical-writer**: Documentation creation and review
- **ux-researcher**: User needs and behavior insights
- **qa-expert**: Test planning and acceptance criteria
- **data-analyst**: Data analysis and insights generation
- **scrum-master**: Agile delivery and sprint planning

## Troubleshooting

### Common Issues

**Issue**: MCP servers not connecting
```bash
# Verify Node.js installation
node --version  # Should be 18+

# Test npx access
npx -y @modelcontextprotocol/server-filesystem --help
```

**Issue**: GitHub integration not working
```bash
# Check token is set
echo $GITHUB_TOKEN

# Verify token permissions (needs repo scope)
```

**Issue**: Memory not persisting
```bash
# Memory server requires write access to home directory
# Check permissions in ~/.mcp/memory/
```

## Advanced Usage

### Custom Process Templates

Create reusable templates for common processes:

```
User: Create a template for our standard approval workflow

The agent will:
1. Design generic approval process
2. Identify customization points
3. Document decision criteria
4. Create swimlane diagram
5. Save as reusable template
```

### Requirements Baseline Management

```
User: Create a requirements baseline for version 2.0

The agent will:
1. Consolidate all approved requirements
2. Assign unique identifiers
3. Create traceability matrix
4. Document dependencies
5. Freeze baseline in version control
6. Set up change control process
```

### ROI Analysis

```
User: Calculate ROI for automating our manual reporting process

The agent will:
1. Quantify current costs (time, errors, resources)
2. Estimate automation costs
3. Project efficiency gains
4. Calculate payback period
5. Perform sensitivity analysis
6. Recommend implementation approach
```

## Support and Contribution

- **Issues**: Report bugs or request features via GitHub Issues
- **Discussions**: Share use cases and best practices
- **Contributions**: Submit pull requests for improvements

## License

MIT License - See repository for full license text

## Version History

- **1.0.0** (2025-12-24): Initial release
  - Core business analysis capabilities
  - Requirements documentation
  - Process mapping
  - Stakeholder analysis
  - Slash commands implementation
