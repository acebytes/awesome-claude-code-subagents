# Performance Monitor Agent

Expert performance monitor specializing in system-wide metrics collection, analysis, and optimization. Masters real-time monitoring, anomaly detection, and performance insights across distributed agent systems with focus on observability and continuous improvement.

## Overview

The Performance Monitor agent provides comprehensive observability and performance management for multi-agent systems. It collects metrics, detects anomalies, identifies bottlenecks, and delivers actionable insights to maintain system health and optimize performance.

## Key Capabilities

- **Real-time Monitoring**: Live dashboards, streaming metrics, and instant alerts
- **Anomaly Detection**: Statistical and ML-based detection with root cause hints
- **Bottleneck Identification**: Performance profiling, trace analysis, and dependency mapping
- **Trend Analysis**: Long-term patterns, capacity planning, and growth projections
- **Alert Management**: Smart alerting with suppression, routing, and escalation
- **Dashboard Creation**: KPI visualization, service maps, and custom queries
- **Optimization**: Performance tuning recommendations and cost optimization
- **SLO Management**: SLI tracking, error budgets, and reliability reporting

## Performance Metrics

- **Metric Latency**: < 1 second
- **Data Retention**: 90 days
- **Alert Accuracy**: > 95%
- **Dashboard Load Time**: < 2 seconds
- **Anomaly Detection**: < 5 minutes
- **Resource Overhead**: < 2%
- **System Availability**: 99.99%

## Slash Commands

### /perf-monitor
Initialize comprehensive performance monitoring for the system.

**Usage:**
```
/perf-monitor
```

**What it does:**
- Maps system components and topology
- Identifies key metrics to track
- Sets up data collection infrastructure
- Creates baseline measurements
- Configures initial dashboards
- Establishes alert thresholds

### /perf-analyze
Analyze current performance data to identify bottlenecks, anomalies, and optimization opportunities.

**Usage:**
```
/perf-analyze
```

**What it does:**
- Reviews current metrics and trends
- Detects performance anomalies
- Identifies resource bottlenecks
- Analyzes system dependencies
- Generates optimization recommendations
- Highlights cost-saving opportunities

### /perf-alert
Configure and manage alert rules, thresholds, and notification channels.

**Usage:**
```
/perf-alert
```

**What it does:**
- Sets up alert rules and thresholds
- Configures severity levels
- Establishes routing and escalation paths
- Implements suppression rules
- Integrates notification channels
- Tests alert effectiveness

### /perf-report
Generate detailed performance reports with trends, insights, and actionable recommendations.

**Usage:**
```
/perf-report
```

**What it does:**
- Compiles performance metrics over time
- Analyzes trends and patterns
- Highlights critical issues
- Provides optimization recommendations
- Tracks SLO compliance
- Generates executive summaries

## Setup

### Prerequisites

- Node.js and npm installed
- GitHub personal access token (for GitHub integration)

### Environment Variables

Set the following environment variable:

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

### Installation

The agent uses MCP servers that are automatically installed via npx:

- **@modelcontextprotocol/server-filesystem**: File system access for logs and metrics
- **@modelcontextprotocol/server-github**: GitHub integration for issue tracking
- **@modelcontextprotocol/server-memory**: Persistent storage for historical data

## Usage Examples

### Example 1: Initial System Monitoring Setup

```
User: Set up performance monitoring for our multi-agent system

Agent: I'll initialize comprehensive performance monitoring. Let me start by understanding your system architecture and requirements.

[Uses /perf-monitor to:]
1. Query system architecture and agent topology
2. Identify critical metrics (latency, throughput, errors)
3. Set up metric collection with <1s latency
4. Create initial dashboards for key KPIs
5. Establish baseline measurements
6. Configure initial alert rules

Performance monitoring initialized:
- Collecting 2847 metrics across 50 agents
- 23 dashboards created (system overview, agent performance, resource usage)
- 156 alerts configured with 95%+ accuracy
- <1s metric latency achieved
- 90-day retention enabled
```

### Example 2: Bottleneck Investigation

```
User: The system seems slow. Can you identify what's causing the performance issues?

Agent: I'll analyze the current performance data to identify bottlenecks.

[Uses /perf-analyze to:]
1. Review real-time metrics and recent trends
2. Identify CPU and memory hotspots
3. Analyze request latency distributions
4. Map dependency chains
5. Detect resource contention

Analysis complete:
- Bottleneck identified: Database query latency (p95: 850ms)
- Root cause: Missing index on frequently queried table
- Impact: 40% of requests affected, 2.3s avg response time
- Recommendation: Add compound index on (user_id, created_at)
- Expected improvement: Reduce p95 latency to <100ms
- Cost savings: ~$5k/month in reduced compute
```

### Example 3: Anomaly Detection and Alerting

```
User: Configure alerts for unusual system behavior

Agent: I'll set up intelligent alerting with anomaly detection.

[Uses /perf-alert to:]
1. Analyze historical patterns and baselines
2. Configure statistical anomaly detection
3. Set up alert rules with appropriate thresholds
4. Implement alert suppression during deployments
5. Configure routing to on-call teams
6. Test alert accuracy

Alert system configured:
- 47 anomalies detected in historical data
- Alert rules tuned to 97% accuracy
- Escalation paths established (L1 → L2 → L3)
- Notification channels: Slack, PagerDuty, email
- Suppression rules: deployment windows, known issues
- MTTR reduced by 65% with proactive alerting
```

### Example 4: Performance Reporting

```
User: Generate a monthly performance report for stakeholders

Agent: I'll create a comprehensive performance report with trends and insights.

[Uses /perf-report to:]
1. Aggregate metrics for the past 30 days
2. Analyze trends and compare to previous period
3. Calculate SLO compliance
4. Identify optimization opportunities
5. Generate executive summary

Monthly Performance Report:
- System Availability: 99.97% (target: 99.95%)
- Average Response Time: 245ms (down 18% from last month)
- Error Rate: 0.08% (within SLO of <0.1%)
- Throughput: 2.3M requests/day (up 12%)
- Cost per Request: $0.00042 (down 15% via optimization)
- Top Issues: 3 anomalies detected and resolved
- Recommendations: Scale database read replicas, implement caching layer
- Projected Savings: $18k/month with recommended optimizations
```

## Monitoring Stack Design

### Collection Layer
- Agent instrumentation
- Metric aggregation
- Sampling strategies
- Cardinality control

### Storage Layer
- Time-series database
- 90-day retention
- Data compression
- Backup and recovery

### Query Layer
- Real-time queries
- Historical analysis
- Custom aggregations
- Export capabilities

### Visualization Layer
- Live dashboards
- Service maps
- Heat maps
- Distribution charts

### Alert Layer
- Rule engine
- Anomaly detection
- Notification routing
- Incident creation

### Integration Layer
- GitHub issues
- Chat notifications
- On-call systems
- ITSM platforms

## Integration with Other Agents

The Performance Monitor agent collaborates with other meta-orchestration agents:

- **agent-organizer**: Provides performance data for agent coordination
- **error-coordinator**: Collaborates on incident response and root cause analysis
- **workflow-orchestrator**: Identifies workflow bottlenecks and optimization opportunities
- **task-distributor**: Analyzes load patterns for better task distribution
- **context-manager**: Tracks storage metrics and context retrieval performance
- **knowledge-synthesizer**: Provides insights for knowledge-based optimization
- **multi-agent-coordinator**: Monitors overall system efficiency and coordination

## Best Practices

1. **Start with Key Metrics**: Focus on business-critical metrics first
2. **Balance Overhead**: Monitor comprehensively but maintain <2% overhead
3. **High Signal-to-Noise**: Tune alerts to avoid alert fatigue
4. **Enable Drill-Down**: Provide granular details for troubleshooting
5. **Automate Responses**: Implement auto-remediation for common issues
6. **Regular Reviews**: Continuously refine monitoring configuration
7. **Integrate Workflows**: Connect monitoring to incident management
8. **Share Insights**: Make performance data accessible to all teams

## Troubleshooting

### High Metric Latency
- Check collector performance and network connectivity
- Review aggregation pipeline for bottlenecks
- Increase sampling rates if needed
- Optimize metric cardinality

### Alert Fatigue
- Review alert thresholds and tune for accuracy
- Implement suppression rules for known issues
- Consolidate related alerts
- Use anomaly detection instead of static thresholds

### Dashboard Performance
- Optimize query complexity
- Implement caching for frequently accessed data
- Reduce time range for real-time dashboards
- Use pre-aggregated metrics where possible

### Missing Data
- Verify collector health and connectivity
- Check retention policies
- Review data pipeline for errors
- Validate instrumentation coverage

## Contributing

To extend or customize the Performance Monitor agent:

1. Review the `CLAUDE.md` file for agent behavior
2. Modify `agent-manifest.json` to add new capabilities
3. Update `mcp-config.json` to add additional MCP servers
4. Test thoroughly with representative workloads
5. Document new features and slash commands

## License

See the main repository LICENSE file for details.

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.
