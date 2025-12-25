# SQL Pro Agent

Expert SQL developer specializing in complex query optimization, database design, and performance tuning across PostgreSQL, MySQL, SQL Server, and Oracle.

## Overview

The SQL Pro agent is a senior-level SQL developer with deep expertise in:
- Complex query design and optimization
- Database schema architecture
- Performance tuning across major RDBMS platforms
- Advanced SQL features and modern data patterns
- Data warehousing and ETL implementations
- Cross-platform SQL migration strategies

## Features

### Core Capabilities

- **Query Optimization**: Transform slow queries into high-performance solutions with 85%+ improvement
- **Schema Design**: Create efficient, scalable database architectures
- **Performance Tuning**: Analyze execution plans, optimize indexes, and eliminate bottlenecks
- **Transaction Management**: Implement proper isolation levels and deadlock prevention
- **Data Warehousing**: Design star schemas, fact tables, and ETL patterns
- **Security**: Implement row-level security, encryption, and SQL injection prevention

### Advanced Features

- Window functions and complex analytics
- Recursive queries and CTEs
- Temporal and geospatial operations
- JSON/XML handling
- Graph database queries
- Materialized views and partitioning
- Cross-platform compatibility

## Slash Commands

### `/sql-analyze`
Analyze SQL queries, schemas, and execution plans to identify performance bottlenecks and optimization opportunities.

**Example Usage:**
```
/sql-analyze
[Paste your SQL query or schema]
```

**Output:**
- Detailed execution plan analysis
- Performance bottleneck identification
- Index recommendations
- Query anti-pattern detection

### `/sql-optimize`
Optimize existing SQL queries for better performance, reducing execution time and resource usage.

**Example Usage:**
```
/sql-optimize
SELECT * FROM orders o
JOIN customers c ON o.customer_id = c.id
WHERE o.created_at > '2024-01-01'
```

**Output:**
- Optimized query version
- Before/after performance comparison
- Explanation of optimization techniques
- Index suggestions

### `/sql-explain`
Explain complex SQL queries, execution plans, and database concepts in clear, understandable terms.

**Example Usage:**
```
/sql-explain
What is the difference between RANK() and ROW_NUMBER() window functions?
```

**Output:**
- Clear explanations of SQL concepts
- Code examples and use cases
- Best practices and gotchas
- Performance considerations

### `/sql-migrate`
Assist with database migrations, schema changes, and cross-platform SQL conversions.

**Example Usage:**
```
/sql-migrate
Convert this PostgreSQL query to MySQL:
SELECT DISTINCT ON (customer_id) * FROM orders ORDER BY customer_id, created_at DESC
```

**Output:**
- Platform-specific SQL conversions
- Migration strategy recommendations
- Data type mapping
- Zero-downtime migration plans

## MCP Servers

The SQL Pro agent uses the following MCP servers:

### Filesystem
Provides access to local files for reading SQL scripts, schema files, and query logs.

### GitHub
Integrates with GitHub repositories to access and manage database migration scripts, schema versions, and SQL codebases.

**Required Environment Variable:**
- `GITHUB_TOKEN`: Your GitHub personal access token

### Postgres
Connects directly to PostgreSQL databases for query execution, schema analysis, and performance testing.

**Required Environment Variable:**
- `POSTGRES_URL`: PostgreSQL connection string (e.g., `postgresql://user:password@localhost:5432/dbname`)

### Memory
Maintains context about your database schema, past optimizations, and project-specific patterns across sessions.

## Setup

### Environment Variables

Create a `.env` file or set the following environment variables:

```bash
# Optional but recommended for full functionality
export POSTGRES_URL="postgresql://user:password@localhost:5432/dbname"
export GITHUB_TOKEN="ghp_your_token_here"
```

### Installation

1. Ensure you have Node.js installed
2. The MCP servers will be automatically installed via `npx` when the agent starts
3. Configure your environment variables as needed

## Usage Examples

### Query Optimization Workflow

```
/sql-analyze
SELECT o.*, c.name, p.total
FROM orders o
JOIN customers c ON o.customer_id = c.id
LEFT JOIN (
  SELECT order_id, SUM(amount) as total
  FROM payments
  GROUP BY order_id
) p ON o.id = p.order_id
WHERE o.created_at > CURRENT_DATE - INTERVAL '30 days'
```

The agent will:
1. Analyze the execution plan
2. Identify missing indexes
3. Suggest query rewrite opportunities
4. Provide optimized version with performance metrics

### Schema Design

```
I need to design a schema for an e-commerce platform with:
- Users and authentication
- Products with variants and inventory
- Orders with line items
- Payment processing
- Audit trails
```

The agent will:
1. Design normalized schema
2. Recommend indexes and constraints
3. Suggest partitioning strategies
4. Implement audit patterns
5. Add security measures

### Performance Tuning

```
/sql-optimize
My dashboard query is taking 5 seconds to load. Here's the query:
[Paste slow query]

Database: PostgreSQL 15
Table size: 50M rows
Current indexes: [List indexes]
```

The agent will:
1. Analyze execution plan
2. Identify bottlenecks (table scans, nested loops, etc.)
3. Recommend covering indexes
4. Suggest materialized views
5. Provide optimized query achieving <100ms target

## Best Practices

### Performance Targets

- Query execution time: <100ms
- Optimization improvement: 85%+
- Scalability: Linear up to 10M records

### Development Checklist

- ✓ ANSI SQL compliance verified
- ✓ Execution plans analyzed
- ✓ Index coverage optimized
- ✓ Deadlock prevention implemented
- ✓ Data integrity constraints enforced
- ✓ Security best practices applied
- ✓ Backup/recovery strategy defined

## Integration with Other Agents

The SQL Pro agent collaborates effectively with:

- **backend-developer**: Optimize queries for APIs and services
- **database-optimizer**: Schema design and performance tuning
- **data-engineer**: ETL pipeline development
- **python-pro**: ORM query optimization
- **java-architect**: JPA/Hibernate query tuning
- **performance-engineer**: System-wide performance analysis
- **devops-engineer**: Database monitoring and automation
- **data-scientist**: Analytical query development

## Platform Support

### Supported Databases

- **PostgreSQL**: 9.6+, including advanced features (JSONB, arrays, CTEs)
- **MySQL**: 5.7+, 8.0+ (InnoDB, replication)
- **SQL Server**: 2016+, 2019+, 2022+ (Columnstore, In-Memory OLTP)
- **Oracle**: 11g+, 12c+, 19c+ (Partitioning, RAC)

### Feature Coverage

| Feature | PostgreSQL | MySQL | SQL Server | Oracle |
|---------|-----------|-------|------------|--------|
| Window Functions | ✓ | ✓ | ✓ | ✓ |
| CTEs | ✓ | ✓ (8.0+) | ✓ | ✓ |
| Recursive Queries | ✓ | ✓ (8.0+) | ✓ | ✓ |
| JSON Support | ✓ | ✓ | ✓ | ✓ |
| Partitioning | ✓ | ✓ | ✓ | ✓ |
| Temporal Tables | ✓ | Limited | ✓ | ✓ |

## Advanced Topics

### Window Functions

Master ranking, aggregation, and analytical functions:
- ROW_NUMBER(), RANK(), DENSE_RANK()
- LAG(), LEAD() for time-series analysis
- Running totals and moving averages
- Percentile calculations
- Frame clause optimization

### Index Strategies

- Clustered vs non-clustered indexes
- Covering indexes for query optimization
- Filtered indexes for specific conditions
- Function-based indexes
- Composite key ordering
- Index intersection and merge

### Data Warehousing

- Star schema and snowflake design
- Slowly changing dimensions (SCD Type 1, 2, 3)
- Fact table optimization
- Aggregate tables and rollups
- Columnstore indexes
- Incremental loading patterns

### ETL Patterns

- Bulk insert optimization
- MERGE statement usage
- Change data capture (CDC)
- Incremental updates
- Data validation
- Error handling and retry logic

## Troubleshooting

### Common Issues

**Slow Query Performance**
1. Run `/sql-analyze` to get execution plan
2. Check for table scans and missing indexes
3. Verify statistics are up to date
4. Consider partitioning for large tables

**Deadlocks**
1. Review transaction isolation levels
2. Analyze lock wait patterns
3. Implement consistent lock ordering
4. Use optimistic concurrency where appropriate

**Migration Issues**
1. Use `/sql-migrate` for platform-specific conversions
2. Test with representative data volumes
3. Plan for rollback scenarios
4. Monitor performance during migration

## Contributing

The SQL Pro agent is part of the Claude Code Agent Marketplace. Contributions and improvements are welcome.

## License

See the main marketplace repository for licensing information.
