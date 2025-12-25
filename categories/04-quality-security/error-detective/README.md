# Error Detective Agent

> Expert error detective specializing in complex error pattern analysis, correlation, and root cause discovery

## Overview

The Error Detective agent specializes in analyzing complex error patterns, correlating distributed system failures, and uncovering hidden root causes. It excels at log analysis, error correlation, distributed tracing, anomaly detection, and predictive error prevention to improve system-wide reliability and prevent cascading failures.

## Capabilities

### Primary Skills
- Error pattern analysis and classification
- Log correlation across distributed systems
- Distributed tracing and request flow analysis
- Anomaly detection and predictive alerting
- Error cascade mapping and prevention
- Automated recovery strategy design
- Error taxonomy and categorization
- Impact assessment and risk scoring

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write error logs, analysis reports, and pattern databases |
| github | Track error patterns, create issues, and document solutions |
| memory | Maintain error patterns, root causes, and resolution history |
| context7 | Understand system architecture for error correlation |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/error-analyze` | Analyze error patterns and identify root causes |
| `/pattern-detect` | Detect recurring error patterns across systems |
| `/correlate` | Correlate errors across services and time |
| `/anomaly-find` | Identify anomalies and predict future errors |

### Example Prompts

```
Analyze the error patterns from the last 7 days and identify the top 5 root causes
```

```
Find the correlation between database timeout errors and user checkout failures
```

```
Detect anomalies in our error rates and predict potential outages
```

```
Map the error cascade when the payment service fails
```

```
Create a comprehensive error analysis report for the incident last night
```

```
Identify recurring 5xx errors in our API gateway and trace them to their origin services
```

```
Analyze error patterns across different user segments and geographic regions
```

```
Design predictive monitoring to prevent the database connection pool exhaustion we saw last week
```

## Error Analysis Workflow

### 1. Landscape Analysis
- **Error Inventory**: Aggregate errors from all sources (logs, traces, metrics)
- **Pattern Identification**: Identify frequency, timing, and distribution patterns
- **Service Mapping**: Map errors to services and dependencies
- **Baseline Establishment**: Create normal error rate baselines
- **Impact Assessment**: Quantify user, business, and system impacts

### 2. Correlation Phase
- **Cross-Service Correlation**: Connect errors across microservices
- **Temporal Correlation**: Identify time-based relationships
- **Causal Chain Analysis**: Reconstruct cause-and-effect sequences
- **Dependency Mapping**: Map service dependencies and error propagation
- **User Journey Tracking**: Trace errors through user workflows

### 3. Root Cause Discovery
- **Hypothesis Formation**: Develop testable theories based on evidence
- **Trace Analysis**: Follow distributed traces to error origins
- **Evidence Collection**: Gather logs, metrics, and traces
- **Verification**: Validate root causes with experiments
- **Documentation**: Create evidence chain and root cause report

### 4. Prevention Design
- **Predictive Monitoring**: Design early warning systems
- **Circuit Breakers**: Implement failure isolation patterns
- **Alert Optimization**: Tune alerts to reduce noise and improve signal
- **Automation**: Create automated recovery procedures
- **Knowledge Capture**: Document patterns for future reference

## Pattern Detection Techniques

### Error Classification
- **System Errors**: Infrastructure, network, database failures
- **Application Errors**: Logic bugs, exceptions, unhandled errors
- **User Errors**: Invalid input, authentication failures
- **Integration Errors**: Third-party API failures, timeouts
- **Performance Errors**: Slowdowns, timeouts, resource exhaustion
- **Security Errors**: Access violations, authentication failures
- **Data Errors**: Validation failures, corruption
- **Configuration Errors**: Misconfigurations, environment issues

### Pattern Analysis
1. **Frequency Analysis**: Error rate trends over time
2. **Time-Based Patterns**: Daily, weekly, seasonal variations
3. **Service Correlations**: Error relationships between services
4. **User Impact Patterns**: Affected user segments and demographics
5. **Geographic Patterns**: Regional error distribution
6. **Device Patterns**: Browser, OS, mobile vs desktop
7. **Version Patterns**: Errors by application version
8. **Load Patterns**: Error correlation with traffic load

## Distributed Tracing

### Request Flow Analysis
- Trace requests across microservices
- Identify latency bottlenecks
- Map service dependencies
- Detect error propagation paths
- Analyze timeout cascades
- Track resource utilization
- Reconstruct user journeys
- Identify critical paths

### Tools and Frameworks
- **OpenTelemetry**: Instrumentation and trace collection
- **Jaeger**: Distributed tracing platform
- **Zipkin**: Trace visualization and analysis
- **AWS X-Ray**: Cloud-native tracing
- **Datadog APM**: Application performance monitoring
- **New Relic**: Full-stack observability
- **Elastic APM**: ELK stack tracing
- **Grafana Tempo**: Distributed tracing backend

## Anomaly Detection

### Detection Methods
- **Statistical Analysis**: Standard deviation, Z-scores
- **Baseline Comparison**: Current vs historical patterns
- **Machine Learning**: Anomaly detection models
- **Threshold Monitoring**: Dynamic and static thresholds
- **Pattern Recognition**: Known vs unknown patterns
- **Trend Analysis**: Rate of change detection
- **Seasonal Decomposition**: Separate trends from seasonality

### Alert Optimization
- **False Positive Reduction**: Tune thresholds and correlation rules
- **Alert Grouping**: Combine related alerts
- **Severity Classification**: P0 (critical) to P3 (low)
- **Notification Routing**: Send to appropriate teams
- **Escalation Policies**: Auto-escalate unresolved alerts
- **Snooze and Suppress**: Temporary alert suspension
- **Feedback Loop**: Improve based on alert outcomes

## Cascade Analysis

### Understanding Error Propagation
1. **Identify Trigger**: Find the initial failure point
2. **Map Dependencies**: Document service dependencies
3. **Trace Propagation**: Follow error through the system
4. **Identify Amplification**: Find where errors multiply
5. **Assess Blast Radius**: Determine total impact
6. **Find Circuit Breakers**: Identify missing protections
7. **Design Prevention**: Implement isolation patterns

### Common Cascade Patterns
- **Retry Storms**: Aggressive retries overwhelming services
- **Timeout Chains**: Cascading timeouts across services
- **Queue Backups**: Message queue saturation
- **Connection Pool Exhaustion**: Database connection limits
- **Memory Leaks**: Gradual resource exhaustion
- **Thread Pool Exhaustion**: Worker thread depletion
- **Disk Space Exhaustion**: Storage capacity issues

## Forensic Analysis

### Investigation Process
1. **Evidence Collection**: Gather all available data
2. **Timeline Reconstruction**: Build event sequence
3. **Actor Identification**: Identify involved services and users
4. **Sequence Analysis**: Understand the order of events
5. **Impact Measurement**: Quantify the damage
6. **Recovery Analysis**: Document recovery actions
7. **Lesson Extraction**: Identify key learnings
8. **Report Generation**: Create comprehensive postmortem

### Data Sources
- Application logs
- System logs
- Error tracking platforms (Sentry, Rollbar)
- Distributed traces
- Metrics and dashboards
- Deployment history
- Configuration changes
- User feedback and reports

## Visualization

### Error Heat Maps
- Service error density over time
- Geographic error distribution
- User segment impact visualization
- Feature/endpoint error rates
- Time-of-day error patterns
- Resource correlation heatmaps

### Dependency Graphs
- Service dependency visualization
- Error propagation paths
- Critical path identification
- Circuit breaker placement
- Failure point highlighting
- Resource dependency mapping

### Trend Charts
- Error rate over time
- Pattern evolution tracking
- Seasonal variation display
- Version impact comparison
- Performance correlation
- Business metric correlation

## Prevention Strategies

### Proactive Monitoring
- Predictive error detection
- Early warning systems
- Anomaly alerting
- Capacity forecasting
- Health check automation
- Synthetic monitoring
- Chaos engineering experiments

### Circuit Breakers
- Timeout configuration
- Retry policy optimization
- Bulkhead pattern implementation
- Fallback strategy design
- Rate limiting
- Load shedding
- Graceful degradation

### Automated Recovery
- Auto-scaling triggers
- Service restart automation
- Traffic rerouting
- Cache warming
- Database failover
- Queue draining
- Resource cleanup

## Knowledge Management

### Pattern Library
Maintain comprehensive database of:
- Known error patterns
- Root cause mappings
- Resolution strategies
- Prevention techniques
- Detection methods
- Impact assessments
- Recovery procedures

### Team Collaboration
- Share error insights with developers
- Guide QA on test scenarios
- Support SRE on reliability improvements
- Help performance engineers on optimization
- Assist security team on security patterns
- Train teams on error prevention

## Best Practices

1. **Think Holistically**: Consider the entire distributed system
2. **Correlate Everything**: Connect errors across all dimensions
3. **Predict Proactively**: Use patterns to prevent future errors
4. **Map Cascades**: Understand error propagation thoroughly
5. **Measure Impact**: Quantify user, business, and system effects
6. **Automate Detection**: Build predictive monitoring systems
7. **Share Knowledge**: Document patterns and solutions
8. **Improve Continuously**: Refine detection and prevention
9. **Validate Hypotheses**: Always verify with evidence
10. **Design for Failure**: Implement resilience patterns

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for issue management and repository access
- `CONTEXT7_API_KEY` - Optional for architecture context access
- `UPSTASH_VECTOR_REST_URL` - Optional for Context7 integration
- `UPSTASH_VECTOR_REST_TOKEN` - Optional for Context7 integration

### CLI Tools
- Node.js 18+
- npx
- git

### Runtime Dependencies
None (analysis tools and platforms accessed via APIs)

## Error Investigation Checklist

- [ ] Error inventory completed comprehensively
- [ ] Patterns identified and categorized
- [ ] Cross-service correlations mapped
- [ ] Distributed traces analyzed
- [ ] Root causes determined with evidence
- [ ] Cascade effects documented
- [ ] Impact assessment completed
- [ ] Prevention strategies designed
- [ ] Monitoring improvements implemented
- [ ] Alerts optimized and validated
- [ ] Knowledge captured and shared
- [ ] Team trained on patterns
- [ ] Automation opportunities identified
- [ ] Recovery procedures documented
- [ ] Success metrics tracked

## Collaboration

Works closely with:
- **Debugger**: Deep technical issue analysis and code-level debugging
- **QA Expert**: Test scenario design based on error patterns
- **Performance Engineer**: Performance-related error analysis
- **Security Auditor**: Security error pattern identification
- **SRE Engineer**: Reliability improvements and SLO/SLA monitoring
- **DevOps Incident Responder**: Incident resolution and prevention
- **Backend Developer**: Application error fixes and prevention
- **Monitoring Specialist**: Alert optimization and dashboard creation

## Example Workflow

### Scenario: High Error Rate Investigation

1. **Discovery**
   - Alert triggered: 5xx error rate 10x above baseline
   - Collect logs from past 24 hours
   - Gather distributed traces
   - Review recent deployments

2. **Analysis**
   - Identify pattern: Errors spike after deployment
   - Correlate with specific API endpoints
   - Trace to database connection pool exhaustion
   - Map cascade: API → Database → Cache → User impact

3. **Root Cause**
   - New feature increased database queries 5x
   - Connection pool not sized for new load
   - No circuit breaker on database connections
   - Retry logic amplified the problem

4. **Prevention**
   - Increase connection pool size
   - Add circuit breaker pattern
   - Implement exponential backoff retries
   - Add database query monitoring
   - Create predictive capacity alerts

5. **Documentation**
   - Document pattern in knowledge base
   - Create runbook for similar issues
   - Share lessons with team
   - Update deployment checklist

## Metrics and Success

Track effectiveness through:
- **Error Detection Time**: Time to identify error patterns
- **Root Cause Time**: Time to identify root causes
- **Prevention Rate**: Percentage of errors prevented
- **Alert Accuracy**: True positive vs false positive ratio
- **Mean Time to Resolution**: Average time to resolve errors
- **Error Reduction**: Decrease in overall error rates
- **Cascade Prevention**: Reduction in cascading failures
- **Knowledge Sharing**: Team awareness and education
