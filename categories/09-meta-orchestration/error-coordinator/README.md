# Error Coordinator Agent

Expert error coordinator specializing in distributed error handling, failure recovery, and system resilience. Masters error correlation, cascade prevention, and automated recovery strategies across multi-agent systems with focus on minimizing impact and learning from failures.

## Overview

The Error Coordinator agent is a senior specialist in distributed system resilience, providing comprehensive error handling, failure recovery, and continuous learning capabilities. It focuses on preventing cascading failures, minimizing downtime, and building anti-fragile systems that improve through failure.

## Key Features

- **Error Aggregation**: Collect, classify, and analyze errors across distributed systems
- **Cross-Agent Correlation**: Identify temporal and causal relationships between errors
- **Cascade Prevention**: Implement circuit breakers, bulkheads, and isolation patterns
- **Recovery Orchestration**: Automate rollback, state restoration, and service recovery
- **Pattern Analysis**: Detect trends, anomalies, and predict future failures
- **Post-Mortem Automation**: Generate incident reports and extract learnings
- **Chaos Engineering**: Proactively test system resilience
- **Continuous Learning**: Improve recovery strategies based on historical data

## Performance Targets

- **Error Detection**: < 30 seconds
- **Recovery Success Rate**: > 90%
- **Cascade Prevention**: 100%
- **False Positive Rate**: < 5%
- **Mean Time To Recovery (MTTR)**: < 5 minutes

## Slash Commands

### `/error-analyze`
Analyze error patterns, correlations, and impact chains across the system. Identifies root causes, temporal correlations, and potential cascade risks.

**Usage:**
```
/error-analyze
```

**Output:**
- Error classification and taxonomy
- Temporal and causal correlations
- Impact analysis and severity assessment
- Root cause identification
- Cascade risk evaluation

### `/error-correlate`
Correlate errors across multiple agents and services to identify systemic issues, dependency failures, and propagation patterns.

**Usage:**
```
/error-correlate
```

**Output:**
- Cross-service error relationships
- Dependency chain analysis
- Error propagation paths
- Systemic issue identification
- Service mesh impact map

### `/error-recover`
Execute automated recovery procedures including rollback, state restoration, service restart, and health verification.

**Usage:**
```
/error-recover
```

**Actions:**
- Automated rollback procedures
- State restoration and reconciliation
- Service health verification
- Gradual recovery implementation
- Post-recovery validation

### `/error-report`
Generate comprehensive error reports including incident timeline, impact analysis, recovery actions, and improvement recommendations.

**Usage:**
```
/error-report
```

**Output:**
- Incident timeline
- Impact analysis
- Root cause documentation
- Recovery actions taken
- Action items for improvement
- Lessons learned

## Installation

### Prerequisites

- Node.js and npx installed
- GitHub Personal Access Token (for GitHub integration)
- Access to the project workspace

### MCP Servers

The agent uses the following MCP servers:

1. **Filesystem**: Access to local files and directories
2. **GitHub**: Integration with GitHub for issue tracking and documentation
3. **Memory**: Persistent storage for error patterns and learning

### Setup

1. Set your GitHub token as an environment variable:
```bash
export GITHUB_TOKEN=your_github_personal_access_token
```

2. The agent will automatically use the MCP servers configured in `mcp-config.json`

## Usage Examples

### Basic Error Analysis
```
Can you analyze the recent errors in our system?
```
The agent will:
1. Collect recent error logs
2. Classify and categorize errors
3. Identify patterns and correlations
4. Provide severity assessment
5. Suggest immediate actions

### Recovery Coordination
```
We're experiencing cascading failures in the payment service. Can you coordinate recovery?
```
The agent will:
1. Analyze error propagation
2. Implement circuit breakers
3. Execute automated recovery
4. Verify service health
5. Monitor for re-occurrence

### Post-Incident Analysis
```
Generate a post-mortem for the incident on December 20th
```
The agent will:
1. Reconstruct incident timeline
2. Analyze root causes
3. Document impact
4. List recovery actions
5. Generate improvement recommendations

### Proactive Resilience Testing
```
Can you design chaos engineering tests for our microservices?
```
The agent will:
1. Identify critical failure points
2. Design failure injection tests
3. Define success criteria
4. Implement monitoring
5. Schedule test execution

## Workflow

### Phase 1: Failure Analysis
1. Map failure modes across the system
2. Identify and classify error types
3. Analyze service dependencies
4. Review incident history
5. Assess recovery gaps
6. Calculate impact costs
7. Prioritize improvements

### Phase 2: Implementation
1. Deploy error collectors
2. Configure correlation engines
3. Implement circuit breakers
4. Set up recovery flows
5. Create fallback mechanisms
6. Enable comprehensive monitoring
7. Automate response procedures
8. Document all procedures

### Phase 3: Resilience Excellence
1. Ensure graceful failure handling
2. Automate recovery processes
3. Prevent cascade failures
4. Capture learning from incidents
5. Identify and fix systemic patterns
6. Harden system components
7. Train teams on procedures
8. Validate resilience continuously

## Integration with Other Agents

The Error Coordinator works seamlessly with:

- **performance-monitor**: Error detection and alerting
- **workflow-orchestrator**: Recovery workflow coordination
- **multi-agent-coordinator**: System-wide resilience
- **agent-organizer**: Error handling patterns
- **task-distributor**: Failure routing and retry
- **context-manager**: State recovery and consistency
- **knowledge-synthesizer**: Learning extraction and knowledge base
- **Teams**: Incident response coordination

## Resilience Patterns

### Circuit Breaker
- Threshold-based activation
- Half-open state testing
- Automatic reset on success
- Monitoring and alerting

### Retry Strategies
- Exponential backoff with jitter
- Retry budgets to prevent storms
- Dead letter queues for exhausted retries
- Alternative path routing

### Fallback Mechanisms
- Cached response serving
- Default value provisioning
- Degraded service modes
- Alternative provider failover

### Bulkhead Isolation
- Resource pool separation
- Thread pool isolation
- Queue-based buffering
- Load shedding under pressure

## Best Practices

1. **Fail Fast**: Detect failures quickly and respond immediately
2. **Graceful Degradation**: Provide reduced functionality rather than complete failure
3. **Automate Recovery**: Minimize manual intervention in recovery processes
4. **Learn Continuously**: Extract lessons from every incident
5. **Test Resilience**: Regular chaos engineering and failure testing
6. **Document Everything**: Automated documentation of incidents and recovery
7. **Monitor Comprehensively**: Full observability across all components
8. **Balance Automation**: Maintain human oversight for critical decisions

## Configuration

The agent uses the following configuration options:

- **errorBudget**: Enable error budget tracking
- **autoRecovery**: Enable automated recovery procedures
- **chaosEngineering**: Enable chaos engineering tests
- **learningEnabled**: Enable continuous learning from incidents
- **circuitBreakerEnabled**: Enable circuit breaker patterns

## Metrics and Monitoring

Track the following metrics:

- **Errors Handled**: Total number of errors processed
- **Recovery Rate**: Percentage of automatic successful recoveries
- **Cascades Prevented**: Number of cascade failures avoided
- **MTTR**: Mean time to recovery in minutes
- **False Positives**: Rate of incorrect error classifications
- **Learning Effectiveness**: Improvement in recovery over time

## Troubleshooting

### High False Positive Rate
- Review error classification thresholds
- Tune alert sensitivity
- Update pattern recognition models
- Increase baseline data collection

### Low Recovery Rate
- Review automated recovery procedures
- Check for new failure modes
- Update recovery playbooks
- Increase monitoring coverage

### Cascading Failures
- Review circuit breaker thresholds
- Implement stricter bulkhead isolation
- Add more aggressive timeout management
- Improve service dependency mapping

## Support and Feedback

For issues, improvements, or questions about the Error Coordinator agent, please refer to the main repository documentation or contact the maintainers.

## License

Part of the Claude Code Agent Marketplace.
