# Scrum Master Agent

Expert Scrum Master specializing in agile transformation, team facilitation, and continuous improvement. Masters Scrum framework implementation, impediment removal, and fostering high-performing, self-organizing teams that deliver value consistently.

## Overview

This agent serves as a certified Scrum Master with expertise in facilitating agile teams, removing impediments, and driving continuous improvement. It focuses on team dynamics, process optimization, and stakeholder management with emphasis on creating psychological safety, enabling self-organization, and maximizing value delivery through the Scrum framework.

## Key Capabilities

- **Sprint Planning & Facilitation**: Capacity planning, story estimation, sprint goal setting, and commitment protocols
- **Daily Standup Management**: Time-box enforcement, impediment capture, and collaboration fostering
- **Sprint Review Coordination**: Demo preparation, stakeholder management, and feedback collection
- **Retrospective Facilitation**: Safe space creation, root cause analysis, and action item generation
- **Backlog Refinement**: Story breakdown, acceptance criteria, and estimation sessions
- **Impediment Removal**: Blocker identification, escalation paths, and resolution tracking
- **Team Coaching**: Self-organization, conflict resolution, and continuous learning
- **Metrics Tracking**: Velocity trends, burndown charts, cycle time, and team happiness
- **Stakeholder Management**: Expectation setting, transparency practices, and executive reporting
- **Agile Transformation**: Maturity assessment, change management, and scaling frameworks

## Installation

1. Copy the `scrum-master` directory to your Claude Code agents location
2. Install required MCP servers (they will be installed automatically on first use):
   - `@modelcontextprotocol/server-filesystem`
   - `@modelcontextprotocol/server-github`
   - `@modelcontextprotocol/server-memory`

## Configuration

### Environment Variables

Set up the following environment variable for full functionality:

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

The GitHub token is optional but recommended for repository access and issue tracking.

### MCP Servers

The agent uses three MCP servers:

1. **Filesystem**: Access to local project files for documentation and tracking
2. **GitHub**: Repository access for issue tracking and project management
3. **Memory**: Persistent storage for team metrics, impediments, and historical data

## Usage

### Slash Commands

The agent provides four specialized slash commands:

#### `/sprint-plan`
Plan the upcoming sprint with comprehensive preparation:
- Capacity planning and resource allocation
- Story estimation using planning poker
- Sprint goal setting and alignment
- Commitment protocols and team agreement
- Risk identification and mitigation
- Dependency mapping across teams
- Task breakdown and assignment
- Definition of done clarification

Example:
```
/sprint-plan
```

#### `/retro-facilitate`
Facilitate an effective retrospective session:
- Create a safe space for open discussion
- Use varied formats (Start-Stop-Continue, 4Ls, etc.)
- Perform root cause analysis on issues
- Generate actionable improvement items
- Track follow-through on previous actions
- Check team health and morale
- Celebrate successes and wins
- Document improvement metrics

Example:
```
/retro-facilitate
```

#### `/velocity-track`
Track and analyze team performance metrics:
- Velocity trends over multiple sprints
- Burndown and burnup charts
- Cycle time and lead time analysis
- Sprint predictability scoring
- Defect rate tracking
- Team happiness metrics
- Business value delivered
- Capacity utilization

Example:
```
/velocity-track
```

#### `/impediment-log`
Log and manage team impediments:
- Document new blockers and impediments
- Track resolution progress and ownership
- Identify escalation paths
- Monitor resolution time metrics
- Implement preventive measures
- Categorize impediment types
- Generate impediment reports
- Track patterns and recurring issues

Example:
```
/impediment-log "Database performance issues blocking feature development"
```

## Workflow

### Initial Team Assessment

When first invoked, the agent will:
1. Query for team structure and composition
2. Review existing processes and ceremonies
3. Analyze current velocity and metrics
4. Assess agile maturity level
5. Identify pain points and improvement opportunities

### Ongoing Facilitation

The agent supports the complete Scrum cycle:

1. **Sprint Planning**
   - Facilitate capacity planning
   - Guide estimation sessions
   - Help set meaningful sprint goals
   - Ensure commitment and alignment

2. **Daily Standups**
   - Maintain time-box discipline
   - Capture impediments and blockers
   - Foster team collaboration
   - Identify patterns and risks

3. **Sprint Review**
   - Coordinate demo preparation
   - Manage stakeholder engagement
   - Collect and document feedback
   - Celebrate achievements

4. **Retrospective**
   - Create psychological safety
   - Facilitate root cause analysis
   - Generate improvement actions
   - Track team health metrics

5. **Backlog Refinement**
   - Guide story breakdown
   - Clarify acceptance criteria
   - Facilitate estimation
   - Identify dependencies

### Impediment Management

The agent maintains a systematic approach to impediments:
- Immediate identification and logging
- Clear ownership and escalation
- Resolution time tracking (target < 48h)
- Pattern analysis and prevention
- Regular status updates

### Metrics and Reporting

Track key performance indicators:
- Sprint velocity (target: stable and predictable)
- Team happiness (target: > 8/10)
- Impediment resolution time (target: < 48h)
- Sprint predictability (target: > 90%)
- Burndown health (target: consistent)
- Quality metrics (defect rates)

## Integration with Other Agents

The Scrum Master agent collaborates with:

- **product-manager**: Backlog prioritization and product vision
- **project-manager**: Delivery coordination and timeline management
- **qa-expert**: Quality metrics and testing processes
- **business-analyst**: Requirements clarification and story refinement
- **ux-researcher**: User feedback integration and validation
- **technical-writer**: Documentation standards and sprint reviews
- **devops-engineer**: Deployment processes and technical impediments

## Best Practices

### Team Empowerment
- Foster self-organization and autonomy
- Enable cross-functional collaboration
- Build psychological safety
- Encourage continuous learning

### Process Optimization
- Keep ceremonies time-boxed and effective
- Adapt processes to team needs
- Maintain focus on value delivery
- Remove unnecessary overhead

### Continuous Improvement
- Celebrate experiments and learning
- Track improvement metrics
- Share best practices
- Build a culture of excellence

### Stakeholder Management
- Maintain transparency and visibility
- Set realistic expectations
- Provide regular updates
- Build trust and partnerships

## Example Scenarios

### Scenario 1: New Team Formation
```
I need help setting up Scrum practices for a new development team of 7 people
working on a SaaS product. They have basic agile knowledge but no Scrum experience.
```

The agent will:
- Assess team composition and skills
- Establish foundational ceremonies
- Set up basic metrics tracking
- Create initial sprint cadence
- Coach on Scrum fundamentals

### Scenario 2: Velocity Improvement
```
Our team's velocity has been declining for the past 3 sprints. Can you help
analyze the issue and create an improvement plan?
```

The agent will:
- Analyze velocity trends and patterns
- Review sprint retrospective data
- Identify root causes
- Assess impediment resolution times
- Create actionable improvement plan
- Set up tracking for progress

### Scenario 3: Remote Team Facilitation
```
We're transitioning to a fully remote team. How should we adapt our Scrum
ceremonies for virtual collaboration?
```

The agent will:
- Recommend virtual facilitation tools
- Adapt ceremony formats for remote
- Establish communication protocols
- Set up engagement techniques
- Plan team bonding activities
- Monitor remote team health

## Scrum Mastery Checklist

Use this checklist to ensure Scrum excellence:

- [ ] Sprint velocity stable and predictable
- [ ] Team satisfaction score > 8/10
- [ ] Impediments resolved in < 48h
- [ ] All ceremonies effective and valued
- [ ] Burndown charts healthy
- [ ] Quality standards consistently met
- [ ] Delivery predictable (> 90%)
- [ ] Continuous improvement active
- [ ] Team self-organizing effectively
- [ ] Stakeholders satisfied with transparency

## Support and Contributions

For issues, feature requests, or contributions, please visit the [Claude Code Agent Marketplace repository](https://github.com/VoltAgent/claude-code-agent-marketplace).

## License

MIT License - See the main repository for details.
