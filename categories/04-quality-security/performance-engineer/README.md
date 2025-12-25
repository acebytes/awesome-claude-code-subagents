# Performance Engineer Agent

> Expert performance engineer specializing in system optimization, bottleneck identification, and scalability engineering

## Overview

The Performance Engineer agent specializes in optimizing system performance, identifying bottlenecks, and ensuring scalability. It masters performance testing, profiling, and tuning across applications, databases, and infrastructure to achieve optimal response times and resource efficiency.

## Capabilities

### Primary Skills
- Performance testing (load, stress, spike, soak, scalability)
- Bottleneck analysis and identification
- Application profiling and optimization
- Database query optimization and indexing
- Infrastructure tuning and configuration
- Caching strategy implementation
- Load testing and capacity planning
- Performance monitoring and alerting

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write performance reports and profiles |
| github | Track performance issues and improvements |
| context7 | Access codebase context for performance analysis |
| postgres | Analyze and optimize database query performance |
| memory | Maintain performance baselines and optimization context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/perf-test` | Execute comprehensive performance testing suite |
| `/profile` | Profile application to identify hotspots and bottlenecks |
| `/optimize` | Analyze and implement performance optimizations |
| `/capacity-plan` | Project capacity needs and scaling requirements |

### Example Prompts

```
Our API response time is too slow. Profile and optimize the critical endpoints.
```

```
Run load tests to verify our system can handle 10x traffic
```

```
Optimize slow database queries and improve overall database performance
```

```
Analyze memory usage and identify potential memory leaks
```

## Performance Testing Methodology

### Load Testing
- **Normal Load**: Simulate expected user traffic patterns
- **Stress Testing**: Find system breaking points
- **Spike Testing**: Test sudden traffic bursts
- **Soak Testing**: Identify memory leaks and degradation
- **Scalability Testing**: Verify linear scaling

### Profiling Techniques
- CPU profiling for hotspot identification
- Memory profiling for leak detection
- I/O analysis for bottleneck identification
- Database query analysis and optimization
- Network latency measurement

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for issue tracking
- `DATABASE_URL` - PostgreSQL connection for query analysis

### CLI Tools
- Node.js 18+
- npx
- Performance testing tools (k6, JMeter, Locust, etc.)

## Performance Targets

The agent aims to achieve:
- **Response Time**: p50 < 200ms, p95 < 500ms, p99 < 1s
- **Throughput**: Handle 10x peak load
- **Resource Efficiency**: < 70% CPU/memory at peak
- **Error Rate**: < 0.1% under normal load
- **Scalability**: Linear scaling with resources

## Optimization Strategies

### Application Level
- Algorithm and data structure optimization
- Code-level performance improvements
- Async processing and parallelization
- Batch operations for efficiency
- Resource pooling

### Database Level
- Query optimization and indexing
- Execution plan analysis
- Connection pooling
- Query result caching
- Partitioning strategies

### Infrastructure Level
- OS kernel parameter tuning
- Network configuration optimization
- Storage performance tuning
- Container resource limits
- Cloud instance sizing

### Caching Strategies
- Application-level caching (Redis, Memcached)
- Database query caching
- CDN for static assets
- API response caching
- Browser caching headers

## Best Practices

1. **Measure First**: Always establish baselines before optimizing
2. **Focus on Bottlenecks**: Optimize the critical path first
3. **Test Thoroughly**: Validate improvements with load tests
4. **Monitor Continuously**: Set up comprehensive monitoring
5. **Document Changes**: Track optimizations and their impact
6. **Capacity Planning**: Project future resource needs
7. **Regression Testing**: Prevent performance degradation

## Collaboration

Works closely with:
- **Backend Developer**: Code-level optimizations
- **Database Administrator**: Query and schema optimization
- **DevOps Engineer**: Infrastructure tuning
- **Architect Reviewer**: Performance architecture design
- **QA Expert**: Performance test requirements
- **SRE Engineer**: SLI/SLO definition

## Common Performance Patterns

### Problems Identified
- N+1 query problems
- Memory leaks
- Connection pool exhaustion
- Cache misses
- Synchronous blocking operations
- Inefficient algorithms
- Resource contention
- Network latency

### Solutions Implemented
- Query optimization and batching
- Memory leak fixes
- Connection pooling
- Caching implementation
- Async processing
- Algorithm improvements
- Lock optimization
- CDN and edge caching
