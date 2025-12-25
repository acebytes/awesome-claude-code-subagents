# Architect Reviewer Agent

> Expert architecture reviewer specializing in system design validation, architectural patterns, and technical decision assessment

## Overview

The Architect Reviewer agent is a senior architecture reviewer with expertise in evaluating system designs, architectural decisions, and technology choices. It masters scalability analysis, technology stack evaluation, and evolutionary architecture with focus on building sustainable, evolvable systems that meet both current and future needs.

## Capabilities

### Primary Skills
- **System Design Review**: Component boundaries, data flow, service contracts, dependency management
- **Architectural Patterns**: Microservices, DDD, event-driven, CQRS, hexagonal architecture
- **Scalability Assessment**: Horizontal/vertical scaling, partitioning, load distribution, caching
- **Technology Evaluation**: Stack appropriateness, maturity, team fit, long-term viability
- **Integration Patterns**: API design, messaging, event streaming, service discovery
- **Security Architecture**: Authentication, authorization, encryption, compliance, threat modeling
- **Performance Architecture**: Response time, throughput, resource utilization, optimization
- **Technical Debt**: Architecture smells, modernization roadmap, evolution strategy

### Supported Technologies
JavaScript, TypeScript, Python, Java, Go, C#, Ruby, Rust, Kotlin, Scala

### Architecture Patterns
Microservices, Domain-Driven Design, Event-Driven Architecture, CQRS, Hexagonal Architecture, Clean Architecture, Service Mesh, API Gateway, Event Sourcing, Saga Pattern

### MCP Server Integrations

| Server | Purpose | Required |
|--------|---------|----------|
| filesystem | Read/write architecture diagrams and design documents | Yes |
| github | Access architecture documents and ADRs | Yes |
| context7 | Understand system architecture and design patterns | No |
| memory | Track architectural decisions and evolution history | No |

## Usage

### Slash Commands

| Command | Description | Example |
|---------|-------------|---------|
| `/arch-review` | Comprehensive architecture review | `/arch-review` |
| `/scalability-check` | Analyze scalability architecture | `/scalability-check` |
| `/tech-stack` | Evaluate technology choices | `/tech-stack` |
| `/design-patterns` | Review pattern usage | `/design-patterns` |

### Example Prompts

**Microservices Architecture Review**
```
Review the microservices architecture for the e-commerce platform
```
Evaluates service boundaries, communication patterns, data ownership, deployment independence, and provides recommendations for optimization.

**Scalability Assessment**
```
Assess the scalability of our current database architecture
```
Analyzes horizontal/vertical scaling capability, identifies bottlenecks, reviews partitioning strategies, and provides capacity planning guidance.

**Technology Stack Evaluation**
```
Evaluate our technology stack for the new analytics platform
```
Compares alternatives, assesses technology maturity, team expertise fit, community support, licensing, and long-term viability.

**Event-Driven Architecture Review**
```
Review the event-driven architecture design
```
Validates event sourcing implementation, CQRS patterns, message flow, consistency guarantees, and provides improvement recommendations.

**Security Architecture Analysis**
```
Analyze the security architecture for our API gateway
```
Reviews authentication mechanisms, authorization models, data encryption, network security, threat modeling, and compliance alignment.

## Requirements

### API Keys

#### Required
- `GITHUB_TOKEN` - GitHub Personal Access Token for accessing architecture documentation
  - Obtain at: https://github.com/settings/tokens
  - Scopes needed: `repo`, `read:org`

#### Optional
- `UPSTASH_VECTOR_REST_URL` - Upstash Vector database URL for architecture context
- `UPSTASH_VECTOR_REST_TOKEN` - Upstash Vector database token
  - Obtain at: https://upstash.com

### CLI Tools
- Node.js 18+
- npx
- git

## Architecture Review Process

### 1. Context Gathering
- Review architecture documentation (ADRs, diagrams, design docs)
- Understand system requirements and constraints
- Identify business goals and quality attributes
- Analyze current pain points and challenges

### 2. Design Analysis
- Evaluate component boundaries and responsibilities
- Map data flows and interactions
- Review service contracts and APIs
- Assess dependency management
- Analyze coupling and cohesion

### 3. Pattern Review
- Validate architectural pattern selection
- Check pattern implementation correctness
- Assess pattern appropriateness for context
- Identify anti-patterns and smells
- Recommend pattern improvements

### 4. Scalability Assessment
- Analyze horizontal scaling capability
- Evaluate vertical scaling limits
- Review data partitioning strategy
- Assess load balancing approach
- Validate caching layers
- Identify performance bottlenecks
- Plan capacity and growth

### 5. Technology Evaluation
- Assess technology appropriateness
- Review stack maturity and stability
- Evaluate team expertise alignment
- Analyze community support
- Consider licensing implications
- Calculate total cost of ownership
- Assess migration complexity
- Evaluate long-term viability

### 6. Integration Review
- Review API design quality (REST, GraphQL, gRPC)
- Validate message queue patterns
- Assess event-driven architecture
- Check service discovery mechanisms
- Review circuit breaker implementation
- Validate retry and timeout strategies
- Analyze data synchronization
- Review transaction handling

### 7. Security Architecture
- Validate authentication design
- Review authorization model (RBAC, ABAC)
- Check data encryption (at rest, in transit)
- Assess network security topology
- Review secret management
- Validate audit logging strategy
- Check compliance requirements
- Perform threat modeling

### 8. Performance Architecture
- Validate response time targets
- Review throughput requirements
- Assess resource utilization goals
- Evaluate caching strategy
- Review CDN implementation
- Analyze database optimization
- Check async processing design
- Validate batch operations

## Architecture Principles

The Architect Reviewer enforces these principles:

- **Separation of Concerns**: Clear component boundaries
- **Single Responsibility**: One reason to change
- **Interface Segregation**: Focused, minimal interfaces
- **Dependency Inversion**: Depend on abstractions
- **Open/Closed Principle**: Open for extension, closed for modification
- **DRY**: Eliminate architectural duplication
- **KISS**: Simplicity over complexity
- **YAGNI**: Build only what's needed now

## Quality Attributes Assessment

### Availability
- Uptime targets and SLAs
- Redundancy design
- Failover mechanisms
- Disaster recovery
- High availability patterns

### Reliability
- Error handling strategy
- Fault tolerance design
- Data consistency approach
- Transaction integrity
- Recovery procedures

### Performance
- Response time goals
- Throughput capacity
- Resource efficiency
- Scalability limits
- Bottleneck analysis

### Security
- Authentication strength
- Authorization granularity
- Data protection measures
- Network security design
- Compliance alignment

### Maintainability
- Code organization quality
- Documentation completeness
- Testing strategy
- Deployment automation
- Technical debt level

### Scalability
- Horizontal scaling design
- Vertical scaling capability
- Data partitioning approach
- Load distribution strategy
- Auto-scaling implementation

## Modernization Strategies

### Strangler Pattern
- Incremental replacement approach
- Parallel run capability
- Traffic routing strategy
- Legacy API facade
- Phased migration plan

### Evolutionary Architecture
- Fitness functions definition
- Architectural decision records
- Change management process
- Incremental evolution
- Reversibility design
- Experimentation framework
- Continuous validation

### Technical Debt Management
- Architecture smell detection
- Outdated pattern identification
- Technology obsolescence tracking
- Complexity metrics
- Risk-based prioritization
- Remediation roadmap
- Modernization phases

## Architecture Documentation

Reviews and validates:
- **C4 Model Diagrams**: Context, Container, Component, Code
- **Sequence Diagrams**: Key interaction flows
- **Data Flow Diagrams**: Data movement and transformation
- **Deployment Diagrams**: Infrastructure and runtime
- **ADRs (Architecture Decision Records)**: Design decisions and rationale
- **Quality Attribute Scenarios**: Non-functional requirements
- **API Specifications**: OpenAPI, GraphQL schemas
- **Runbooks**: Operational procedures

## Cloud Architecture Patterns

- **Cloud-Native Design**: Containerization, orchestration, service mesh
- **Multi-Cloud Strategy**: Vendor independence, data residency
- **Serverless Architecture**: FaaS, event-driven compute
- **Infrastructure as Code**: Terraform, CloudFormation
- **Container Orchestration**: Kubernetes patterns, auto-scaling
- **Cloud Storage**: Object, block, database services
- **Networking**: VPC design, load balancing, CDN
- **Cost Optimization**: Resource tagging, reserved instances

## Risk Assessment

The agent identifies and assesses:

### Technical Risks
- Technology maturity concerns
- Skill gap analysis
- Complexity management challenges
- Performance bottlenecks
- Security vulnerabilities
- Integration difficulties

### Business Risks
- Time to market delays
- Cost overruns
- Scope creep potential
- Vendor lock-in
- Regulatory compliance
- Market dynamics

### Operational Risks
- Deployment complexity
- Monitoring gaps
- Support challenges
- Disaster recovery gaps
- Data loss potential
- Service disruption risks

## Review Deliverables

1. **Architecture Assessment Report**: Comprehensive analysis of current design
2. **Risk Register**: Identified risks with severity ratings and mitigation strategies
3. **Recommendation Document**: Prioritized improvements and alternative approaches
4. **Scalability Analysis**: Capacity planning and growth projections
5. **Technology Evaluation**: Stack assessment with alternatives and comparisons
6. **Modernization Roadmap**: Phased evolution plan with milestones and timelines
7. **Architecture Decision Records**: Documented design decisions with context
8. **Quality Metrics Dashboard**: Non-functional requirement alignment tracking

## Best Practices

1. **Long-term Thinking**: Consider evolution and maintenance over 3-5 years
2. **Balanced Trade-offs**: No perfect solution, optimize for business goals
3. **Document Decisions**: ADRs capture context, alternatives, and rationale
4. **Embrace Standards**: Industry patterns reduce risk and complexity
5. **Plan for Change**: Build flexibility and reversibility into design
6. **Measure Quality**: Define fitness functions for key attributes
7. **Stakeholder Alignment**: Ensure architecture serves business needs
8. **Continuous Improvement**: Iterate based on feedback and metrics

## Collaboration

Works with:
- **code-reviewer** - Implementation quality and design pattern validation
- **security-auditor** - Security architecture and threat modeling
- **performance-engineer** - Performance optimization and bottleneck analysis
- **qa-expert** - Quality attribute validation and testing strategy
- **cloud-architect** - Cloud-native patterns and infrastructure design

Guides:
- **fullstack-developer** - Architecture implementation and pattern adoption
- **backend-developer** - Service design and integration patterns
- **devops-engineer** - Deployment architecture and automation

## Common Review Scenarios

### New System Design
```
Review the architecture design for our new microservices platform
```

### Legacy System Modernization
```
Create a modernization roadmap for our monolithic application
```

### Scalability Planning
```
Assess our architecture's ability to scale to 10x current traffic
```

### Technology Migration
```
Evaluate migrating from REST to event-driven architecture
```

### Security Architecture Audit
```
Review the security architecture for our payment processing system
```

### Cloud Migration Planning
```
Assess our application for cloud-native migration to AWS
```

## Metrics and Reporting

The agent tracks and reports:
- Architecture quality score (0-100)
- Technical debt percentage
- Scalability headroom (current vs capacity)
- Security posture rating
- Technology stack health
- Pattern compliance rate
- Documentation completeness
- Risk severity distribution

## Integration

The Architect Reviewer integrates with:
- GitHub repositories (documentation, ADRs)
- Architecture diagram tools (draw.io, PlantUML, Mermaid)
- Design documentation (Markdown, Confluence)
- API specifications (OpenAPI, GraphQL)
- Cloud platforms (AWS, Azure, GCP)
- Infrastructure as Code (Terraform, CloudFormation)
- Monitoring platforms (Datadog, New Relic)

## Tips for Effective Reviews

1. **Gather Complete Context**: Review all documentation before analysis
2. **Understand Business Goals**: Align architecture with business objectives
3. **Consider Future State**: Plan for 3-5 year evolution
4. **Balance Trade-offs**: Document pros/cons of architectural decisions
5. **Provide Alternatives**: Suggest multiple approaches with rationale
6. **Prioritize Recommendations**: Focus on high-impact improvements first
7. **Create Actionable Plans**: Break down roadmaps into concrete steps
8. **Track Decisions**: Maintain ADRs for all significant choices

## Support

For issues, questions, or contributions:
- Repository: https://github.com/VoltAgent/awesome-claude-code-subagents
- Issues: https://github.com/VoltAgent/awesome-claude-code-subagents/issues
- Discussions: https://github.com/VoltAgent/awesome-claude-code-subagents/discussions
