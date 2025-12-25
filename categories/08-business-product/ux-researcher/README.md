# UX Researcher Agent

Expert UX researcher specializing in user insights, usability testing, and data-driven design decisions. Masters qualitative and quantitative research methods to uncover user needs, validate designs, and drive product improvements through actionable insights.

## Overview

The UX Researcher agent is a senior-level specialist focused on uncovering deep user insights through mixed-methods research. This agent excels at user interviews, usability testing, behavioral analytics, persona development, and journey mapping to drive meaningful product improvements.

## Key Capabilities

### Research Methods
- **User Interviews**: Contextual inquiry, in-depth interviews, screening, and recruitment
- **Usability Testing**: Moderated and unmoderated testing, task design, observation protocols
- **Survey Design**: Question formulation, response scales, logic branching, statistical validation
- **Analytics Interpretation**: Behavioral patterns, conversion funnels, user flows, cohort analysis
- **Persona Development**: User segmentation, behavioral patterns, goal mapping, pain point analysis
- **Journey Mapping**: Touchpoint identification, emotion mapping, service blueprints, experience metrics
- **A/B Testing**: Hypothesis formulation, test design, statistical significance, result interpretation
- **Accessibility Research**: WCAG compliance, assistive technology testing, inclusive design
- **Competitive Analysis**: Feature comparison, user flow analysis, design patterns, benchmarking

### Advanced Techniques
- Contextual inquiry and ethnographic research
- Diary studies and longitudinal research
- Card sorting and tree testing
- Eye tracking and biometric testing
- Participatory design workshops
- Qualitative coding and thematic analysis
- Statistical and sentiment analysis
- Data triangulation and synthesis

## Setup

### Prerequisites
- Node.js installed
- GitHub account (optional, for collaboration)
- Access to MCP-compatible Claude environment

### Installation

1. Copy the agent directory to your Claude Code agents folder
2. Install the agent using Claude Code:
   ```
   Load the ux-researcher agent
   ```

### MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read/write research documents, interview guides, and reports
- **github**: Track research findings, collaborate on design documentation
- **memory**: Maintain context about user insights, personas, and research history
- **fetch**: Retrieve web content for competitive analysis and research

### Environment Variables

Optional:
- `GITHUB_TOKEN`: GitHub personal access token for collaboration and documentation tracking

## Usage

### Basic Invocation

Simply invoke the agent with your research needs:

```
@ux-researcher Plan user interviews to understand onboarding pain points
```

### Slash Commands

The agent provides specialized slash commands for common research tasks:

#### `/user-interview`
Create comprehensive user interview guide and recruitment plan.

```
@ux-researcher /user-interview Create interview guide for e-commerce checkout experience
```

Outputs:
- Research objectives and questions
- Participant screening criteria
- Interview guide with questions
- Recruitment plan
- Consent and recording setup

#### `/usability-test`
Design usability test protocol and tasks.

```
@ux-researcher /usability-test Design usability test for new dashboard
```

Outputs:
- Test plan and objectives
- Task scenarios
- Success metrics
- Observation guide
- Data collection template

#### `/persona-create`
Develop user personas from research data.

```
@ux-researcher /persona-create Build personas from customer interviews
```

Outputs:
- User segments
- Detailed persona profiles
- Goals and motivations
- Pain points and needs
- Behavioral patterns
- Scenario examples

#### `/journey-map`
Build customer journey map with touchpoints.

```
@ux-researcher /journey-map Map customer journey for subscription signup
```

Outputs:
- Journey stages
- Touchpoint inventory
- Emotion mapping
- Pain point identification
- Opportunity areas
- Service blueprint

## Workflow

### 1. Research Planning
The agent starts by understanding your research objectives:
- Defines research questions
- Identifies user segments
- Selects appropriate methodologies
- Plans timeline and resources
- Sets success criteria

### 2. Implementation Phase
Conducts research systematically:
- Recruits participants
- Conducts sessions (interviews, tests, surveys)
- Collects data rigorously
- Analyzes findings objectively
- Synthesizes insights
- Generates recommendations
- Creates deliverables

### 3. Impact Excellence
Ensures research drives improvements:
- Validates findings through triangulation
- Controls for bias
- Measures impact quantitatively
- Aligns stakeholders
- Communicates clearly

## Examples

### Example 1: User Interview Study

```
@ux-researcher I need to understand why users abandon our checkout process. Plan and conduct user interviews.
```

The agent will:
1. Review existing analytics data
2. Create interview guide focused on checkout experience
3. Define screening criteria and recruit 8-12 participants
4. Conduct in-depth interviews
5. Analyze responses and identify patterns
6. Deliver actionable insights with recommendations

### Example 2: Usability Testing

```
@ux-researcher Run moderated usability tests on our redesigned mobile app with 10 users
```

The agent will:
1. Design test protocol with 5-7 tasks
2. Prepare testing materials and environment
3. Recruit representative participants
4. Conduct moderated sessions
5. Collect quantitative and qualitative data
6. Analyze results and provide prioritized recommendations

### Example 3: Persona Development

```
@ux-researcher Create user personas based on our recent customer research
```

The agent will:
1. Analyze interview transcripts, survey data, and analytics
2. Identify distinct user segments
3. Develop 3-5 detailed personas
4. Include demographics, goals, pain points, and behaviors
5. Validate personas with stakeholders
6. Create persona cards for team reference

### Example 4: Journey Mapping

```
@ux-researcher Map the end-to-end customer journey for our SaaS onboarding
```

The agent will:
1. Identify all customer touchpoints
2. Map emotional states at each stage
3. Highlight pain points and friction
4. Discover opportunity areas
5. Create service blueprint
6. Define experience metrics

## Quality Standards

The UX Researcher maintains high research quality:

- **Sample Size**: Adequate participant numbers for statistical validity
- **Bias Control**: Systematic minimization of researcher and selection bias
- **Actionability**: Insights directly applicable to design decisions
- **Triangulation**: Multiple data sources validate findings
- **Validation**: Findings verified through multiple methods
- **Clarity**: Recommendations clear and prioritized
- **Impact Measurement**: Quantitative metrics track improvements
- **Stakeholder Alignment**: Team buy-in and shared understanding

## Deliverables

The agent produces comprehensive research deliverables:

- Executive summaries for stakeholders
- Detailed research reports
- Video highlights from sessions
- Journey maps and service blueprints
- Persona cards and profiles
- Design principles and guidelines
- Opportunity maps
- Recommendation matrices with prioritization

## Integration with Other Agents

The UX Researcher collaborates effectively:

- **product-manager**: Align on priorities and success metrics
- **ux-designer**: Translate insights into design solutions
- **frontend-developer**: Support implementation with user context
- **content-marketer**: Guide messaging based on user language
- **customer-success-manager**: Incorporate support feedback
- **business-analyst**: Connect research to business metrics
- **data-analyst**: Combine qualitative and quantitative insights
- **scrum-master**: Integrate research into sprint planning

## Best Practices

1. **Start with Clear Objectives**: Define what you need to learn before choosing methods
2. **Choose the Right Method**: Match research method to the question (exploratory vs evaluative)
3. **Recruit Thoughtfully**: Ensure participants represent your target users
4. **Remain Objective**: Minimize bias through careful question design and analysis
5. **Triangulate Data**: Validate insights using multiple research methods
6. **Focus on Actionability**: Ensure insights lead to concrete design improvements
7. **Communicate Effectively**: Tailor deliverables to audience (executives vs designers)
8. **Measure Impact**: Track how research influences product decisions and outcomes
9. **Build Continuous Discovery**: Establish ongoing research practice, not one-off studies
10. **Maintain Ethics**: Follow proper consent, privacy, and data handling protocols

## Research Operations

The agent supports research operations:

- Participant database management
- Research repository organization
- Tool and platform management
- Process documentation
- Template libraries
- Ethics and consent protocols
- Legal compliance (GDPR, privacy)
- Knowledge sharing across teams

## Continuous Discovery

Supports ongoing research practice:

- Regular user touchpoints
- Feedback loops with product teams
- Iterative testing cycles
- Trend monitoring and analysis
- Emerging behavior tracking
- Technology impact assessment
- Market change monitoring
- User evolution understanding

## Troubleshooting

### Common Issues

**Issue**: Not enough participants recruited
- **Solution**: Review screening criteria, expand recruitment channels, adjust incentives

**Issue**: Interview responses are superficial
- **Solution**: Use better probes, ask "why" questions, create comfortable environment

**Issue**: Usability test tasks not revealing issues
- **Solution**: Revise task scenarios, use realistic data, adjust difficulty level

**Issue**: Research insights not being used
- **Solution**: Present findings sooner, involve stakeholders early, focus on actionability

## Contributing

This agent is part of the VoltAgent community. Contributions welcome:

1. Suggest new research methods
2. Add new slash commands
3. Improve templates and guides
4. Share case studies and examples

## License

MIT License - See repository for details

## Support

- Repository: https://github.com/VoltAgent/awesome-claude-code-subagents
- Category: Business & Product
- Version: 2.0.0

---

**Remember**: The best UX research combines empathy with rigor, curiosity with objectivity, and insights with action. This agent helps you understand your users deeply and translate that understanding into better product experiences.
