# Product Manager Agent

Expert product manager specializing in product strategy, user-centric development, and business outcomes. Masters roadmap planning, feature prioritization, and cross-functional leadership with focus on delivering products that users love and drive business growth.

## Overview

The Product Manager agent is your strategic partner for building successful products. It combines deep product management expertise with data-driven decision making to help you deliver products that delight users and achieve business objectives.

## Key Features

- **Product Strategy**: Vision development, market analysis, and competitive positioning
- **Roadmap Planning**: Strategic themes, quarterly objectives, and feature prioritization
- **User Research**: User interviews, surveys, usability testing, and analytics analysis
- **Feature Prioritization**: RICE scoring, impact assessment, and value vs complexity analysis
- **Data-Driven Decisions**: Hypothesis formation, experiment design, and impact measurement
- **Cross-Functional Leadership**: Team alignment, stakeholder management, and conflict resolution
- **Go-to-Market Execution**: Launch strategy, marketing coordination, and success metrics
- **Product Lifecycle**: From ideation to launch, growth, iteration, and sunset planning

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read/write product documentation, PRDs, roadmaps, and strategy documents
- **github**: Track product development, manage issues, and review feature implementation
- **memory**: Maintain product context, user feedback, and strategic decisions
- **fetch**: Research market trends, competitive analysis, and user insights

## Setup

### Prerequisites

- Node.js and npx installed
- GitHub personal access token (optional, for GitHub integration)

### Configuration

1. Set up your GitHub token (optional):
   ```bash
   export GITHUB_TOKEN=your_github_personal_access_token
   ```

2. The agent will use the current working directory for filesystem operations.

## Slash Commands

### `/prd-create`
Create comprehensive Product Requirements Document.

**Example:**
```
/prd-create for a new user authentication system with SSO support
```

Creates a detailed PRD including:
- Product overview and objectives
- User stories and use cases
- Functional and non-functional requirements
- Acceptance criteria
- Success metrics
- Technical considerations
- Timeline and milestones

### `/roadmap`
Generate strategic product roadmap.

**Example:**
```
/roadmap for Q1-Q4 focusing on enterprise features and scalability
```

Generates a roadmap with:
- Strategic themes
- Quarterly objectives
- Feature timeline
- Resource allocation
- Dependencies
- Risk assessment
- Business impact

### `/feature-prioritize`
Prioritize features using RICE framework.

**Example:**
```
/feature-prioritize these 10 feature requests from our backlog
```

Analyzes features using:
- Reach (how many users affected)
- Impact (how much it moves the needle)
- Confidence (certainty in estimates)
- Effort (time and resources required)
- RICE score calculation
- Prioritized recommendations

### `/metrics-define`
Define success metrics and tracking plan.

**Example:**
```
/metrics-define for our new mobile app launch
```

Creates metrics framework including:
- North Star metric
- Key performance indicators (KPIs)
- Leading and lagging indicators
- Tracking implementation plan
- Dashboard requirements
- Success criteria

## Usage Examples

### Example 1: Create Product Roadmap

```
Create a Q1-Q4 product roadmap for our SaaS platform. We want to focus on
enterprise features, scalability improvements, and international expansion.
```

The agent will:
1. Analyze current product state and market position
2. Define strategic themes for each quarter
3. Prioritize features based on business impact
4. Map dependencies and resource requirements
5. Generate comprehensive roadmap with timelines

### Example 2: Feature Prioritization

```
Help me prioritize these feature requests:
1. Dark mode UI
2. SSO authentication
3. Mobile app
4. API rate limiting
5. Advanced reporting
6. Slack integration
7. Custom branding
8. Multi-language support
9. Offline mode
10. Real-time collaboration
```

The agent will:
1. Apply RICE framework to each feature
2. Assess user impact and business value
3. Estimate development effort
4. Consider technical feasibility
5. Provide prioritized recommendations with scores

### Example 3: PRD Creation

```
Write a PRD for a new analytics dashboard that helps users understand
their product usage patterns and user engagement metrics.
```

The agent will create:
1. Executive summary and objectives
2. User personas and use cases
3. Detailed feature requirements
4. User stories with acceptance criteria
5. Success metrics and KPIs
6. Technical considerations
7. Launch plan and timeline

## Product Management Frameworks

The agent is expert in these frameworks:

- **RICE Prioritization**: Reach × Impact × Confidence ÷ Effort
- **Jobs to be Done (JTBD)**: Understanding user motivation and context
- **Design Thinking**: Empathize, Define, Ideate, Prototype, Test
- **Lean Startup**: Build-Measure-Learn cycles
- **OKRs**: Objectives and Key Results alignment
- **North Star Metrics**: Single metric that best captures core value
- **Kano Model**: Understanding feature satisfaction and delight

## Workflow

When invoked, the agent follows this workflow:

1. **Context Analysis**: Query product vision, market context, and user feedback
2. **Research**: Review analytics data, competitive landscape, and user insights
3. **Opportunity Assessment**: Analyze user needs and business impact
4. **Decision Making**: Balance user value with business goals
5. **Documentation**: Create clear, actionable product documents
6. **Tracking**: Define metrics and success criteria

## Quality Standards

The agent ensures:

- User satisfaction > 80%
- Feature adoption tracked thoroughly
- Business metrics achieved consistently
- Roadmap updated quarterly
- Backlog prioritized strategically
- Analytics implemented comprehensively
- Feedback loops active continuously
- Market position strong and measurable

## Collaboration

The Product Manager agent collaborates with:

- **ux-researcher**: User insights and usability testing
- **business-analyst**: Requirements analysis and documentation
- **data-analyst**: Metrics tracking and analytics
- **scrum-master**: Sprint planning and delivery coordination
- **sales-engineer**: Product demos and customer feedback
- **customer-success-manager**: User adoption and satisfaction
- **engineering teams**: Technical feasibility and implementation

## Best Practices

1. **User-Centric**: Always start with user needs and pain points
2. **Data-Driven**: Base decisions on data, not assumptions
3. **Iterative**: Launch, learn, iterate continuously
4. **Collaborative**: Align stakeholders early and often
5. **Strategic**: Connect features to business objectives
6. **Measurable**: Define clear success metrics upfront
7. **Transparent**: Communicate decisions and rationale clearly

## Tips for Effective Use

1. **Provide Context**: Share product vision, target users, and business goals
2. **Be Specific**: Clear requirements lead to better recommendations
3. **Share Data**: Include analytics, user feedback, and market research
4. **Ask Questions**: The agent can help clarify ambiguous requirements
5. **Iterate**: Start with MVP, gather feedback, refine continuously

## Troubleshooting

### GitHub Integration Issues
- Ensure `GITHUB_TOKEN` is set correctly
- Verify token has appropriate repository permissions

### Context Memory
- The memory server maintains product context across sessions
- Clear memory if you need to start fresh with a new product

## Contributing

This agent is part of the VoltAgent Community marketplace. Contributions and feedback are welcome at the [GitHub repository](https://github.com/VoltAgent/awesome-claude-code-subagents).

## License

MIT License - See repository for details.
