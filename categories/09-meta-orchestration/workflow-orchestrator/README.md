# Workflow Orchestrator Agent

Expert workflow orchestrator specializing in complex process design, state machine implementation, and business process automation. Masters workflow patterns, error compensation, and transaction management with focus on building reliable, flexible, and observable workflow systems.

## Overview

The Workflow Orchestrator is a specialized AI agent designed to help you design, implement, and manage complex business processes and workflows. It excels at creating reliable, fault-tolerant workflow systems with comprehensive error handling, state management, and monitoring capabilities.

### Key Features

- **Process Modeling**: Design workflows using industry-standard patterns (BPMN, state machines)
- **State Management**: Robust state persistence, versioning, and consistency guarantees
- **Transaction Management**: ACID properties, Saga patterns, two-phase commit
- **Error Handling**: Comprehensive retry strategies, compensation flows, and circuit breakers
- **Event Orchestration**: Event sourcing, correlation, and event-driven workflows
- **Human Tasks**: Approval workflows, task assignment, escalation, and SLA tracking
- **Monitoring**: Real-time metrics, performance analytics, and audit trails

## Installation

### Prerequisites

- Node.js 18+ installed
- Git access (for GitHub integration)
- Environment variables configured:
  - `GITHUB_TOKEN`: GitHub personal access token (for GitHub integration)

### Setup

1. Copy the agent directory to your Claude Code agents folder:
```bash
cp -r workflow-orchestrator ~/.config/claude-code/agents/
```

2. Set up environment variables:
```bash
export GITHUB_TOKEN="your_github_token_here"
```

3. The agent will automatically install required MCP servers on first use:
   - `@modelcontextprotocol/server-filesystem`
   - `@modelcontextprotocol/server-github`
   - `@modelcontextprotocol/server-memory`

## Usage

### Basic Workflow

1. **Start the agent** in Claude Code
2. **Describe your process** requirements
3. **Let the agent design** the workflow architecture
4. **Review and refine** the workflow design
5. **Implement** the workflow with agent assistance
6. **Monitor and optimize** using built-in observability

### Slash Commands

#### `/workflow-create`

Create a new workflow definition with states, transitions, and error handling.

```
/workflow-create order-processing "Process customer orders from submission to fulfillment"
```

**What it does:**
- Analyzes workflow requirements
- Defines states and transitions
- Configures error handling and compensation
- Sets up monitoring and observability
- Creates workflow definition file
- Validates configuration
- Documents design decisions

#### `/workflow-execute`

Execute a workflow instance with provided input parameters.

```
/workflow-execute order-processing {"orderId": "12345", "customerId": "C789"}
```

**What it does:**
- Validates workflow exists
- Parses and validates input parameters
- Initializes workflow instance
- Executes workflow steps
- Handles state transitions
- Monitors execution progress
- Returns results or current status

#### `/workflow-status`

Check the status of running workflow instances.

```
/workflow-status order-processing
/workflow-status order-processing instance-abc123
```

**What it does:**
- Queries workflow instances
- Retrieves current state and progress
- Checks for errors or blocked tasks
- Displays execution timeline
- Shows performance metrics
- Reports SLA compliance
- Provides optimization recommendations

#### `/workflow-rollback`

Rollback a workflow instance to a previous state or execute compensation.

```
/workflow-rollback instance-abc123
/workflow-rollback instance-abc123 checkpoint-5
```

**What it does:**
- Validates instance and checkpoint
- Analyzes current state
- Determines compensation steps
- Executes rollback procedure
- Restores state consistency
- Updates audit logs
- Notifies stakeholders
- Returns rollback status

## Workflow Patterns

The agent implements industry-standard workflow patterns:

### Basic Patterns
- **Sequential Flow**: Linear step-by-step execution
- **Parallel Split/Join**: Concurrent execution with synchronization
- **Exclusive Choice**: Decision-based routing
- **Loops and Iterations**: Repetitive processes

### Advanced Patterns
- **Event-Based Gateway**: Event-driven routing decisions
- **Compensation**: Error recovery and rollback flows
- **Sub-Processes**: Nested workflow execution
- **Time-Based Events**: Scheduled triggers and timeouts

## Transaction Management

### Saga Pattern
The agent implements the Saga pattern for distributed transactions:

```
Order Processing Saga:
1. Reserve Inventory → Compensate: Release Inventory
2. Process Payment → Compensate: Refund Payment
3. Ship Order → Compensate: Cancel Shipment
4. Send Confirmation → Compensate: Send Cancellation
```

### ACID Properties
- **Atomicity**: All-or-nothing execution
- **Consistency**: State invariants maintained
- **Isolation**: Concurrent execution handling
- **Durability**: Persistent state storage

## Error Handling

### Retry Strategies
- Exponential backoff
- Configurable retry limits
- Idempotent operations
- Circuit breakers for failing services

### Compensation Flows
- Automatic rollback on failures
- Partial recovery strategies
- State restoration
- Business continuity planning

## State Management

### State Persistence
- Automatic checkpointing
- Version control for state
- Migration support
- Recovery procedures

### State Transitions
- Validation rules
- Guards and conditions
- Audit logging
- Consistency checks

## Monitoring & Observability

### Metrics Tracked
- **Execution Rate**: Workflows per minute
- **Success Rate**: Percentage of successful completions
- **Average Duration**: Mean execution time
- **Active Workflows**: Currently running instances
- **Error Rate**: Failures and exceptions
- **SLA Compliance**: Meeting service level agreements

### Dashboards
Real-time visualization of:
- Workflow execution status
- Performance trends
- Error analytics
- Bottleneck detection
- Resource utilization

## Performance Targets

The agent aims to achieve:

| Metric | Target |
|--------|--------|
| Reliability | > 99.9% |
| State Consistency | 100% |
| Recovery Time | < 30 seconds |
| Execution Rate | 1.2K workflows/min |
| Success Rate | > 99% |

## Integration with Other Agents

The Workflow Orchestrator collaborates with:

- **agent-organizer**: Process task organization
- **multi-agent-coordinator**: Distributed workflow execution
- **task-distributor**: Work allocation and load balancing
- **context-manager**: Process state and context
- **performance-monitor**: Performance metrics and optimization
- **error-coordinator**: Error recovery and compensation
- **knowledge-synthesizer**: Pattern recognition and best practices

## Use Cases

### Business Process Automation
- Order processing and fulfillment
- Customer onboarding workflows
- Invoice processing and approvals
- Contract review and signing

### Technical Workflows
- Data pipeline orchestration
- Microservice coordination
- CI/CD pipeline management
- Infrastructure provisioning

### Human-in-the-Loop
- Approval workflows
- Multi-stage reviews
- Escalation processes
- Task assignment and delegation

### Event-Driven Processes
- Real-time event processing
- Complex event correlation
- Scheduled batch processing
- Reactive workflows

## Examples

### Example 1: Order Processing Workflow

```markdown
Design an order processing workflow that:
1. Validates order details
2. Checks inventory availability
3. Processes payment
4. Creates shipment
5. Sends confirmation

Include error handling for:
- Invalid orders
- Insufficient inventory
- Payment failures
- Shipment issues
```

The agent will:
- Create state machine diagram
- Define states: OrderReceived, InventoryChecked, PaymentProcessed, etc.
- Configure transitions with guards
- Implement compensation flows
- Setup monitoring and alerts

### Example 2: Approval Workflow

```markdown
Create an approval workflow for expense reports:
- Auto-approve amounts < $100
- Manager approval for $100-$1000
- Director approval for $1000-$5000
- CFO approval for > $5000
- Escalate after 48 hours without response
```

The agent will:
- Model approval chains
- Configure routing rules
- Setup escalation timers
- Implement notification system
- Track SLA compliance

### Example 3: Data Pipeline

```markdown
Orchestrate a data processing pipeline:
1. Extract data from multiple sources
2. Transform and clean data
3. Validate data quality
4. Load to data warehouse
5. Generate reports

Handle failures gracefully with retry and compensation.
```

The agent will:
- Design parallel extraction
- Configure transformation steps
- Implement validation rules
- Setup error handling
- Enable progress tracking

## Configuration

### Default Settings

```json
{
  "default_retry_attempts": 3,
  "default_timeout": 300,
  "checkpoint_interval": 60,
  "audit_logging": true,
  "performance_monitoring": true,
  "error_tracking": true
}
```

### Customization

You can customize workflow behavior by:
- Adjusting retry policies
- Configuring timeout values
- Setting checkpoint frequency
- Enabling/disabling features
- Defining custom metrics

## Best Practices

### Design Principles
1. **Design for Failure**: Assume components will fail
2. **Idempotent Operations**: Make operations safe to retry
3. **Clear State Management**: Use explicit state transitions
4. **Comprehensive Logging**: Maintain complete audit trails
5. **Performance Monitoring**: Track all relevant metrics

### Implementation Guidelines
1. **Version Control**: Manage workflow versions
2. **Testing Coverage**: Test all paths and edge cases
3. **Documentation**: Keep documentation up-to-date
4. **Monitoring**: Set up alerts and dashboards
5. **Optimization**: Continuously improve performance

### Operational Excellence
1. **Reliability**: Build fault-tolerant systems
2. **Flexibility**: Design for easy modifications
3. **Observability**: Ensure complete visibility
4. **Compliance**: Meet regulatory requirements
5. **Automation**: Reduce manual intervention

## Troubleshooting

### Common Issues

**Workflow stuck in a state**
- Check for blocking conditions
- Review transition guards
- Examine error logs
- Use `/workflow-status` to inspect

**High failure rate**
- Review error patterns
- Check retry configurations
- Examine compensation flows
- Analyze performance metrics

**Performance degradation**
- Identify bottlenecks
- Review parallel execution
- Check resource utilization
- Optimize critical paths

### Getting Help

1. Use `/workflow-status` for detailed diagnostics
2. Check audit logs for execution history
3. Review performance metrics
4. Consult error analytics
5. Ask the agent for specific guidance

## Advanced Features

### Process Mining
Analyze workflow execution history to:
- Identify optimization opportunities
- Detect process variations
- Find bottlenecks
- Improve efficiency

### Dynamic Routing
Route workflows based on:
- Runtime conditions
- Business rules
- Historical patterns
- Performance metrics

### Multi-Instance Execution
Execute multiple instances:
- Parallel processing
- Sequential processing
- Complex correlations
- Instance management

## Contributing

To extend the Workflow Orchestrator:

1. Add custom workflow patterns
2. Implement domain-specific logic
3. Integrate with external systems
4. Enhance monitoring capabilities
5. Contribute improvements back to the marketplace

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or contributions:
- GitHub Issues: [claude-code-agent-marketplace](https://github.com/anthropics/claude-code-agent-marketplace)
- Documentation: See CLAUDE.md for detailed agent instructions

---

**Version**: 1.0.0
**Category**: Meta Orchestration
**Author**: Claude Code Agent Marketplace
