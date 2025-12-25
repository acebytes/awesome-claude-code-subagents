# Agent Organizer

Expert agent organizer specializing in multi-agent orchestration, team assembly, and workflow optimization. Masters task decomposition, agent selection, and coordination strategies with focus on achieving optimal team performance and resource utilization.

## Overview

The Agent Organizer is a specialized agent designed to coordinate and optimize multi-agent teams. It excels at analyzing complex tasks, selecting the right agents for each job, designing efficient workflows, and ensuring seamless collaboration across distributed agent systems. Whether you're orchestrating a simple two-agent collaboration or managing a complex multi-phase project with dozens of agents, the Agent Organizer ensures optimal performance and resource utilization.

## Key Capabilities

- **Task Decomposition**: Break down complex tasks into manageable subtasks with clear dependencies
- **Agent Selection**: Match agent capabilities to task requirements with >95% accuracy
- **Team Assembly**: Build optimal agent teams with complementary skills and efficient communication
- **Workflow Design**: Create efficient multi-agent workflows using proven orchestration patterns
- **Performance Optimization**: Monitor and optimize team performance in real-time
- **Resource Management**: Balance workload and minimize costs while maximizing throughput
- **Failure Recovery**: Implement automatic error recovery and failover strategies
- **Continuous Learning**: Learn from each orchestration to improve future team assemblies

## Quick Start

### Prerequisites

- Node.js 18 or higher
- npm or npx installed
- GitHub Personal Access Token (for agent repository access)

### Installation

1. Set up your GitHub token:
```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

2. The agent will automatically install required MCP servers on first use:
   - `@modelcontextprotocol/server-filesystem` - For reading/writing orchestration artifacts
   - `@modelcontextprotocol/server-github` - For accessing agent repositories
   - `@modelcontextprotocol/server-memory` - For remembering successful patterns

### Basic Usage

Invoke the Agent Organizer in your Claude Code session:

```
Load the agent-organizer agent to help me coordinate multiple agents for this project
```

## Slash Commands

### `/organize-agents` - Organize Agent Team

Analyze a task and assemble the optimal agent team with roles, workflow, and monitoring.

```bash
/organize-agents Build a real-time chat application with React frontend and Node.js backend
```

**What it does**:
1. Parses task requirements and complexity
2. Queries available agents and capabilities
3. Selects optimal team composition (e.g., react-specialist, backend-developer, database-optimizer)
4. Assigns clear roles and responsibilities
5. Designs coordination workflow
6. Sets up monitoring and checkpoints
7. Returns complete team configuration

**Output**: Team composition, workflow diagram, coordination plan, monitoring setup

### `/agent-matrix` - Capability Matrix

Generate a capability matrix of available agents with compatibility analysis.

```bash
/agent-matrix frontend
```

**What it does**:
1. Queries all available agents (optionally filtered)
2. Extracts capability information
3. Builds skills matrix
4. Analyzes compatibility patterns
5. Identifies capability gaps
6. Suggests optimal team combinations

**Output**: Visual capability matrix, compatibility scores, team recommendations

### `/team-assemble` - Constrained Team Assembly

Assemble an agent team with specific budget, time, and skill constraints.

```bash
/team-assemble --budget 500 --time "2 weeks" --skills "API development, database design, security"
```

**What it does**:
1. Parses constraints (budget, time, required skills)
2. Filters agents meeting all constraints
3. Optimizes for cost and performance
4. Scores candidate team compositions
5. Selects optimal team
6. Validates against constraints

**Output**: Optimal team with cost breakdown, timeline, skill coverage analysis

### `/workflow-design` - Workflow Designer

Design an efficient multi-agent workflow with orchestration patterns.

```bash
/workflow-design "Process customer orders" --pattern pipeline
```

**What it does**:
1. Analyzes task structure and dependencies
2. Applies selected orchestration pattern (sequential, parallel, pipeline, map-reduce, etc.)
3. Designs data flow between agents
4. Defines coordination and synchronization points
5. Adds error handling paths
6. Inserts monitoring checkpoints
7. Plans result aggregation strategy

**Output**: Workflow diagram, coordination protocol, error handling plan, monitoring points

## Orchestration Patterns

The Agent Organizer supports multiple proven orchestration patterns:

### Sequential Execution
Tasks executed one after another. Best for dependent tasks.
```
Agent A → Agent B → Agent C → Result
```

### Parallel Processing
Multiple tasks executed simultaneously. Best for independent tasks.
```
Agent A ↘
Agent B → Aggregator → Result
Agent C ↗
```

### Pipeline Pattern
Data flows through sequential stages. Best for transformation workflows.
```
Input → Stage 1 → Stage 2 → Stage 3 → Output
```

### Map-Reduce
Distribute work, process in parallel, aggregate results. Best for large datasets.
```
Data → Mapper (distribute) → Workers (parallel) → Reducer (aggregate) → Result
```

### Event-Driven
Agents react to events. Best for asynchronous workflows.
```
Event → Handler → Multiple Agents (reactive) → Event Bus
```

### Hierarchical Delegation
Tree-like command structure. Best for complex multi-level tasks.
```
Master Agent → Sub-coordinators → Worker Agents → Results
```

## Configuration

### MCP Servers

The agent uses three MCP servers configured in `mcp-config.json`:

**filesystem** - Local file operations
- Read agent capability files
- Write team composition plans
- Edit workflow configurations
- Store orchestration results

**github** - Agent repository access
- Browse agent implementations
- Review team patterns
- Study successful orchestrations
- Track agent versions

Requires: `GITHUB_PERSONAL_ACCESS_TOKEN` environment variable

**memory** - Pattern learning and recall
- Store successful team compositions
- Recall agent performance data
- Track optimization strategies
- Learn from past orchestrations

### Environment Variables

```bash
# Required
export GITHUB_TOKEN="ghp_your_token_here"

# Optional - customize MCP server paths if needed
export MCP_FILESYSTEM_PATH="/custom/path"
```

## Use Cases

### 1. Complex Application Development

**Scenario**: Build a full-stack e-commerce platform

```
/organize-agents Build an e-commerce platform with React frontend, Node.js API, PostgreSQL database, payment integration, and deployment
```

**Result**: Team of 8-12 agents including:
- frontend-developer (React UI)
- backend-developer (Node.js API)
- postgres-pro (Database design)
- security-engineer (Payment security)
- devops-engineer (Deployment)
- test-automator (Testing)
- documentation-engineer (Docs)

### 2. Performance Optimization

**Scenario**: Optimize slow application performance

```
/organize-agents Optimize application performance - current response time is 3s, target is <500ms
```

**Result**: Specialized team:
- performance-engineer (Analysis & optimization)
- database-optimizer (Query optimization)
- code-reviewer (Code analysis)
- monitoring setup and bottleneck identification plan

### 3. Large-Scale Data Processing

**Scenario**: Process 1 million records through validation and transformation

```
/workflow-design "Process 1M customer records through validation, enrichment, and storage" --pattern map-reduce
```

**Result**: Map-reduce workflow with:
- Data partitioning strategy
- Parallel processing agents
- Validation and transformation logic
- Result aggregation and storage
- Error handling and retry logic

### 4. Microservices Migration

**Scenario**: Migrate monolithic app to microservices

```
/organize-agents Migrate our monolithic Rails application to microservices architecture
```

**Result**: Multi-phase orchestration:
- Phase 1: Analysis (architect-reviewer, code-analyzer)
- Phase 2: Service extraction (backend-developer, api-designer)
- Phase 3: Database splitting (postgres-pro, data-engineer)
- Phase 4: Deployment (devops-engineer, kubernetes-specialist)
- Phase 5: Testing (qa-expert, performance-engineer)

### 5. Budget-Constrained Projects

**Scenario**: Small project with tight budget

```
/team-assemble --budget 200 --time "1 week" --skills "full-stack development, basic security"
```

**Result**: Minimal but effective team:
- fullstack-developer (core development)
- security-auditor (basic security review)
- Resource-optimized workflow
- Clear deliverables within constraints

## Performance Metrics

The Agent Organizer tracks and optimizes these key metrics:

- **Agent Selection Accuracy**: >95% (right agent for the task)
- **Task Completion Rate**: >99% (successful task completion)
- **Average Response Time**: <5s (agent assignment latency)
- **Resource Utilization**: 60-80% optimal range
- **Error Recovery Time**: <30s (automatic failover)
- **Cost Efficiency**: Tracked per orchestration
- **Team Synergy**: Measured by coordination overhead

## Best Practices

### 1. Clear Task Definition
Be specific about requirements, constraints, and success criteria.

**Good**: "Build a REST API with authentication, rate limiting, and PostgreSQL storage, deployed on AWS"

**Bad**: "Make an API"

### 2. Use Appropriate Patterns
Match orchestration pattern to task characteristics:
- Sequential: Strongly dependent tasks
- Parallel: Independent tasks with same deadline
- Pipeline: Multi-stage transformations
- Map-Reduce: Large-scale data processing

### 3. Plan for Failure
Always include error handling and backup agents in critical paths.

### 4. Monitor Performance
Use built-in monitoring to detect and resolve bottlenecks early.

### 5. Learn from History
Review past orchestrations to improve future team assemblies.

## Troubleshooting

### Issue: Agent selection seems suboptimal

**Solution**: Ensure agent capability files are up-to-date and provide detailed task requirements.

```bash
/agent-matrix  # Review current capabilities
# Then refine your task description
```

### Issue: Team coordination overhead too high

**Solution**: Simplify team structure or use different orchestration pattern.

```bash
/workflow-design "your task" --pattern sequential  # Try simpler pattern
```

### Issue: Resource constraints causing failures

**Solution**: Use constrained team assembly to stay within limits.

```bash
/team-assemble --budget <limit> --skills "required skills only"
```

### Issue: Task completion taking too long

**Solution**: Analyze for bottlenecks and rebalance workload.

```
Ask agent to monitor current orchestration and identify bottlenecks
Rebalance team based on analysis
```

## Integration with Other Agents

The Agent Organizer collaborates effectively with:

- **context-manager**: Share information and context across agents
- **multi-agent-coordinator**: Execute coordinated multi-agent tasks
- **task-distributor**: Distribute workload across agent teams
- **workflow-orchestrator**: Design and execute complex process flows
- **performance-monitor**: Track team and individual agent metrics
- **error-coordinator**: Handle failures and implement recovery strategies
- **knowledge-synthesizer**: Capture and apply orchestration learnings

## Advanced Features

### Dynamic Rebalancing

The Agent Organizer can detect bottlenecks and rebalance teams in real-time:

```
Monitor my current agent team and rebalance if you detect any bottlenecks
```

### Learning from History

Successful orchestrations are stored in memory for future reference:

```
What team composition worked best for similar API development projects?
```

### Custom Orchestration Patterns

Define custom patterns for specific use cases:

```
Design a custom orchestration pattern for our CI/CD pipeline with 5 test stages
```

### Cost Optimization

Minimize costs while maintaining performance:

```
Optimize the current team composition to reduce costs by 30% without impacting delivery time
```

## Examples

### Example 1: Simple Web Application

```
/organize-agents Create a simple blog application with user authentication
```

**Output**:
- Team: frontend-developer, backend-developer, postgres-pro
- Pattern: Sequential execution
- Timeline: 3-5 days
- Cost estimate: Medium

### Example 2: Data Pipeline

```
/workflow-design "ETL pipeline for customer analytics" --pattern pipeline
```

**Output**:
- Stage 1: Extract (data-engineer)
- Stage 2: Transform (data-analyst)
- Stage 3: Load (postgres-pro)
- Stage 4: Visualize (frontend-developer)
- Checkpoints after each stage

### Example 3: Capability Analysis

```
/agent-matrix security
```

**Output**:
```
Security-Related Agents:
- security-engineer: 95% match (penetration testing, OWASP, vulnerability assessment)
- security-auditor: 90% match (compliance, security reviews, audit trails)
- penetration-tester: 85% match (exploit testing, security scanning)

Recommended Teams:
1. security-engineer + security-auditor (comprehensive security)
2. penetration-tester + security-engineer (offensive + defensive)
```

## Support

For issues, questions, or contributions:
- GitHub: https://github.com/VoltAgent/claude-code-agent-marketplace
- Category: 09-meta-orchestration
- Agent: agent-organizer

## License

MIT License - See repository for full details

## Version History

- **1.0.0** (2025-12-24): Initial release with core orchestration capabilities
  - Task decomposition and analysis
  - Agent capability mapping
  - Team assembly optimization
  - Workflow design with multiple patterns
  - Real-time monitoring and adaptation
  - Four slash commands for common operations
