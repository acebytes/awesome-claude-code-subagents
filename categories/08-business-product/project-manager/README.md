# Project Manager Agent

Expert project manager specializing in project planning, execution, and delivery. Masters resource management, risk mitigation, and stakeholder communication with focus on delivering projects on time, within budget, and exceeding expectations.

## Overview

The Project Manager agent is a senior project management professional equipped to lead complex projects from inception to closure. It combines expertise in multiple project management methodologies (Agile, Waterfall, Hybrid) with practical tools for planning, tracking, and delivering successful projects.

## Key Capabilities

- **Project Planning**: Charter development, WBS creation, schedule and budget planning
- **Resource Management**: Team allocation, capacity planning, workload balancing
- **Risk Management**: Risk identification, assessment, mitigation, and tracking
- **Schedule Management**: Timeline development, critical path analysis, milestone tracking
- **Budget Tracking**: Cost estimation, variance analysis, financial reporting
- **Stakeholder Communication**: Status reporting, expectation management, decision facilitation
- **Quality Assurance**: Standards definition, deliverable validation, continuous improvement
- **Team Coordination**: Task assignment, blocker removal, conflict resolution

## Prerequisites

### Required

- **Node.js**: Version 18 or higher
- **GitHub Token**: Personal access token with repo and project permissions
  - Obtain at: https://github.com/settings/tokens
  - Required scopes: `repo`, `project`, `read:org`

### Optional

- **Git**: For version control integration
- **Project Management Tools**: Jira, Asana, or similar (for advanced integration)

## Installation

1. Clone or download this agent configuration

2. Set up environment variables:
```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

3. Install MCP servers (handled automatically by npx):
   - @modelcontextprotocol/server-filesystem
   - @modelcontextprotocol/server-github
   - @modelcontextprotocol/server-memory

## Configuration

### MCP Servers

The agent uses three MCP servers:

1. **filesystem** (required)
   - Purpose: Read/write project plans, status reports, risk registers
   - Command: `npx -y @modelcontextprotocol/server-filesystem ${PWD}`

2. **github** (required)
   - Purpose: Track issues, milestones, pull requests, team collaboration
   - Command: `npx -y @modelcontextprotocol/server-github`
   - Environment: `GITHUB_PERSONAL_ACCESS_TOKEN=${GITHUB_TOKEN}`

3. **memory** (optional)
   - Purpose: Store project context, decisions, lessons learned
   - Command: `npx -y @modelcontextprotocol/server-memory`

### Agent Configuration

The agent can be configured in your Claude Code settings by importing the `mcp-config.json` file or manually adding the MCP servers to your configuration.

## Usage

### Slash Commands

The Project Manager agent provides four specialized slash commands:

#### `/project-plan`
Create comprehensive project plan with WBS, timeline, and resources.

```
/project-plan
```

**Example prompts:**
- "Create a project plan for our mobile app redesign"
- "Generate a 6-month roadmap for the new API platform"
- "Plan the migration to microservices architecture"

**Output includes:**
- Project charter with objectives and success criteria
- Work breakdown structure (WBS)
- Resource allocation plan
- Schedule with milestones and dependencies
- Risk register
- Communication plan

#### `/milestone-track`
Track milestone progress and identify schedule risks.

```
/milestone-track
```

**Example prompts:**
- "Review current sprint milestones and identify delays"
- "Analyze Q4 milestone completion status"
- "Check critical path milestones for the product launch"

**Output includes:**
- Milestone completion status
- Schedule performance index (SPI)
- Identified delays and blockers
- Corrective action recommendations
- Updated timeline forecast

#### `/resource-allocate`
Optimize resource allocation across project tasks.

```
/resource-allocate
```

**Example prompts:**
- "Balance team workload for the next two sprints"
- "Allocate resources for concurrent projects A, B, and C"
- "Identify resource conflicts and suggest solutions"

**Output includes:**
- Resource capacity analysis
- Workload distribution by team member
- Over/under allocation identification
- Optimization recommendations
- Skill gap analysis

#### `/risk-register`
Maintain and update project risk register with mitigation plans.

```
/risk-register
```

**Example prompts:**
- "Update risk register with recent technical debt concerns"
- "Assess infrastructure risks for the new deployment"
- "Create contingency plans for identified critical risks"

**Output includes:**
- Risk identification and description
- Impact and probability assessment
- Risk priority matrix
- Mitigation strategies
- Contingency plans
- Risk owners and timelines

### General Prompts

Beyond slash commands, you can interact naturally with the Project Manager agent:

**Project Planning:**
- "Help me estimate the timeline for a new feature development"
- "What resources do we need for the Q1 initiative?"
- "Create a communication plan for stakeholders"

**Execution Monitoring:**
- "Analyze current project health and identify bottlenecks"
- "Generate a status report for the executive team"
- "What's our budget variance this quarter?"

**Risk Management:**
- "What are the top risks for launching on time?"
- "Help me create a risk mitigation plan for vendor delays"
- "Assess the impact of losing a key team member"

**Team Coordination:**
- "How should I handle this scheduling conflict?"
- "Suggest ways to improve team velocity"
- "Help me facilitate the retrospective meeting"

## Workflow

### 1. Project Initiation
```
User: "I need to plan a new e-commerce platform launch"
Agent:
- Queries for project context (objectives, scope, constraints)
- Creates project charter
- Develops initial WBS
- Identifies key stakeholders
- Establishes success criteria
```

### 2. Planning Phase
```
User: "/project-plan"
Agent:
- Breaks down work into manageable tasks
- Creates realistic timeline with dependencies
- Allocates resources based on skills and capacity
- Identifies risks and mitigation strategies
- Develops communication plan
- Sets quality standards
```

### 3. Execution Monitoring
```
User: "/milestone-track"
Agent:
- Reviews progress against baseline
- Calculates schedule performance (SPI)
- Identifies delays and blockers
- Recommends corrective actions
- Updates forecasts
```

### 4. Risk Management
```
User: "/risk-register"
Agent:
- Identifies new risks from project activity
- Assesses impact and probability
- Prioritizes risks by severity
- Develops mitigation plans
- Tracks mitigation progress
```

### 5. Project Closure
```
User: "Help me close out the project"
Agent:
- Validates deliverable completion
- Conducts lessons learned session
- Archives project documentation
- Analyzes success metrics
- Recognizes team contributions
```

## Success Metrics

The Project Manager agent tracks and reports on key performance indicators:

- **Schedule Performance Index (SPI)**: ≥ 0.95 (on or ahead of schedule)
- **Cost Performance Index (CPI)**: ≥ 0.95 (on or under budget)
- **Scope Variance**: < 10% (minimal scope creep)
- **Risk Mitigation**: > 90% of identified risks addressed
- **Stakeholder Satisfaction**: ≥ 85% satisfaction score
- **On-time Delivery**: > 90% of milestones met
- **Budget Variance**: < 5% variance from baseline
- **Team Morale**: Positive and improving

## Best Practices

### Planning
- Break down complex projects into manageable work packages
- Include realistic buffers for uncertainty (10-20%)
- Map dependencies early to identify critical path
- Involve stakeholders in planning for buy-in
- Establish clear success criteria upfront

### Execution
- Monitor progress daily, review weekly
- Address blockers within 24 hours
- Communicate proactively, not reactively
- Enforce quality gates at key milestones
- Celebrate team wins regularly

### Risk Management
- Review risk register weekly
- Update probability/impact as context changes
- Activate contingency plans early
- Document lessons learned continuously
- Don't ignore small risks that could compound

### Communication
- Tailor messages to audience (exec vs. team)
- Use visual dashboards for clarity
- Establish regular cadence (daily standups, weekly reviews)
- Document all major decisions
- Create feedback loops with stakeholders

## Collaboration

The Project Manager agent works effectively with:

- **Business Analyst**: Requirements gathering and scope definition
- **Product Manager**: Product roadmap alignment and delivery
- **Scrum Master**: Agile ceremony facilitation and sprint planning
- **QA Expert**: Quality planning and acceptance criteria
- **Technical Lead**: Technical feasibility and architecture decisions
- **DevOps Engineer**: Deployment planning and infrastructure
- **Stakeholders**: Status updates and expectation management

## Troubleshooting

### GitHub Token Issues
```
Error: GitHub API authentication failed
Solution: Verify GITHUB_TOKEN is set correctly and has required scopes
```

### MCP Server Connection
```
Error: Cannot connect to MCP server
Solution: Ensure Node.js is installed and npx can access npm registry
```

### Missing Project Context
```
Agent: "I need more information about project scope"
Solution: Provide objectives, timeline, budget, and success criteria upfront
```

### Resource Conflicts
```
Issue: Over-allocated team members
Solution: Use /resource-allocate to identify conflicts and rebalance workload
```

## Examples

### Example 1: New Project Planning
```
User: "Plan a 3-month project to migrate our monolith to microservices"

Agent: "I'll create a comprehensive project plan. Let me gather some context:
- What's the current monolith stack?
- How many microservices are targeted?
- Team size and skills available?
- Budget constraints?
- Critical business functions to prioritize?

[After receiving context]

I've created a project plan with:
✓ 12-week timeline with 4 major milestones
✓ Work breakdown structure (89 tasks across 6 work packages)
✓ Resource allocation (3 backend devs, 2 DevOps, 1 QA)
✓ Risk register (8 identified risks, all with mitigation plans)
✓ Budget estimate: $240K (within your $250K constraint)
✓ Communication plan (weekly stakeholder updates, daily standups)

Critical path: Database migration → Service extraction → API gateway → Testing
Next step: Review and approve plan, then commence Phase 1"
```

### Example 2: Milestone Tracking
```
User: "/milestone-track"

Agent: "Milestone Status Report - Week 8 of 12

✓ M1: Architecture Design (Week 2) - COMPLETE
✓ M2: Infrastructure Setup (Week 4) - COMPLETE
⚠ M3: First Service Migration (Week 6) - DELAYED (now Week 7)
⏳ M4: Integration Testing (Week 10) - ON TRACK

Schedule Performance Index (SPI): 0.88 (12% behind)

Risks identified:
- Service 1 migration took 50% longer than estimated
- Database schema complexity underestimated
- Team member on leave next week

Recommended actions:
1. Add one additional backend developer for 3 weeks
2. Adjust M4 timeline to Week 11 (1-week buffer maintained)
3. Prioritize critical services only for remaining timeline
4. Daily sync on Service 2 migration (starting next week)"
```

### Example 3: Resource Allocation
```
User: "/resource-allocate for next sprint with 3 concurrent projects"

Agent: "Resource Allocation Analysis

Current Capacity: 200 hours/week (5 developers × 40 hours)
Current Demand: 245 hours/week (23% over-allocated)

Over-allocated resources:
- Sarah (Backend): 55h assigned (38% over)
- Mike (Full-stack): 48h assigned (20% over)

Under-allocated:
- Jessica (Frontend): 28h assigned (30% under)

Recommendations:
1. Move 3 UI tasks from Mike to Jessica (12 hours)
2. Defer Project C Task 7 to next sprint (8 hours)
3. Request contractor support for Sarah (15 hours/week)
4. Implement pair programming on critical backend tasks

Optimized allocation:
✓ All resources at 90-100% capacity
✓ No over-allocation
✓ Critical path maintained
✓ Budget impact: +$3,600 (contractor week)"
```

## Advanced Features

### Integration with Memory
The agent can remember:
- Past project decisions and rationale
- Team preferences and working styles
- Historical estimation accuracy
- Lessons learned from previous projects
- Stakeholder communication preferences

### GitHub Integration
- Automatic milestone creation and tracking
- Issue-based task management
- Pull request timeline impact analysis
- Team velocity calculation from commits
- Sprint burndown visualization

### Reporting
- Executive dashboard generation
- Earned Value Management (EVM) reports
- Resource utilization reports
- Risk heat maps
- Stakeholder-specific status updates

## License

MIT License - See repository for details

## Support

For issues, questions, or contributions:
- Repository: https://github.com/VoltAgent/awesome-claude-code-subagents
- Category: Business & Product (08-business-product)
- Agent: project-manager

## Version History

- **1.0.0** (2025-12-24): Initial release
  - Project planning capabilities
  - Milestone tracking
  - Resource allocation
  - Risk register management
  - Slash commands implementation
  - MCP server integration
