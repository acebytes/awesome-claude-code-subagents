# Chaos Engineer Agent

> Expert chaos engineer specializing in controlled failure injection, resilience testing, and building antifragile systems

## Overview

The Chaos Engineer agent specializes in resilience testing through controlled failure injection, chaos experiments, and game day planning. It helps teams discover weaknesses before they become outages, reduce MTTR through practice, and build systems that get stronger under stress.

## Capabilities

### Primary Skills
- Experiment design and hypothesis formulation
- Controlled failure injection and blast radius management
- Infrastructure chaos (servers, zones, regions)
- Application chaos (memory, CPU, threads, deadlocks)
- Data chaos (replication lag, corruption, backups)
- Network chaos (latency, packet loss, partitions)
- Security chaos (auth failures, cert rotation)
- Game day planning and execution
- Chaos automation frameworks
- Resilience assessment and MTTR reduction

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Access experiment plans, runbooks, and chaos playbooks |
| github | Track chaos experiments and resilience improvements |
| memory | Maintain experiment history and failure patterns |
| fetch | Monitor system health and validate steady state |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/chaos-experiment` | Design and execute a controlled chaos experiment |
| `/game-day` | Plan and execute a chaos game day |
| `/resilience-test` | Assess system resilience and identify weak points |
| `/blast-radius` | Analyze and control experiment blast radius |

### Example Prompts

```
Design a chaos experiment to test our system's resilience to availability zone failures
```

```
Plan and execute a game day to simulate a database failover scenario
```

```
Assess our microservices architecture for resilience and identify weak points
```

```
Test how our system handles network latency and packet loss between services
```

```
Execute a chaos experiment to validate our circuit breaker implementation
```

## Chaos Engineering Methodology

### Experiment Design Process

1. **Form Hypothesis**: What do you expect will happen when you inject a specific failure?
2. **Define Steady State**: What metrics indicate normal system behavior?
3. **Inject Failure**: Introduce controlled chaos (infrastructure, network, application)
4. **Observe Behavior**: Monitor system response and recovery
5. **Learn and Improve**: Document findings and implement resilience improvements

### Steady State Metrics

- **Response Time**: p50, p95, p99 latency
- **Error Rate**: Percentage of failed requests
- **Throughput**: Requests per second
- **Availability**: Uptime percentage
- **Resource Utilization**: CPU, memory, disk usage
- **Queue Depths**: Backlog and processing queues
- **Business Metrics**: Custom KPIs

### Failure Injection Types

#### Infrastructure Chaos
- Server shutdowns and crashes
- Availability zone outages
- Region-level failures
- Storage failures
- Network device failures
- Certificate expiration
- DNS resolution failures

#### Application Chaos
- Memory leak injection
- CPU spike simulation
- Thread pool exhaustion
- Deadlock scenarios
- Race conditions
- Cache invalidation
- Exception injection
- Timeout simulation

#### Network Chaos
- Latency injection (50ms-5000ms)
- Packet loss (1%-50%)
- Network partitions
- Bandwidth throttling
- Connection timeouts
- DNS failures
- Load balancer failures

#### Data Chaos
- Replication lag simulation
- Data corruption
- Backup/restore testing
- Consistency issues
- Transaction failures
- Volume testing
- Schema migration failures

#### Security Chaos
- Authentication failures
- Authorization bypass
- Certificate rotation
- Key rotation
- DDoS simulation
- Access revocation
- Token expiration

## Blast Radius Control

### Safety Mechanisms

The agent implements multiple layers of safety:

1. **Environment Isolation**: Start in non-production
2. **Traffic Limiting**: Affect only a percentage of traffic
3. **User Segmentation**: Impact only canary users
4. **Feature Flags**: Quick disable capability
5. **Circuit Breakers**: Automatic protection
6. **Auto Rollback**: < 30 second recovery
7. **Kill Switches**: Manual abort capability
8. **Monitoring**: Continuous metric tracking

### Rollback Procedures

- Automated rollback triggers based on metrics
- Manual override capability
- Health check validation
- Alert integration
- Team notification
- Documentation of actions

## Game Day Planning

### Scenario Types

- **Production Incident Replay**: Recreate past incidents
- **Worst-Case Failures**: Test extreme scenarios
- **Cascading Failures**: Multiple simultaneous failures
- **Data Center Outages**: Regional failures
- **Dependency Failures**: Third-party service issues
- **Communication Chaos**: Incident response drills

### Game Day Structure

1. **Preparation (T-60min)**: Team assembly, tool verification
2. **Briefing (T-30min)**: Roles, scenario, success criteria
3. **Baseline (T-15min)**: Verify steady state metrics
4. **Injection (T-0)**: Begin chaos experiment
5. **Observation (T+0 to T+30)**: Monitor and respond
6. **Recovery (T+30 to T+45)**: Restore normal operation
7. **Validation (T+45 to T+60)**: Verify complete recovery
8. **Debrief (T+60+)**: Extract learnings and action items

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for tracking experiments in GitHub

### CLI Tools
- Node.js 18+
- npx
- kubectl (for Kubernetes chaos)
- Chaos engineering tools (optional):
  - Chaos Toolkit
  - Litmus Chaos
  - Chaos Mesh
  - Pumba

## Automation Framework

### Continuous Chaos

The agent supports automated chaos engineering:

- **Scheduled Experiments**: Regular chaos tests
- **CI/CD Integration**: Chaos in deployment pipeline
- **Production Testing**: Safe production chaos
- **Metric Collection**: Automated result gathering
- **Trend Analysis**: Resilience tracking over time
- **Alert Correlation**: Link chaos to monitoring
- **Report Generation**: Automated documentation

### Metrics Tracked

- Experiments executed
- Failure modes discovered
- Improvements implemented
- MTTR reduction percentage
- Resilience score (1-5)
- Coverage percentage
- Cost savings
- Team confidence level

## Resilience Assessment

### Assessment Areas

1. **Architecture Review**: Identify single points of failure
2. **Dependency Mapping**: Understand cascading failures
3. **Recovery Procedures**: Validate runbooks
4. **Monitoring Coverage**: Ensure observability
5. **Team Readiness**: Assess response capability
6. **Redundancy**: Check failover mechanisms
7. **Resilience Score**: Quantify system strength

### Resilience Score (1-5)

- **1.0**: No redundancy, single points of failure
- **2.0**: Basic redundancy, manual recovery
- **3.0**: Automated failover, monitoring in place
- **4.0**: Self-healing, proven through chaos
- **5.0**: Antifragile, gets stronger from failures

## Best Practices

### Safety First
1. Always start in non-production environments
2. Control blast radius tightly
3. Enable quick rollback mechanisms
4. Monitor continuously during experiments
5. Communicate clearly with stakeholders
6. Document everything thoroughly
7. Never surprise your team or users

### Scientific Method
1. Form clear, testable hypotheses
2. Define steady state metrics
3. Control experiment variables
4. Measure everything
5. Analyze results objectively
6. Share findings widely
7. Implement learnings
8. Iterate continuously

### Team Culture
1. Blameless experimentation
2. Learning over blame
3. Transparency in results
4. Shared responsibility
5. Continuous improvement
6. Knowledge sharing
7. Psychological safety
8. Celebrate learning from failure

### Success Metrics
- Regular experiment execution
- Failure modes discovered and fixed
- MTTR reduction achieved
- Resilience score improvement
- Team confidence increase
- Zero customer impact from chaos
- Cost savings from prevented outages
- Knowledge shared across organization

## Collaboration

Works closely with:
- **SRE Engineer**: Reliability, SLOs, error budgets
- **DevOps Engineer**: Infrastructure resilience
- **Platform Engineer**: Chaos tools and frameworks
- **Kubernetes Specialist**: K8s chaos experiments
- **Security Engineer**: Security chaos testing
- **Performance Engineer**: Combined performance/chaos testing
- **Incident Responder**: Response procedure improvement
- **Architect Reviewer**: Resilience architecture design

## Advanced Techniques

### Combinatorial Failures
- Multiple simultaneous failures
- Cascading failure chains
- Correlated failure scenarios
- Worst-case combinations

### Byzantine Failures
- Inconsistent states across nodes
- Split-brain scenarios
- Data inconsistency
- Partial failures

### Performance Degradation
- Gradual slowdowns
- Resource contention
- Thundering herd problems
- Recovery storms

## Common Experiment Examples

### Example 1: Zone Failure
```
Hypothesis: System will continue serving traffic with <1% error rate
when one availability zone fails.

Steady State: Error rate < 0.1%, p99 latency < 500ms
Injection: Terminate all instances in one AZ
Observation: Monitor error rate, latency, and recovery time
Success: Error rate stays < 1%, automatic recovery < 5 minutes
```

### Example 2: Database Failover
```
Hypothesis: Application will automatically failover to replica
database within 30 seconds with zero data loss.

Steady State: All transactions succeeding, replication lag < 1s
Injection: Force primary database failure
Observation: Monitor failover time, data consistency, errors
Success: Failover < 30s, no data loss, no user-facing errors
```

### Example 3: Network Latency
```
Hypothesis: Circuit breakers will open when service latency
exceeds 1000ms, preventing cascading failures.

Steady State: Service latency < 100ms, no timeouts
Injection: Add 2000ms latency to downstream service
Observation: Monitor circuit breaker state, timeout errors, recovery
Success: Circuit breaker opens, graceful degradation, auto recovery
```

## Learning and Improvement

### Capture Learnings
- Document all experiment results
- Identify gaps in monitoring
- Update runbooks with new procedures
- Share findings across teams
- Create action items for improvements
- Track improvement implementation
- Measure resilience improvement

### Continuous Improvement
- Regular experiment schedule
- Increasing complexity over time
- Building team confidence
- Reducing MTTR
- Improving resilience score
- Sharing knowledge
- Celebrating learning

## Output and Reporting

The agent provides comprehensive reporting:

- **Experiment Reports**: Detailed findings and learnings
- **Resilience Assessments**: System strength evaluation
- **Game Day Summaries**: Team performance and action items
- **Trend Analysis**: Resilience improvement over time
- **Recommendations**: Prioritized improvement suggestions
- **Cost Analysis**: Value of chaos engineering program

## Getting Started

1. Start with resilience assessment using `/resilience-test`
2. Design your first experiment with `/chaos-experiment infrastructure`
3. Plan a game day with `/game-day plan`
4. Analyze blast radius with `/blast-radius analyze`
5. Execute experiments in non-production first
6. Build team confidence through practice
7. Graduate to production chaos testing
8. Automate and continuously improve

Remember: Chaos engineering is about learning and improvement, not breaking things. The goal is to discover and fix weaknesses before they cause real outages, making your systems antifragile.
