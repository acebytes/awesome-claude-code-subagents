# SRE Engineer Agent

Expert Site Reliability Engineer balancing feature velocity with system stability through SLOs, automation, and operational excellence. Masters reliability engineering, chaos testing, and toil reduction with focus on building resilient, self-healing systems.

## Overview

The SRE Engineer agent implements Google's Site Reliability Engineering principles to build and maintain highly reliable, scalable systems. From defining SLOs and managing error budgets to reducing toil and conducting chaos experiments, this agent helps teams achieve operational excellence while maintaining sustainable development velocity.

## Key Capabilities

### SLI/SLO Management
- **SLI Identification**: Define meaningful service level indicators based on user experience
- **SLO Target Setting**: Set realistic objectives aligned with business requirements
- **Error Budgets**: Calculate and manage error budgets for velocity/reliability balance
- **Burn Rate Monitoring**: Track SLO consumption and trigger appropriate responses

### Toil Reduction
- **Toil Identification**: Quantify manual, repetitive work consuming engineering time
- **Automation Development**: Build tools and scripts to eliminate repetitive tasks
- **Process Optimization**: Streamline operations and reduce cognitive load
- **Efficiency Metrics**: Track toil reduction progress and automation coverage

### Chaos Engineering
- **Experiment Design**: Plan controlled failure injection experiments
- **Resilience Testing**: Validate system behavior under adverse conditions
- **Blast Radius Control**: Implement safety mechanisms for chaos experiments
- **Learning Integration**: Incorporate chaos findings into architecture improvements

### Reliability Patterns
- **Circuit Breakers**: Prevent cascading failures with intelligent circuit breaking
- **Retry Strategies**: Implement exponential backoff and jitter
- **Graceful Degradation**: Design systems that degrade gracefully under load
- **Self-Healing**: Build automation that detects and resolves common issues

### Capacity Planning
- **Demand Forecasting**: Project future capacity needs based on growth trends
- **Load Testing**: Validate system performance under various load conditions
- **Resource Optimization**: Right-size infrastructure for cost and performance
- **Scaling Strategies**: Design horizontal and vertical scaling approaches

### Incident Management
- **Response Procedures**: Establish clear incident response protocols
- **Postmortem Culture**: Build blameless learning culture from incidents
- **Root Cause Analysis**: Systematically identify underlying causes
- **Knowledge Sharing**: Capture and distribute learnings across teams

## Slash Commands

### /sre-slo
Define and manage Service Level Objectives (SLOs).

```
/sre-slo [action]
```

**Actions:**
- `define` - Define new SLOs for a service (default)
- `review` - Review existing SLOs and compliance
- `error-budget` - Calculate and analyze error budgets
- `burn-rate` - Monitor SLO burn rates

**Example usage:**

```bash
# Define SLOs for a service
/sre-slo define

# Review current SLO compliance
/sre-slo review

# Analyze error budget status
/sre-slo error-budget

# Monitor burn rates
/sre-slo burn-rate
```

**Actions performed:**
- Identify key SLIs (latency, availability, error rate)
- Set realistic SLO targets with stakeholders
- Implement SLI measurement infrastructure
- Calculate error budgets (100% - SLO target)
- Configure burn rate alerts
- Create SLO tracking dashboards
- Document SLO policies
- Setup stakeholder reporting

**Example output:**
```
SLO Definition Complete
=======================

Service: api-gateway
SLIs Identified: 4

1. Availability SLO
   SLI: Percentage of successful requests
   Target: 99.9% (3 nines)
   Error Budget: 0.1% (~43 minutes/month)
   Measurement: HTTP 200-299 / Total requests
   Current: 99.95% ✓ (within budget)

2. Latency SLO
   SLI: P95 response time
   Target: < 500ms
   Error Budget: 0.5% requests > 500ms
   Measurement: Response time histogram
   Current: P95 = 380ms ✓ (within budget)

3. Error Rate SLO
   SLI: Percentage of 5xx errors
   Target: < 0.1%
   Error Budget: 43 minutes of elevated errors/month
   Measurement: 5xx / Total requests
   Current: 0.03% ✓ (within budget)

4. Throughput SLO
   SLI: Requests handled per second
   Target: > 1000 RPS sustained
   Measurement: Request counter
   Current: 1450 RPS ✓ (within budget)

Error Budget Status:
- Availability: 75% remaining (32 min left this month)
- Latency: 90% remaining
- Error Rate: 85% remaining
- Overall Health: GOOD ✓

Burn Rate Alerts:
- Fast burn: > 5% budget/hour → Page
- Moderate burn: > 1% budget/hour → Alert
- Slow burn: > 0.1% budget/hour → Ticket

Dashboards Created:
- SLO Overview Dashboard
- Error Budget Tracking
- Burn Rate Monitoring
- Service Health Summary

Next Steps:
1. Share SLO dashboard with stakeholders
2. Schedule weekly error budget review
3. Document SLO policy and consequences
4. Train team on SLO-driven decision making
```

### /sre-toil
Identify and reduce toil in operations.

```
/sre-toil [action]
```

**Actions:**
- `identify` - Identify sources of toil (default)
- `measure` - Measure toil percentage
- `automate` - Create automation to reduce toil
- `track` - Track toil reduction progress

**Example usage:**

```bash
# Identify toil sources
/sre-toil identify

# Measure current toil percentage
/sre-toil measure

# Automate repetitive tasks
/sre-toil automate

# Track reduction progress
/sre-toil track
```

**Actions performed:**
- Analyze team activities and time allocation
- Identify repetitive, manual tasks
- Quantify toil as percentage of engineering time
- Prioritize automation opportunities by impact
- Build automation tools and scripts
- Implement self-service platforms
- Measure toil reduction progress
- Track efficiency improvements

**Example output:**
```
Toil Analysis Complete
======================

Current Toil Level: 62% of engineering time
Target: < 50%
Reduction Needed: 12 percentage points

Top Toil Sources:
1. Manual Deployment (18% of time)
   - 3-4 deployments/day
   - 45 minutes per deployment
   - High error rate (15%)
   - Automation Opportunity: HIGH

2. Log Investigation (15% of time)
   - Manual log searching
   - Multiple tools required
   - Time-consuming correlation
   - Automation Opportunity: MEDIUM

3. Certificate Rotation (12% of time)
   - Monthly manual renewal
   - 20+ certificates
   - Risk of expiration
   - Automation Opportunity: HIGH

4. On-call Alert Triage (10% of time)
   - 40% alerts are noise
   - Manual investigation required
   - Lack of context
   - Automation Opportunity: MEDIUM

5. Database Maintenance (7% of time)
   - Manual backups
   - Index optimization
   - Slow query analysis
   - Automation Opportunity: HIGH

Automation Roadmap:
Quarter 1:
- Automate deployments (eliminate 18% toil)
- Certificate automation (eliminate 12% toil)
- Expected toil: 32%

Quarter 2:
- Centralized logging with correlation (reduce 10%)
- Alert quality improvement (reduce 6%)
- Expected toil: 16%

Tools to Build:
1. deploy-bot
   - Slack-integrated deployment
   - Automated rollback
   - Health verification
   - Estimated time: 2 weeks

2. cert-manager
   - Automatic renewal
   - Expiration monitoring
   - Self-service API
   - Estimated time: 1 week

3. log-correlator
   - Cross-service log search
   - Automatic correlation
   - Pattern detection
   - Estimated time: 3 weeks

ROI Analysis:
- Time invested: 6 person-weeks
- Time saved: 30% of team capacity (ongoing)
- Payback period: 1.5 months
- Annual savings: ~1.5 FTE equivalent

Next Steps:
1. Get approval for automation roadmap
2. Start with deploy-bot (highest impact)
3. Weekly toil tracking review
4. Celebrate wins and share learnings
```

### /sre-chaos
Plan and execute chaos engineering experiments.

```
/sre-chaos [experiment]
```

**Experiments:**
- `plan` - Design chaos experiment (default)
- `latency` - Inject network latency
- `failure` - Simulate service failures
- `resource` - Stress CPU/memory/disk
- `network` - Test network partitions

**Example usage:**

```bash
# Plan chaos experiment
/sre-chaos plan

# Test latency resilience
/sre-chaos latency

# Simulate service failures
/sre-chaos failure

# Stress test resources
/sre-chaos resource

# Test network partitions
/sre-chaos network
```

**Actions performed:**
- Define steady state and success criteria
- Form hypothesis about system behavior
- Design experiment with controlled scope
- Implement safety mechanisms and abort conditions
- Execute chaos injection in production
- Observe system behavior and metrics
- Analyze results and document findings
- Integrate learnings into improvements

**Example output:**
```
Chaos Experiment Plan
=====================

Experiment: Network Latency Injection
Target: payment-service
Environment: Production (10% traffic)
Duration: 30 minutes
Safety: Auto-abort enabled

Hypothesis:
"When network latency to payment-service increases to 500ms,
the system will gracefully degrade by:
- Showing cached payment status to users
- Queuing payment requests for retry
- Maintaining overall availability > 99.5%
- Not cascading failures to other services"

Steady State Definition:
- API availability: 99.9%
- P95 latency: < 300ms
- Error rate: < 0.1%
- Payment success rate: > 99%
- Upstream services healthy

Experiment Design:
1. Baseline Period (5 min)
   - Measure steady state metrics
   - Confirm system health

2. Ramp-up (5 min)
   - Gradually inject latency: 0→500ms
   - Monitor for degradation

3. Steady Chaos (15 min)
   - Maintain 500ms latency
   - Observe system behavior
   - Validate hypothesis

4. Recovery (5 min)
   - Remove latency injection
   - Monitor return to steady state

Blast Radius Controls:
- Traffic: 10% of production load
- Geography: US-West region only
- Auto-abort triggers:
  * Error rate > 1%
  * Availability < 99%
  * Manual stop button
  * Timeout after 30 minutes

Metrics to Monitor:
- Request latency (all percentiles)
- Error rate by type
- Circuit breaker state
- Cache hit rate
- Queue depth
- Upstream service health
- User-facing errors

Safety Mechanisms:
1. Gradual rollout (10% traffic)
2. Real-time monitoring dashboard
3. Auto-abort on threshold breach
4. Manual kill switch accessible
5. Rollback procedure documented
6. Incident response team on standby

Expected Outcomes:
✓ Circuit breaker opens after 10 failed requests
✓ Cache serves stale data for non-critical paths
✓ Payment requests queue for retry
✓ User sees "processing" status (not error)
✓ No impact to other services
✓ Recovery within 2 minutes of ending chaos

Success Criteria:
- Overall availability remains > 99.5%
- No cascading failures observed
- Circuit breaker functions correctly
- User experience gracefully degraded
- System recovers within 5 minutes

Risks Identified:
- Cache may not cover all scenarios
- Queue could fill if latency persists
- Monitoring gaps in retry logic
- Potential customer impact if abort fails

Mitigation:
- Test in staging first
- Start with 1% traffic
- Have manual rollback ready
- Customer support team notified

Post-Experiment Actions:
1. Analyze results vs. hypothesis
2. Document unexpected behaviors
3. Create action items for gaps found
4. Update runbooks with learnings
5. Share findings with team
6. Plan follow-up experiments

Execution Command:
```bash
chaos-toolkit run experiments/latency-payment-service.yaml \
  --rollback-strategy=always \
  --hypothesis-frequency=5s
```

Next Steps:
1. Review and approve experiment plan
2. Schedule chaos experiment window
3. Brief incident response team
4. Execute in staging environment first
5. Execute in production (if staging succeeds)
6. Conduct post-experiment review
```

## Maturity Targets

The agent optimizes toward these SRE maturity targets:

| Metric | Target | Industry Average |
|--------|--------|------------------|
| SLO Coverage | 95%+ | 40-60% |
| SLO Compliance | >99.9% | 95-99% |
| Toil Percentage | <50% | 60-80% |
| Automation Coverage | >90% | 50-70% |
| MTTR | <30 minutes | 1-4 hours |
| Postmortem Completion | 100% | 60-80% |
| On-call Sustainability | Verified | Often problematic |
| Error Budget Managed | Active | Rarely used |
| Chaos Experiments | Monthly | Rare |

## Use Cases

### 1. Undefined Reliability Targets
**Problem**: No clear reliability targets, frequent debates about feature velocity vs. stability.

**Solution**:
```bash
/sre-slo define
```

**Results**:
- Clear SLO targets for all critical services
- Error budget framework for decision making
- Data-driven velocity/reliability balance
- Stakeholder alignment on expectations
- 99.9% SLO compliance achieved

### 2. High Operational Toil
**Problem**: Team spending 70% of time on manual operations, little time for improvements.

**Solution**:
```bash
/sre-toil identify
/sre-toil automate
```

**Results**:
- Toil reduced from 70% to 35%
- Automation coverage increased to 90%
- Team capacity freed for strategic work
- Developer satisfaction improved
- Faster incident response

### 3. Unknown System Resilience
**Problem**: Uncertain how system behaves under failure conditions, incidents reveal surprises.

**Solution**:
```bash
/sre-chaos plan
/sre-chaos failure
```

**Results**:
- Regular chaos experiments validate resilience
- Failure modes discovered and fixed proactively
- Confidence in system behavior under stress
- Improved incident response procedures
- Reduced MTTR by 60%

### 4. Alert Fatigue
**Problem**: 100+ alerts per day, 80% noise, on-call team burned out.

**Solution**:
- Implement SLO-based alerting
- Reduce alert noise through correlation
- Focus on actionable alerts only
- Improve runbook quality

**Results**:
- Alerts reduced from 100/day to 5/day
- 95% of alerts are actionable
- On-call burden sustainable
- MTTR improved (less noise)
- Team well-being improved

### 5. Capacity Surprises
**Problem**: Unexpected capacity limits during traffic spikes, emergency scaling required.

**Solution**:
- Implement capacity planning process
- Regular load testing
- Traffic forecasting
- Proactive scaling

**Results**:
- Capacity planned 6 months ahead
- No emergency scaling incidents
- Cost optimized (right-sized resources)
- Confident in handling 3x traffic
- Smooth handling of seasonal peaks

## MCP Server Configuration

The agent uses four MCP servers for comprehensive SRE capabilities:

### Filesystem Server (Required)
Access service configs, runbooks, and automation scripts.

```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
  }
}
```

**Used for**:
- Reading service configurations
- Accessing runbook documentation
- Reviewing automation scripts
- Analyzing SLO definitions
- Reading incident postmortems

### GitHub Server (Optional)
Track incidents and manage infrastructure as code.

```json
{
  "github": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-github"],
    "env": {
      "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_PERSONAL_ACCESS_TOKEN}"
    }
  }
}
```

**Used for**:
- Tracking incidents as issues
- Managing runbooks in repositories
- Automating deployment workflows
- Monitoring SLO compliance via CI/CD
- Collaborating on postmortems

### Context7 Server (Optional)
Access SRE best practices and documentation.

```json
{
  "context7": {
    "command": "npx",
    "args": ["-y", "@upstash/context7-mcp-server"],
    "env": {
      "UPSTASH_VECTOR_REST_URL": "${UPSTASH_VECTOR_REST_URL}",
      "UPSTASH_VECTOR_REST_TOKEN": "${UPSTASH_VECTOR_REST_TOKEN}"
    }
  }
}
```

**Used for**:
- Learning SRE best practices
- Understanding reliability patterns
- Researching chaos engineering techniques
- Studying monitoring strategies
- Reviewing incident response procedures

### Fetch Server (Optional)
Query monitoring endpoints and validate service health.

```json
{
  "fetch": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-fetch"]
  }
}
```

**Used for**:
- Querying monitoring APIs (Prometheus, Datadog)
- Checking service health endpoints
- Retrieving current metrics
- Validating SLO compliance
- Testing API availability

## Integration with Other Agents

### devops-engineer
Partner on automation infrastructure, CI/CD pipelines, and reliability tooling.

### cloud-architect
Collaborate on reliability patterns, architecture design, and failure domain isolation.

### kubernetes-specialist
Work on Kubernetes reliability, self-healing, and resource optimization.

### platform-engineer
Guide on platform SLOs, developer experience, and self-service reliability.

### deployment-engineer
Help with safe deployment practices, rollback procedures, and release confidence.

### incident-responder
Support incident management, response procedures, and postmortem culture.

### security-engineer
Integrate security with reliability engineering and chaos testing.

### database-administrator
Coordinate on database reliability, performance, and disaster recovery.

## Best Practices

### SRE Principles
1. **SLOs Drive Decisions**: Use error budgets to balance velocity and reliability
2. **Embrace Failure**: Build resilient systems that expect and handle failure
3. **Reduce Toil**: Automate repetitive work to free capacity for improvements
4. **Measure Everything**: Data-driven decision making based on metrics
5. **Blameless Culture**: Learn from incidents without blame or punishment
6. **Sustainable On-call**: Keep on-call burden manageable and valued
7. **Chaos Engineering**: Proactively test resilience through controlled failures
8. **Continuous Learning**: Every incident is an opportunity to improve

### Implementation Approach
1. **Start with SLOs**: Define what reliability means for your service
2. **Measure Current State**: Baseline metrics before making changes
3. **Identify Quick Wins**: Build momentum with high-impact, low-effort improvements
4. **Automate Incrementally**: Don't try to automate everything at once
5. **Build Culture**: SRE is as much about culture as technology
6. **Share Learnings**: Postmortems and knowledge sharing are critical
7. **Iterate and Improve**: Continuous refinement based on feedback

### Success Metrics
- **SLO Compliance**: > 99.9% of time within SLO targets
- **Toil Level**: < 50% of engineering time on toil
- **MTTR**: Mean time to recovery < 30 minutes
- **Automation**: > 90% of operational tasks automated
- **Postmortems**: 100% of incidents have blameless postmortems
- **On-call Load**: < 2 actionable alerts per on-call shift
- **Team Satisfaction**: > 4.0/5.0 on team happiness surveys
- **Chaos Experiments**: Regular (monthly) chaos testing
- **Error Budget**: Actively used in feature velocity decisions

## Getting Started

1. **Install the agent** in your Claude Code environment
2. **Configure MCP servers** (at minimum, filesystem server)
3. **Assess current state**: Review reliability metrics and practices
4. **Define SLOs**: `/sre-slo define`
5. **Identify toil**: `/sre-toil identify`
6. **Plan chaos experiments**: `/sre-chaos plan`
7. **Implement improvements**: Focus on high-impact areas
8. **Measure and iterate**: Track progress toward maturity targets

## Example Workflow

```bash
# Step 1: Define SLOs for critical services
/sre-slo define

# Step 2: Set up error budget tracking
/sre-slo error-budget

# Step 3: Identify operational toil
/sre-toil identify

# Step 4: Build automation to reduce toil
/sre-toil automate

# Step 5: Plan chaos experiment
/sre-chaos plan

# Step 6: Execute controlled failure test
/sre-chaos failure

# Step 7: Monitor burn rates
/sre-slo burn-rate

# Step 8: Track toil reduction progress
/sre-toil track
```

## Advanced Features

### Error Budget Policy
- Automated feature freeze when budget depleted
- Burn rate alerts at multiple thresholds
- Stakeholder communication automation
- Exception handling process

### Self-Healing Systems
- Automatic incident detection
- Automated remediation for common issues
- Health check-based auto-recovery
- Progressive rollback capabilities

### Capacity Management
- Demand forecasting models
- Automated scaling policies
- Cost optimization recommendations
- Resource efficiency tracking

### Observability
- Golden signals monitoring (latency, traffic, errors, saturation)
- User journey tracking
- Distributed tracing
- Real user monitoring (RUM)

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT
