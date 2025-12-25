# DevOps Incident Responder Agent

Expert incident responder specializing in rapid detection, diagnosis, and resolution of production issues. Masters observability tools, root cause analysis, and automated remediation with focus on minimizing downtime and preventing recurrence.

## Overview

The DevOps Incident Responder agent is designed to handle critical production incidents with speed and precision. From detecting anomalies through monitoring systems to coordinating complex responses across teams, from diagnosing root causes to implementing automated remediation, this agent minimizes downtime and builds resilient systems through continuous learning.

## Key Capabilities

### Incident Detection
- **Multi-layer Monitoring**: Application, infrastructure, user experience, and business metrics
- **Anomaly Detection**: Statistical and ML-based pattern recognition for early warning
- **Alert Optimization**: Reduce noise, improve signal, eliminate alert fatigue
- **Synthetic Monitoring**: Proactive issue detection before user impact

### Rapid Diagnosis
- **Triage Procedures**: Quick severity classification and impact assessment
- **Root Cause Analysis**: Five whys, hypothesis testing, timeline reconstruction
- **Distributed Tracing**: Service interaction mapping and latency breakdown
- **Log Correlation**: Cross-service pattern identification and timeline building

### Automated Remediation
- **Auto-healing**: Self-remediation scripts for common issue patterns
- **Rollback Automation**: Instant deployment reversal on detection
- **Circuit Breakers**: Automatic dependency isolation and fallback
- **Emergency Scaling**: Dynamic resource adjustment under load

### Response Coordination
- **Incident Command**: Structured leadership and decision-making framework
- **Communication Management**: Stakeholder updates, status pages, team coordination
- **War Room Setup**: Dedicated channels and real-time collaboration
- **Escalation Management**: Tiered response with appropriate expertise

### Observability Mastery
- **APM Platforms**: Datadog, New Relic, Dynatrace expertise
- **Metric Systems**: Prometheus, Grafana, time-series analysis
- **Log Aggregation**: ELK Stack, Splunk, Loki proficiency
- **Tracing Tools**: Jaeger, Zipkin, distributed request tracking

### Continuous Improvement
- **Blameless Postmortems**: Learning-focused retrospectives
- **Action Item Tracking**: Systematic follow-through on improvements
- **Runbook Development**: Automated, tested response procedures
- **Knowledge Management**: Searchable incident database and solution library

## Slash Commands

### /ops-detect
Detect and analyze production issues using monitoring data.

```
/ops-detect [service]
```

**Services:**
- `all` - System-wide detection (default)
- `api-service` - Specific service analysis
- `database` - Database issue detection
- `frontend` - Frontend service analysis

**Example usage:**

```bash
# Detect issues across all services
/ops-detect

# Analyze specific service
/ops-detect api-service

# Check database health
/ops-detect database
```

**Actions performed:**
- Query monitoring systems (Prometheus, Datadog, CloudWatch)
- Analyze metrics for anomalies (RED/USE methods)
- Review recent alerts and their patterns
- Correlate logs for error spikes
- Examine distributed traces for latency issues
- Assess user impact and scope
- Determine severity level (P0-P4)
- Generate detection report with recommendations

**Example output:**
```
Incident Detection Report
=========================

Status: CRITICAL INCIDENT DETECTED
Severity: P1 (High Impact)
Detected at: 2024-12-24 14:32:17 UTC
MTTD: 2 minutes 13 seconds

Affected Services:
- api-service (PRIMARY)
  - Error rate: 12.3% (baseline: 0.1%)
  - Response time P95: 8.2s (baseline: 450ms)
  - Request rate: -45% (significant drop)

- database-service (SECONDARY)
  - Connection pool: 98% utilization (critical)
  - Query latency P95: 5.1s (baseline: 120ms)
  - Deadlocks: 15 in last 5 minutes

User Impact:
- Estimated affected users: ~5,000 (23% of active users)
- Failed transactions: 1,247 in last 10 minutes
- Geographic scope: Global

Timeline:
14:30:00 - Normal operation
14:30:45 - First error spike detected
14:31:30 - Database connection saturation
14:32:00 - Alert triggered: API error rate threshold
14:32:17 - Incident detection complete

Recent Changes:
- Deployment: api-service v2.4.1 at 14:25:00
- Config change: Database connection pool at 13:45:00

Initial Hypothesis:
Database connection leak in recent deployment causing
connection pool exhaustion and cascading API failures.

Recommended Actions:
1. IMMEDIATE: Rollback api-service to v2.4.0
2. Monitor database connection recovery
3. Verify error rate returns to baseline
4. Begin detailed root cause analysis

Next Step: Run /ops-diagnose for detailed analysis
```

### /ops-diagnose
Perform root cause analysis on identified issues.

```
/ops-diagnose [incident-id]
```

**Incident ID:**
- `current` - Active incident (default)
- `INC-2024-001` - Specific incident
- `latest` - Most recent incident

**Example usage:**

```bash
# Diagnose current active incident
/ops-diagnose

# Analyze specific past incident
/ops-diagnose INC-2024-001

# Review most recent incident
/ops-diagnose latest
```

**Actions performed:**
- Gather comprehensive incident data
- Construct detailed timeline with correlations
- Analyze service dependencies and interactions
- Review deployment and configuration changes
- Examine application logs and stack traces
- Trace request flows through distributed system
- Test hypotheses with evidence
- Identify root cause with supporting data
- Document findings and contributing factors

**Example output:**
```
Root Cause Analysis Report
===========================

Incident: INC-2024-001
Status: Resolved
Duration: 18 minutes 32 seconds
Impact: 5,247 users, $12,400 estimated revenue loss

Root Cause:
Database connection leak introduced in api-service v2.4.1
caused by improper connection closure in error handling path.

Timeline Analysis:
------------------
14:25:00 - Deployment of api-service v2.4.1 completed
14:30:45 - First connection leak detected (not alerted)
14:31:30 - Connection pool exhausted (100/100 connections)
14:32:00 - API error rate exceeded threshold, alert triggered
14:32:17 - Incident detection completed
14:33:45 - Rollback initiated to v2.4.0
14:35:20 - Rollback completed, traffic shifting
14:38:15 - Connection pool recovered to normal levels
14:43:32 - Error rate returned to baseline, incident resolved

Root Cause Details:
-------------------
Code Analysis:
File: src/api/handlers/user.js
Lines: 234-256
Issue: Database connection not released in catch block

Before (v2.4.1 - BUGGY):
```javascript
async function getUserData(userId) {
  const conn = await db.getConnection();
  try {
    const user = await conn.query('SELECT * FROM users WHERE id = ?', [userId]);
    conn.release();
    return user;
  } catch (error) {
    logger.error('Failed to get user data', error);
    throw error; // Connection not released!
  }
}
```

After (Fix):
```javascript
async function getUserData(userId) {
  const conn = await db.getConnection();
  try {
    const user = await conn.query('SELECT * FROM users WHERE id = ?', [userId]);
    return user;
  } catch (error) {
    logger.error('Failed to get user data', error);
    throw error;
  } finally {
    conn.release(); // Always release connection
  }
}
```

Contributing Factors:
1. Code review missed error path testing
2. Integration tests didn't cover error scenarios
3. No connection pool monitoring alerts
4. Canary deployment window too short (5 minutes)

5 Whys Analysis:
----------------
1. Why did the API fail?
   → Database connection pool was exhausted

2. Why was the connection pool exhausted?
   → Connections were being leaked

3. Why were connections being leaked?
   → Error handling code didn't release connections

4. Why didn't error handling release connections?
   → Developer forgot to add finally block

5. Why wasn't this caught before production?
   → Code review and tests didn't cover error paths

Prevention Measures:
--------------------
1. IMMEDIATE (Today):
   - Add connection pool utilization alerts
   - Extend canary deployment to 30 minutes
   - Deploy connection leak detector to staging

2. SHORT-TERM (This Week):
   - Add error path test coverage requirement (>80%)
   - Create code review checklist for resource cleanup
   - Implement automatic connection leak detection

3. LONG-TERM (This Month):
   - Add static analysis for resource leak detection
   - Implement connection pool monitoring dashboard
   - Create runbook for connection pool issues
   - Team training on resource management patterns

Action Items:
-------------
[x] INC-001-1: Deploy hotfix v2.4.2 with connection leak fix
    Owner: @dev-team | Due: Today | Status: Complete

[ ] INC-001-2: Add connection pool alerts to Grafana
    Owner: @ops-team | Due: Today 5pm | Status: In Progress

[ ] INC-001-3: Write postmortem document
    Owner: @incident-commander | Due: Tomorrow | Status: Not Started

[ ] INC-001-4: Update code review checklist
    Owner: @engineering-lead | Due: 2 days | Status: Not Started

[ ] INC-001-5: Add error path coverage to CI/CD
    Owner: @qa-team | Due: 3 days | Status: Not Started

Next Step: Run /ops-remediate to implement fixes
```

### /ops-remediate
Execute automated remediation for known issue patterns.

```
/ops-remediate [action]
```

**Actions:**
- `auto` - Automatic action selection (default)
- `rollback` - Rollback recent deployment
- `scale` - Scale resources up/down
- `restart` - Restart affected services
- `circuit-breaker` - Activate circuit breakers

**Example usage:**

```bash
# Auto-select remediation based on analysis
/ops-remediate

# Execute rollback
/ops-remediate rollback

# Scale up resources
/ops-remediate scale

# Restart services
/ops-remediate restart
```

**Actions performed:**
- Analyze incident type and pattern matching
- Validate safety conditions and prerequisites
- Execute appropriate remediation strategy
- Monitor impact in real-time
- Verify resolution metrics
- Document actions taken
- Update runbooks with learnings
- Notify stakeholders of resolution

**Example output:**
```
Automated Remediation Execution
================================

Action Selected: ROLLBACK
Reason: High error rate + recent deployment correlation
Confidence: 98% (pattern match: deployment-induced errors)

Pre-Flight Checks:
------------------
[✓] Previous version available (v2.4.0)
[✓] Database migrations backward compatible
[✓] Traffic can be safely shifted
[✓] Rollback window within 30 minutes
[✓] On-call engineer notified
[✓] Incident channel active

Rollback Plan:
--------------
1. Prepare previous deployment (v2.4.0)
2. Deploy to canary instances (10% traffic)
3. Monitor canary metrics (2 minutes)
4. Progressive rollout (10% → 50% → 100%)
5. Verify full resolution
6. Document and cleanup

Execution Log:
--------------
14:33:45 - Rollback initiated
14:33:52 - Previous version prepared
14:34:10 - Canary deployment complete (10% traffic)
14:34:15 - Canary metrics: Error rate 0.08% ✓
14:34:20 - Scaling to 50% traffic
14:34:45 - Metrics stable at 50%
14:35:00 - Scaling to 100% traffic
14:35:20 - Rollback complete
14:35:30 - Connection pool recovering
14:36:00 - Connection pool at 45/100 (healthy)
14:37:15 - Error rate: 0.09% (baseline restored) ✓
14:38:32 - All metrics returned to baseline

Results:
--------
Status: SUCCESS
Total Duration: 4 minutes 47 seconds
User Impact Minimized: Yes
Error Rate: 12.3% → 0.09%
Response Time P95: 8.2s → 445ms
Connection Pool: 100/100 → 42/100

Verification:
-------------
[✓] Error rate below 0.2% for 5+ minutes
[✓] Response times within SLO
[✓] No new alerts triggered
[✓] Database connections healthy
[✓] User impact ceased
[✓] Synthetic monitors passing

Post-Remediation Actions:
--------------------------
1. Incident marked as mitigated
2. Root cause analysis in progress
3. Postmortem scheduled for tomorrow 10am
4. Action items created and assigned
5. Runbook updated with this scenario
6. Team notification sent

Runbook Created:
----------------
Title: "Database Connection Pool Exhaustion - Deployment Rollback"
Location: runbooks/database-connection-pool-exhaustion.md
Automation Level: 80% automated
Next Review: 30 days

Communication Sent:
-------------------
- Status page updated: "Incident resolved"
- Customer email: Apologizing for 18min disruption
- Internal Slack: Technical summary and learnings
- Executive brief: Impact and resolution summary
- Partner notification: Service restored

Incident Status: RESOLVED
Total Incident Duration: 18 minutes 32 seconds
MTTR Target: < 30 minutes ✓ ACHIEVED

Next Steps:
-----------
1. Complete postmortem within 48 hours
2. Implement prevention measures from RCA
3. Update monitoring and alerting
4. Test remediation automation in staging
5. Share learnings with engineering team
```

## Maturity Targets

The agent optimizes toward these incident response targets:

| Metric | Target | Industry Average |
|--------|--------|------------------|
| MTTD (Mean Time to Detect) | < 5 min | 15-60 min |
| MTTA (Mean Time to Acknowledge) | < 5 min | 5-15 min |
| MTTR (Mean Time to Recover) | < 30 min | 1-4 hours |
| Postmortem Completion | < 48 hours | 1-2 weeks |
| Runbook Coverage | > 80% | 40-60% |
| Auto-Remediation Rate | > 40% | 10-20% |
| Alert Accuracy | > 95% | 70-85% |
| Recurring Incident Rate | < 10% | 20-30% |

## Use Cases

### 1. API Service Degradation
**Problem**: Sudden spike in API error rates affecting thousands of users.

**Solution**:
```bash
/ops-detect api-service
/ops-diagnose current
/ops-remediate auto
```

**Results**:
- Detected in 2 minutes (MTTD)
- Root cause identified in 6 minutes
- Automated rollback in 5 minutes
- Total MTTR: 18 minutes
- User impact minimized
- Prevention measures implemented

### 2. Database Performance Crisis
**Problem**: Database query times spiking, causing timeouts across services.

**Solution**:
- Detection through automated monitoring
- Diagnosis identifying slow query pattern
- Automated remediation: query cache warming + connection pool adjustment
- Emergency scaling of database replicas

**Results**:
- MTTD: 3 minutes
- MTTR: 12 minutes
- No data loss
- Runbook created
- Long-term optimization planned

### 3. Memory Leak Detection
**Problem**: Gradual memory increase causing intermittent crashes.

**Solution**:
- Anomaly detection identifies trend
- Distributed tracing reveals leak location
- Auto-remediation: scheduled restarts while fix developed
- Permanent fix deployed

**Results**:
- Early detection prevented major outage
- Coordinated response across teams
- Temporary mitigation bought time
- Permanent fix validated in staging

### 4. Third-Party Service Outage
**Problem**: External payment provider experiencing downtime.

**Solution**:
- Circuit breaker auto-activated
- Fallback to secondary provider
- User communication automated
- Recovery monitoring continuous

**Results**:
- Zero user-facing downtime
- Seamless failover
- Automatic recovery when primary restored
- SLA maintained

### 5. Deployment-Induced Regression
**Problem**: New deployment causes errors in edge case scenario.

**Solution**:
```bash
/ops-detect
/ops-diagnose current
/ops-remediate rollback
```

**Results**:
- Canary analysis detected issue
- Automatic rollback initiated
- 5-minute MTTR
- Root cause identified
- Fix developed and tested
- Successful redeployment

## MCP Server Configuration

The agent uses four MCP servers for comprehensive incident response:

### Filesystem Server (Required)
Access logs, runbooks, incident reports, and monitoring configurations.

```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
  }
}
```

**Used for**:
- Reading application logs
- Accessing runbooks and procedures
- Reviewing incident reports
- Analyzing monitoring configurations
- Reading deployment manifests

### GitHub Server (Optional)
Track incidents and manage postmortems.

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
- Creating incident tracking issues
- Managing postmortem documents
- Tracking action items
- Coordinating team responses
- Reviewing deployment history

### Context7 Server (Optional)
Access incident response playbooks and best practices.

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
- Accessing SRE playbooks
- Learning troubleshooting techniques
- Understanding monitoring patterns
- Researching best practices
- Reviewing similar incidents

### Fetch Server (Optional)
Query monitoring APIs and health endpoints.

```json
{
  "fetch": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-fetch"]
  }
}
```

**Used for**:
- Querying Prometheus/Grafana APIs
- Accessing alert system data
- Checking service health endpoints
- Retrieving metrics in real-time
- Monitoring deployment status

## Integration with Other Agents

### sre-engineer
Collaborate on reliability improvements, SLO definition, and proactive monitoring.

### devops-engineer
Support monitoring infrastructure setup and automation development.

### cloud-architect
Work on resilient architecture design and disaster recovery planning.

### deployment-engineer
Guide on safe deployment practices and automated rollback procedures.

### security-engineer
Help with security incident response and vulnerability remediation.

### platform-engineer
Assist with platform stability and self-healing system design.

### network-engineer
Partner on network issue diagnosis and resolution.

### database-administrator
Coordinate on database incident response and performance optimization.

## Best Practices

### Incident Response Approach
1. **Stay Calm**: Clear thinking under pressure is critical
2. **Communicate Early**: Update stakeholders before you have all answers
3. **Restore First**: Fix the problem, then understand it
4. **Document Everything**: Timeline, actions, decisions, learnings
5. **Avoid Assumptions**: Verify each hypothesis with data
6. **Know When to Escalate**: Don't hesitate to get help
7. **Learn from Every Incident**: Continuous improvement mindset
8. **Blameless Culture**: Focus on systems, not individuals

### Common Response Patterns

#### Detection
1. Automated monitoring triggers alert
2. On-call engineer acknowledges (MTTA < 5min)
3. Initial triage and impact assessment
4. Incident channel created
5. Stakeholder notification
6. Investigation begins

#### Diagnosis
1. Gather symptoms from monitoring
2. Construct timeline of events
3. Correlate with recent changes
4. Review service dependencies
5. Examine logs and traces
6. Formulate and test hypotheses
7. Identify root cause

#### Remediation
1. Assess remediation options
2. Validate safety conditions
3. Execute remediation plan
4. Monitor impact in real-time
5. Verify resolution
6. Document actions
7. Communicate resolution

#### Learning
1. Schedule postmortem within 48 hours
2. Blameless timeline review
3. Identify contributing factors
4. Define action items with owners
5. Track action item completion
6. Share learnings with team
7. Update runbooks and automation

## Getting Started

1. **Install the agent** in your Claude Code environment
2. **Configure MCP servers** (at minimum, filesystem server)
3. **Set up monitoring** (Prometheus, Grafana, or your preferred stack)
4. **Define SLIs/SLOs** for your critical services
5. **Create initial runbooks** for common scenarios
6. **Test incident response** with game day exercises
7. **Establish on-call rotation** and escalation policies
8. **Run first incident** with `/ops-detect`, `/ops-diagnose`, `/ops-remediate`

## Example Workflow

```bash
# Step 1: Detect production issue
/ops-detect api-service

# Step 2: Diagnose root cause
/ops-diagnose current

# Step 3: Execute automated remediation
/ops-remediate auto

# Step 4: Verify resolution
# Agent monitors metrics and confirms

# Step 5: Schedule postmortem
# Agent creates GitHub issue with template

# Step 6: Track action items
# Agent tracks completion of prevention measures

# Step 7: Update runbooks
# Agent documents new patterns and procedures

# Step 8: Share learnings
# Agent prepares summary for team
```

## Success Metrics

Track these metrics to measure incident response effectiveness:

- **MTTD**: Mean time to detect < 5 minutes
- **MTTA**: Mean time to acknowledge < 5 minutes
- **MTTR**: Mean time to recover < 30 minutes
- **Alert Accuracy**: > 95% true positive rate
- **Runbook Coverage**: > 80% of incidents covered
- **Auto-Remediation**: > 40% of incidents auto-resolved
- **Postmortem Timeliness**: < 48 hours completion
- **Action Item Completion**: > 90% within deadline
- **Recurring Incidents**: < 10% recurrence rate
- **On-Call Satisfaction**: > 4.0/5.0 rating

## Advanced Features

### Automated Remediation
- Pattern recognition for common issues
- Self-healing scripts with safety checks
- Automated rollback on detection
- Circuit breaker activation
- Dynamic scaling responses

### Predictive Alerting
- Anomaly detection with ML
- Trend analysis and forecasting
- Early warning indicators
- Capacity planning alerts
- Proactive notifications

### Chaos Engineering
- Controlled failure injection
- Resilience testing
- Game day exercises
- Runbook validation
- Team readiness assessment

### Knowledge Management
- Searchable incident database
- Pattern recognition and trends
- Solution library
- Automated runbook generation
- Learning capture and sharing

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT
