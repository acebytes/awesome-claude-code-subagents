# Database Optimizer Agent

Expert database optimizer specializing in query optimization, performance tuning, and scalability across multiple database systems. Masters execution plan analysis, index strategies, and system-level optimizations with focus on achieving peak database performance.

## Overview

The Database Optimizer agent is your expert partner for achieving optimal database performance across PostgreSQL, MySQL, MongoDB, Redis, and other database systems. It combines deep knowledge of query optimization, index design, and system tuning to deliver measurable performance improvements.

## Key Capabilities

- **Query Optimization**: Achieve sub-100ms query response times through execution plan analysis and query rewriting
- **Index Strategy**: Design and implement optimal indexes with 95%+ usage rates
- **Performance Tuning**: Optimize database configurations for OLTP, OLAP, and mixed workloads
- **Cache Optimization**: Increase cache hit rates to 90%+ through intelligent tuning
- **Lock Reduction**: Minimize lock contention and improve concurrency
- **Multi-Database**: Expert-level optimization across PostgreSQL, MySQL, MongoDB, Redis, and more
- **Scalability**: Design solutions that scale with data growth and traffic increases
- **Monitoring**: Implement comprehensive performance monitoring and alerting

## Performance Targets

- Query time: < 100ms
- Index usage: > 95%
- Cache hit rate: > 90%
- Lock waits: < 1%
- Bloat percentage: < 20%
- Replication lag: < 1 second
- Resource utilization: Optimized and balanced

## Quick Start

### Prerequisites

1. **Database Access**: Credentials and permissions for the database(s) to optimize
2. **MCP Servers**: Install and configure required MCP servers
3. **Monitoring**: Enable query statistics collection (pg_stat_statements, performance_schema, etc.)
4. **Logs**: Access to slow query logs and database error logs

### Installation

1. Clone the repository:
```bash
git clone https://github.com/claude-code-agent-marketplace.git
cd claude-code-agent-marketplace/categories/05-data-ai/database-optimizer
```

2. Configure MCP servers in your Claude Desktop config file:
```bash
# macOS
~/Library/Application Support/Claude/claude_desktop_config.json

# Windows
%APPDATA%\Claude\claude_desktop_config.json
```

3. Copy the MCP configuration from `mcp-config.json` and customize for your environment

### Environment Setup

Configure environment variables based on your database systems:

**PostgreSQL**:
```bash
export PGHOST=localhost
export PGPORT=5432
export PGDATABASE=your_database
export PGUSER=your_user
export PGPASSWORD=your_password
```

**MySQL**:
```bash
export MYSQL_HOST=localhost
export MYSQL_PORT=3306
export MYSQL_DATABASE=your_database
export MYSQL_USER=your_user
export MYSQL_PASSWORD=your_password
```

**Optional**:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=your_github_token
export CONTEXT7_API_KEY=your_context7_key
```

## Slash Commands

### /db-analyze

Comprehensive database performance analysis.

**Usage**:
```
/db-analyze [database_name] [options]
```

**What it does**:
- Identifies slow queries and performance bottlenecks
- Analyzes execution plans with EXPLAIN/EXPLAIN ANALYZE
- Reviews index usage and effectiveness
- Checks cache hit ratios and buffer efficiency
- Examines lock contention and wait events
- Analyzes I/O patterns and resource usage
- Generates detailed performance report with recommendations

**Example**:
```
/db-analyze production_db --slow-queries --cache-analysis
```

### /db-index

Recommend and implement optimal indexes.

**Usage**:
```
/db-index <table_or_query> [options]
```

**What it does**:
- Analyzes query patterns and access paths
- Identifies missing indexes causing table scans
- Reviews existing index usage statistics
- Designs covering, partial, and expression indexes
- Optimizes multi-column index ordering
- Identifies redundant indexes to remove
- Generates optimized index creation statements
- Validates performance improvements

**Example**:
```
/db-index orders_table --covering --partial
```

### /db-tune

Tune database configuration for optimal performance.

**Usage**:
```
/db-tune [database_system] [workload_type]
```

**What it does**:
- Assesses current configuration settings
- Analyzes workload type (OLTP/OLAP/mixed)
- Optimizes memory allocation (buffer pool, cache, work memory)
- Tunes checkpoint and WAL settings
- Configures connection pooling parameters
- Adjusts autovacuum/maintenance settings
- Optimizes parallel execution settings
- Generates tuned configuration with explanations

**Example**:
```
/db-tune postgresql oltp
```

## Common Use Cases

### 1. Slow Query Optimization

**Scenario**: API responses are slow due to database queries

**Steps**:
1. Use `/db-analyze` to identify slow queries
2. Review execution plans for bottlenecks
3. Use `/db-index` to add strategic indexes
4. Rewrite inefficient queries
5. Validate improvements with benchmarks

**Typical Results**:
- 80-90% query time reduction
- Improved user experience
- Reduced server load

### 2. Database Configuration Tuning

**Scenario**: Database running with default settings

**Steps**:
1. Use `/db-tune` to generate optimized configuration
2. Review workload characteristics
3. Apply memory and checkpoint optimizations
4. Configure appropriate connection pooling
5. Monitor performance improvements

**Typical Results**:
- 50-70% throughput increase
- Better resource utilization
- Reduced contention

### 3. Index Optimization

**Scenario**: Too many or too few indexes

**Steps**:
1. Use `/db-index` to analyze index usage
2. Identify unused and redundant indexes
3. Design new indexes for frequent queries
4. Implement covering indexes
5. Monitor index bloat

**Typical Results**:
- 95%+ index usage rate
- Faster query execution
- Reduced storage overhead

### 4. Cache Optimization

**Scenario**: Low cache hit rates causing I/O bottlenecks

**Steps**:
1. Use `/db-analyze` to check cache metrics
2. Review buffer pool configuration
3. Optimize query patterns for cache
4. Adjust cache sizing
5. Monitor cache effectiveness

**Typical Results**:
- 90%+ cache hit rate
- Reduced I/O operations
- Faster query response

## Supported Database Systems

### PostgreSQL
- Query optimization with EXPLAIN ANALYZE
- pg_stat_statements analysis
- Index design (B-tree, GIN, GiST, BRIN)
- Configuration tuning
- Vacuum and autovacuum optimization

### MySQL
- InnoDB optimization
- Query cache tuning (MySQL < 8.0)
- Index optimization
- Configuration tuning
- Slow query log analysis

### MongoDB
- Aggregation pipeline optimization
- Index strategies
- Query profiling
- Sharding optimization
- Collection design

### Redis
- Key design patterns
- Memory optimization
- Persistence tuning
- Data structure selection
- Eviction policy configuration

### Other Systems
- Cassandra: Partition design, compaction strategies
- ClickHouse: Columnar optimization, materialized views
- Elasticsearch: Mapping design, query DSL optimization
- Oracle: Execution plan analysis, optimizer hints

## MCP Server Configuration

### Required MCP Servers

**Filesystem Server**: Access configuration files, logs, and scripts
```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/db/configs", "/path/to/logs"]
  }
}
```

### Optional MCP Servers

**PostgreSQL Server**: Direct database access for PostgreSQL optimization
```json
{
  "postgres": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-postgres", "postgresql://localhost/postgres"],
    "env": {
      "PGHOST": "${PGHOST}",
      "PGUSER": "${PGUSER}",
      "PGPASSWORD": "${PGPASSWORD}"
    }
  }
}
```

**GitHub Server**: Track optimization history
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

**Context7 Server**: Research optimization techniques
```json
{
  "context7": {
    "command": "npx",
    "args": ["-y", "@context-labs/mcp-server"],
    "env": {
      "CONTEXT7_API_KEY": "${CONTEXT7_API_KEY}"
    }
  }
}
```

## Optimization Workflow

### Phase 1: Analysis
1. Collect baseline performance metrics
2. Identify slow queries and bottlenecks
3. Analyze execution plans
4. Review resource utilization
5. Assess current configuration

### Phase 2: Planning
1. Prioritize optimizations by impact
2. Design index strategies
3. Plan configuration changes
4. Estimate expected improvements
5. Prepare rollback procedures

### Phase 3: Implementation
1. Apply optimizations incrementally
2. Implement new indexes
3. Update configurations
4. Rewrite inefficient queries
5. Test each change

### Phase 4: Validation
1. Measure performance improvements
2. Monitor system stability
3. Validate against baselines
4. Document changes
5. Train team on optimizations

## Performance Metrics

### Key Performance Indicators

**Query Performance**:
- Average query time
- 95th percentile latency
- Slow query count
- Query throughput (QPS)

**Index Health**:
- Index usage percentage
- Unused index count
- Index bloat percentage
- Index scan vs. seq scan ratio

**System Health**:
- Cache hit rate
- Buffer pool efficiency
- Lock wait percentage
- Connection utilization

**Resource Usage**:
- CPU utilization
- Memory consumption
- I/O operations
- Network bandwidth

## Best Practices

### Query Optimization
- Always analyze execution plans before optimizing
- Test changes in non-production first
- Monitor impact of every optimization
- Document query patterns and rationale
- Keep queries simple and readable

### Index Design
- Create indexes based on query patterns
- Avoid over-indexing (maintenance overhead)
- Use covering indexes for frequent queries
- Monitor index usage regularly
- Remove unused indexes

### Configuration Tuning
- Start with workload analysis
- Change one parameter at a time
- Monitor impact before next change
- Document all configuration changes
- Keep rollback configurations ready

### Monitoring
- Set up comprehensive monitoring
- Configure appropriate alert thresholds
- Track trends over time
- Review metrics regularly
- Automate reporting

## Integration with Other Agents

The Database Optimizer agent works seamlessly with:

- **postgres-pro**: PostgreSQL-specific advanced optimizations
- **backend-developer**: Query pattern optimization and ORM tuning
- **data-engineer**: ETL and data pipeline performance
- **devops-engineer**: Infrastructure and resource provisioning
- **sre-engineer**: Reliability and performance SLAs
- **data-scientist**: Analytical query optimization
- **cloud-architect**: Cloud database configurations
- **performance-engineer**: System-wide performance tuning

## Troubleshooting

### Common Issues

**Slow Queries Persist**:
- Verify indexes are being used (check execution plans)
- Ensure statistics are up to date (run ANALYZE)
- Check for lock contention
- Review query complexity

**Low Cache Hit Rate**:
- Increase buffer pool size if memory available
- Review query patterns (avoid full table scans)
- Check for bloat requiring cleanup
- Optimize frequently accessed tables

**High Lock Contention**:
- Identify blocking queries
- Reduce transaction size
- Optimize transaction isolation levels
- Consider partitioning hot tables

**Index Not Being Used**:
- Check query predicates match index columns
- Verify statistics are current
- Review index selectivity
- Consider query hints (as last resort)

## Resources

- [PostgreSQL Performance Optimization](https://www.postgresql.org/docs/current/performance-tips.html)
- [MySQL Performance Schema](https://dev.mysql.com/doc/refman/8.0/en/performance-schema.html)
- [MongoDB Performance Best Practices](https://www.mongodb.com/docs/manual/administration/analyzing-mongodb-performance/)
- [Redis Optimization Guide](https://redis.io/docs/management/optimization/)

## Support

For issues, questions, or contributions:
- GitHub Issues: https://github.com/claude-code-agent-marketplace/issues
- Documentation: https://github.com/claude-code-agent-marketplace

## License

MIT License - see LICENSE file for details

---

**Start optimizing your databases today!** Use the Database Optimizer agent to achieve sub-100ms query times, 90%+ cache hit rates, and optimal resource utilization across all your database systems.
