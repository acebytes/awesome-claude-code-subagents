# Legacy Modernizer Agent

Expert legacy system modernizer specializing in incremental migration strategies and risk-free modernization. Masters refactoring patterns, technology updates, and business continuity with focus on transforming legacy systems into modern, maintainable architectures without disrupting operations.

## Overview

The Legacy Modernizer agent helps transform aging systems into modern architectures through systematic assessment, planning, and incremental migration. It prioritizes business continuity, risk mitigation, and zero-downtime deployments while delivering measurable improvements in performance, security, and maintainability.

## Key Features

- **Comprehensive Assessment** - Analyzes code quality, technical debt, dependencies, and security vulnerabilities
- **Strategic Planning** - Creates phased modernization roadmaps with risk assessment and resource estimation
- **Incremental Migration** - Implements strangler fig pattern and other proven migration strategies
- **Risk Mitigation** - Uses feature flags, canary deployments, and rollback procedures
- **Performance Optimization** - Identifies bottlenecks and implements optimization strategies
- **Security Hardening** - Updates authentication, encryption, and dependency vulnerabilities
- **Knowledge Preservation** - Documents legacy business rules and architectural decisions
- **Team Enablement** - Provides training and best practices for modern patterns

## Installation

1. Copy the agent directory to your Claude Desktop configuration:
```bash
cp -r legacy-modernizer ~/.config/claude-desktop/agents/
```

2. Configure MCP servers in `mcp-config.json`:
   - Add GitHub personal access token for repository management
   - Add Context7 API key for documentation queries (optional)

3. Restart Claude Desktop to load the agent

## MCP Servers

### Required
- **filesystem** - Access legacy codebase files for assessment and migration

### Recommended
- **github** - Manage modernization branches, PRs, and team collaboration
- **context7** - Query legacy documentation and understand historical context

## Slash Commands

### /legacy-assess
Perform comprehensive legacy system assessment.

**What it does:**
- Analyzes codebase structure and age
- Identifies technical debt and dependencies
- Evaluates security vulnerabilities
- Measures performance baselines
- Documents architecture and gaps
- Generates detailed assessment report

**When to use:**
- Starting a new modernization project
- Auditing existing legacy systems
- Prioritizing technical debt
- Planning migration budgets

**Example:**
```
/legacy-assess
```

### /legacy-plan
Create detailed modernization plan.

**What it does:**
- Reviews assessment findings
- Prioritizes modernization targets
- Defines migration strategy (strangler fig, parallel run, etc.)
- Estimates resources and timeline
- Identifies risks and mitigation strategies
- Creates phased roadmap with success metrics

**When to use:**
- After completing assessment
- Before starting migration work
- When presenting to stakeholders
- Planning sprint schedules

**Example:**
```
/legacy-plan
```

### /legacy-migrate
Execute incremental migration step.

**What it does:**
- Selects next migration target from plan
- Creates feature flags if needed
- Implements strangler fig pattern
- Adds comprehensive test coverage
- Deploys with monitoring
- Validates migration success
- Documents changes
- Updates progress tracking

**When to use:**
- Executing planned migration phases
- Modernizing specific modules
- Refactoring legacy components
- Deploying incremental updates

**Example:**
```
/legacy-migrate
```

## Workflows

### 1. System Analysis
Assess legacy system and create modernization foundation.

**Steps:**
1. Run `/legacy-assess` to analyze the codebase
2. Review code quality, dependencies, and risks
3. Document findings and gaps
4. Establish performance baselines
5. Identify security vulnerabilities
6. Map business dependencies
7. Generate comprehensive assessment report

**Outputs:**
- Assessment report with prioritized issues
- Technical debt measurements
- Dependency graph
- Security audit results
- Performance baseline metrics

### 2. Modernization Planning
Create strategic roadmap for incremental migration.

**Steps:**
1. Run `/legacy-plan` based on assessment
2. Prioritize modules for migration
3. Select migration strategies (strangler fig, parallel run, etc.)
4. Define success metrics and KPIs
5. Estimate resources and timeline
6. Create risk mitigation plans
7. Get stakeholder approval

**Outputs:**
- Phased modernization roadmap
- Resource estimates and timeline
- Risk assessment with mitigations
- Success metrics and KPIs
- Communication plan

### 3. Incremental Migration
Execute migration in safe, measurable steps.

**Steps:**
1. Select next module from roadmap
2. Run `/legacy-migrate` for targeted module
3. Implement with feature flags
4. Add comprehensive tests (>80% coverage)
5. Deploy with canary strategy
6. Monitor performance and errors
7. Validate success metrics
8. Document and communicate progress

**Outputs:**
- Migrated module with tests
- Performance improvements
- Security vulnerability fixes
- Migration documentation
- Progress report

## Migration Strategies

### Strangler Fig Pattern
Gradually replace legacy functionality by wrapping it with new code.

**Best for:**
- Large monolithic applications
- Systems that can't have downtime
- Incremental team training
- Risk-averse organizations

**Examples:**
- API gateway introduction
- Service extraction
- Database splitting
- UI component migration

### Branch by Abstraction
Create abstraction layer, implement new version, switch gradually.

**Best for:**
- Replacing core algorithms
- Updating frameworks
- Database migrations
- Infrastructure changes

### Parallel Run
Run old and new systems simultaneously, compare results.

**Best for:**
- Financial systems
- Critical business logic
- Data validation
- Compliance requirements

## Refactoring Patterns

- **Extract Service** - Pull functionality into microservice
- **Introduce Facade** - Simplify complex legacy interfaces
- **Replace Algorithm** - Swap old implementation with modern approach
- **Encapsulate Legacy** - Wrap legacy code with clean API
- **Introduce Adapter** - Bridge legacy and modern patterns
- **Extract Interface** - Define contracts for legacy components
- **Replace Inheritance** - Convert to composition patterns
- **Simplify Conditionals** - Replace complex logic with clear patterns

## Best Practices

### Zero-Downtime Deployments
- Use feature flags for gradual rollout
- Implement blue-green deployments
- Deploy with canary strategy
- Maintain rollback capability

### Test Coverage
- Achieve >80% coverage before migration
- Add characterization tests for legacy behavior
- Implement integration tests
- Create performance benchmarks

### Performance Monitoring
- Establish baselines before changes
- Monitor continuously during migration
- Track key business metrics
- Set up alerting for degradation

### Documentation
- Document legacy business rules
- Preserve architectural decisions
- Create runbooks for operations
- Update team knowledge base

### Team Collaboration
- Work with architect-reviewer on design
- Support refactoring-specialist on code improvements
- Coordinate with security-auditor on vulnerabilities
- Guide devops-engineer on deployment
- Help qa-expert on testing strategies

## Success Metrics

- **Test Coverage** - Target >80% coverage
- **Performance** - Measure improvements (latency, throughput)
- **Security** - Track vulnerabilities fixed
- **Technical Debt** - Monitor debt reduction
- **Deployment Frequency** - Increase deployment cadence
- **Mean Time to Recovery** - Reduce recovery time
- **Business Value** - Deliver measurable outcomes

## Integration with Other Agents

- **architect-reviewer** - Collaborate on modern architecture design
- **refactoring-specialist** - Support code improvement efforts
- **security-auditor** - Fix vulnerabilities during migration
- **devops-engineer** - Modernize deployment pipelines
- **qa-expert** - Implement comprehensive testing strategies
- **documentation-engineer** - Preserve and update documentation
- **database-optimizer** - Optimize data layer during migration
- **product-manager** - Prioritize based on business value

## Example Usage

### Assessment Phase
```
User: I have a 10-year-old Java monolith that needs modernization.

Agent: I'll perform a comprehensive legacy assessment. Let me analyze
your codebase structure, dependencies, and technical debt.

[Runs /legacy-assess]

Assessment complete:
- 245K lines of code across 1,234 classes
- Using Java 8 (EOL), Spring 3.x (outdated)
- 156 security vulnerabilities identified
- Test coverage: 12%
- 47 deprecated dependencies
- Monolithic architecture with tight coupling

Key risks:
1. Security vulnerabilities in dependencies
2. Low test coverage prevents safe refactoring
3. Tight coupling makes module extraction difficult
4. Performance bottlenecks in data access layer

Recommended approach: Strangler fig pattern with incremental service extraction
```

### Planning Phase
```
User: Create a modernization plan based on the assessment.

Agent: I'll create a phased modernization roadmap with risk mitigation.

[Runs /legacy-plan]

Modernization Plan (12 months, 3 phases):

Phase 1 (Months 1-3): Foundation
- Update Java to 17, Spring to 6.x
- Increase test coverage to 80%
- Fix critical security vulnerabilities
- Establish CI/CD pipeline
- Set up monitoring and observability

Phase 2 (Months 4-8): Service Extraction
- Extract authentication service
- Extract user management service
- Extract payment processing service
- Implement API gateway
- Add feature flags

Phase 3 (Months 9-12): Optimization
- Database optimization and caching
- Performance tuning
- UI modernization
- Cloud migration preparation
- Team training

Success Metrics:
- Zero production incidents during migration
- Test coverage >80%
- Performance improvement >40%
- All critical vulnerabilities fixed
```

### Migration Phase
```
User: Start migrating the authentication module.

Agent: I'll execute incremental migration of authentication using strangler fig pattern.

[Runs /legacy-migrate]

Migration Steps:
1. Created feature flag: auth_service_v2
2. Implemented new authentication service with OAuth2/OIDC
3. Added comprehensive tests (coverage: 87%)
4. Deployed behind feature flag (0% traffic)
5. Canary deployment (5% -> 25% -> 50% -> 100%)
6. Validated performance (latency improved 52%)
7. Documented changes and updated runbooks

Results:
- Authentication migrated successfully
- Zero production incidents
- Performance improved by 52%
- Security vulnerabilities eliminated
- Test coverage: 87%

Next Steps: Begin user management service extraction
```

## Tips

1. **Start Small** - Begin with low-risk modules to build confidence
2. **Test First** - Add comprehensive tests before refactoring
3. **Measure Everything** - Track metrics before and after changes
4. **Communicate Often** - Keep stakeholders informed of progress
5. **Plan for Rollback** - Always maintain rollback capability
6. **Document Decisions** - Preserve knowledge for future team members
7. **Celebrate Wins** - Acknowledge incremental progress
8. **Stay Incremental** - Avoid big-bang rewrites

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT License - See LICENSE file for details
