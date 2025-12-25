# Task Distributor Agent

Expert task distributor specializing in intelligent work allocation, load balancing, and queue management. Masters priority scheduling, capacity tracking, and fair distribution with focus on maximizing throughput while maintaining quality and meeting deadlines.

## Overview

The Task Distributor is a specialized orchestration agent that optimizes work allocation across distributed systems. It implements sophisticated load balancing algorithms, priority scheduling, and queue management to ensure fair, efficient task distribution that maximizes system throughput while meeting service level objectives.

## Key Features

- **Intelligent Task Distribution**: Analyze task characteristics and distribute across agents optimally
- **Load Balancing**: Maintain < 10% variance across agents with dynamic rebalancing
- **Priority Scheduling**: Enforce priorities and deadlines with > 95% success rate
- **Queue Management**: Handle queues, retries, dead letters, and TTLs efficiently
- **Capacity Tracking**: Monitor agent workloads, performance, and resource usage in real-time
- **Performance Optimization**: Achieve > 99% task completion with < 50ms distribution latency
- **Resource Allocation**: Maintain > 80% resource utilization with elastic scaling
- **Routing Intelligence**: Smart matching, fallback chains, and affinity routing

## Installation

1. Clone this agent directory to your local system
2. Ensure you have Node.js installed for MCP servers
3. Set up required environment variables:
   ```bash
   export GITHUB_TOKEN="your-github-token"
   ```

## Usage

### Starting the Agent

Initialize the agent with the MCP configuration:

```bash
claude-code --agent-config task-distributor/
```

The agent will automatically connect to the filesystem, GitHub, and memory MCP servers.

### Slash Commands

#### `/distribute`
Analyze and distribute tasks across available agents.

```
/distribute
```

This command will:
- Analyze pending tasks and their requirements
- Assess agent capacities and current workloads
- Apply intelligent routing algorithms
- Distribute tasks for optimal throughput
- Report distribution metrics

#### `/task-queue`
View and manage task queues and priorities.

```
/task-queue
```

Features:
- Display current queue states
- Show priority levels and ordering
- Monitor TTL and expiration
- Handle dead letter queues
- Configure retry policies

#### `/load-balance`
Check and optimize load balancing across agents.

```
/load-balance
```

Provides:
- Current load distribution across agents
- Balance variance metrics
- Agent health and availability
- Rebalancing recommendations
- Geographic distribution analysis

#### `/capacity-check`
Review agent capacities and resource utilization.

```
/capacity-check
```

Shows:
- Agent workload monitoring
- Performance metrics and efficiency scores
- Resource usage and availability
- Skill mapping and capability matrix
- Utilization targets vs actual

## Distribution Strategies

### Round-Robin
Simple, fair distribution across all available agents in sequence.

### Weighted Distribution
Assign tasks based on agent capacity, performance, or custom weights.

### Least Connections
Route to agents with fewest active tasks for optimal balance.

### Capacity-Based
Match task requirements with agent capabilities and available resources.

### Performance-Based
Route to highest-performing agents while preventing starvation.

### Consistent Hashing
Use hashing for affinity routing and sticky assignments.

## Performance Targets

The Task Distributor maintains the following performance characteristics:

- **Distribution Latency**: < 50ms per task
- **Load Balance Variance**: < 10% across agents
- **Task Completion Rate**: > 99% success
- **Priority Respect**: 100% adherence
- **Deadline Success**: > 95% met on time
- **Resource Utilization**: > 80% efficient
- **Queue Health**: Zero overflow events
- **Fairness**: Continuous balance maintenance

## Queue Management

### Priority Levels
Configure multi-level priority schemes with preemption rules.

### Message Ordering
Maintain FIFO, priority-based, or deadline-driven ordering.

### TTL Handling
Automatic expiration and cleanup of timed-out tasks.

### Dead Letter Queues
Route failed tasks to DLQ for analysis and recovery.

### Retry Mechanisms
Configurable retry policies with exponential backoff.

### Batch Processing
Group similar tasks for efficient parallel execution.

## Integration

The Task Distributor collaborates with other meta-orchestration agents:

- **agent-organizer**: Capacity planning and agent lifecycle
- **multi-agent-coordinator**: Workload distribution strategies
- **workflow-orchestrator**: Task dependency management
- **performance-monitor**: Metrics collection and analysis
- **error-coordinator**: Retry distribution and failure handling
- **context-manager**: State tracking and context sharing
- **knowledge-synthesizer**: Pattern recognition and optimization

## MCP Servers

### Filesystem
Access to local filesystem for queue storage, metrics, and configuration.

### GitHub
Integration with GitHub for task tracking, issue assignment, and collaboration.

### Memory
Persistent storage for distribution state, performance history, and learned patterns.

## Configuration

### Environment Variables

- `GITHUB_TOKEN`: GitHub personal access token for API access
- `PWD`: Working directory for filesystem operations

### Customization

Edit `mcp-config.json` to add additional MCP servers or modify existing configurations.

Edit `CLAUDE.md` to customize distribution algorithms, priority schemes, or performance targets.

## Monitoring

The agent provides real-time monitoring of:

- Queue depths and processing rates
- Distribution latency and throughput
- Agent workloads and health status
- Task completion rates and failures
- Load balance variance and trends
- Resource utilization metrics
- SLA compliance and deadline adherence

## Best Practices

1. **Start with Analysis**: Use `/capacity-check` before distributing tasks
2. **Monitor Continuously**: Regular `/load-balance` checks prevent bottlenecks
3. **Tune for Workload**: Adjust strategies based on task characteristics
4. **Set Clear Priorities**: Define priority schemes aligned with business goals
5. **Plan Capacity**: Use predictive modeling for resource planning
6. **Handle Failures**: Configure robust retry and DLQ policies
7. **Optimize Batches**: Group similar tasks for efficiency gains
8. **Track Metrics**: Use performance data to refine algorithms

## Troubleshooting

### High Distribution Latency
- Check agent capacity and availability
- Review queue depths and backlogs
- Optimize routing algorithms
- Consider scaling resources

### Load Imbalance
- Verify agent health and responsiveness
- Review weight calculations
- Check for affinity routing conflicts
- Enable dynamic rebalancing

### Deadline Misses
- Increase priority for time-sensitive tasks
- Reserve resources for high-priority work
- Reduce batch sizes for faster processing
- Consider preemption rules

### Queue Overflow
- Scale agent capacity
- Implement backpressure mechanisms
- Optimize task processing speed
- Review TTL and cleanup policies

## Contributing

Contributions are welcome! Please submit pull requests or open issues for:

- New distribution algorithms
- Enhanced monitoring capabilities
- Performance optimizations
- Integration improvements
- Documentation updates

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or contributions, visit:
https://github.com/anthropics/claude-code-agent-marketplace
