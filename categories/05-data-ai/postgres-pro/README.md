# PostgreSQL Expert Agent

Expert PostgreSQL specialist mastering database administration, performance optimization, and high availability. Deep expertise in PostgreSQL internals, advanced features, and enterprise deployment with focus on reliability and peak performance.

## Overview

The PostgreSQL Expert Agent is your dedicated specialist for all PostgreSQL-related tasks, from performance tuning and query optimization to high availability setup and disaster recovery planning. This agent combines deep knowledge of PostgreSQL internals with practical experience in enterprise deployments.

## Key Capabilities

- **Performance Optimization**: Query tuning, index design, configuration optimization
- **High Availability**: Streaming/logical replication, automatic failover, load balancing
- **Backup & Recovery**: pg_dump, pg_basebackup, WAL archiving, PITR
- **Advanced Features**: JSONB, full-text search, PostGIS, partitioning, extensions
- **Security**: Authentication, SSL/TLS, row-level security, audit logging
- **Monitoring**: pg_stat_* views, performance metrics, alerting

## Slash Commands

### /pg-analyze
Comprehensive database performance analysis

```
/pg-analyze [database_name]
```

This command will:
1. Query pg_stat_statements for top slow queries
2. Check table and index bloat
3. Analyze buffer cache hit ratios
4. Review checkpoint and vacuum activity
5. Examine connection patterns and locks
6. Generate performance report with recommendations

**Example output:**
```
Performance Analysis Report
==========================

Top 5 Slow Queries:
1. SELECT * FROM orders WHERE created_at > ... (avg: 287ms, calls: 15,234)
   Recommendation: Add index on created_at, avoid SELECT *

2. SELECT users.*, orders.* FROM users JOIN orders ... (avg: 156ms, calls: 8,901)
   Recommendation: Use hash join, add covering index

Buffer Cache Hit Ratio: 94.2% (target: >95%)
Table Bloat: 3 tables with >20% dead tuples
Replication Lag: 234ms (healthy)
Connection Count: 78/100 (consider connection pooling)
```

### /pg-optimize
Database optimization workflow

```
/pg-optimize <query_or_table>
```

This command will:
1. Run EXPLAIN ANALYZE on target queries
2. Identify missing or unused indexes
3. Review statistics and analyze tables
4. Tune autovacuum settings
5. Optimize memory and checkpoint parameters
6. Implement improvements
7. Validate performance gains

**Example:**
```
/pg-optimize "SELECT * FROM orders WHERE user_id = 123 AND status = 'pending'"

Analysis:
- Sequential scan on orders table (cost: 10000..45000)
- Filter removes 98% of rows
- Missing index on (user_id, status)

Recommendation:
CREATE INDEX CONCURRENTLY idx_orders_user_status
ON orders(user_id, status)
WHERE status = 'pending';

Expected improvement: 287ms → 3ms (95x faster)
```

### /pg-migrate
Create safe database migration

```
/pg-migrate <migration_description>
```

This command will:
1. Analyze schema change requirements
2. Generate migration SQL with safety checks
3. Include rollback procedures
4. Add index creation with CONCURRENTLY
5. Validate against production schema
6. Document migration steps and risks
7. Create testing checklist

**Example:**
```
/pg-migrate "Add email index to users table and create orders_archive partition"

Generated Migration:
==================

-- Migration: 001_add_email_index_and_partition.sql
-- Date: 2025-12-24
-- Description: Add email index and create orders_archive partition

BEGIN;

-- Step 1: Add index (uses CONCURRENTLY, run outside transaction)
COMMIT;

CREATE INDEX CONCURRENTLY idx_users_email ON users(email);

BEGIN;

-- Step 2: Create partition
CREATE TABLE orders_2024_q4 PARTITION OF orders
FOR VALUES FROM ('2024-10-01') TO ('2025-01-01');

COMMIT;

-- Rollback Procedure:
-- DROP INDEX CONCURRENTLY idx_users_email;
-- DROP TABLE orders_2024_q4;

-- Testing Checklist:
-- [ ] Verify index creation completed
-- [ ] Check query performance improvement
-- [ ] Validate partition constraints
-- [ ] Test INSERT/SELECT on new partition
-- [ ] Monitor replication lag during deployment
```

## Setup Instructions

### 1. Environment Variables

Create a `.env` file or set these environment variables:

```bash
# PostgreSQL Connection (Required)
export PGHOST=localhost
export PGPORT=5432
export PGDATABASE=postgres
export PGUSER=postgres
export PGPASSWORD=your_password

# GitHub Integration (Optional)
export GITHUB_PERSONAL_ACCESS_TOKEN=ghp_your_token

# Context7 for Documentation (Optional)
export CONTEXT7_API_KEY=your_api_key
```

### 2. PostgreSQL Configuration

Enable required extensions and configure monitoring:

```sql
-- Enable pg_stat_statements
CREATE EXTENSION IF NOT EXISTS pg_stat_statements;

-- Grant monitoring permissions
GRANT pg_monitor TO your_user;

-- Or grant specific permissions
GRANT SELECT ON pg_stat_statements TO your_user;
GRANT SELECT ON pg_stat_replication TO your_user;
GRANT SELECT ON pg_stat_activity TO your_user;
```

Add to `postgresql.conf`:
```ini
shared_preload_libraries = 'pg_stat_statements'
pg_stat_statements.track = all
pg_stat_statements.max = 10000
```

### 3. Configure pg_hba.conf

Allow local connections:
```
# TYPE  DATABASE        USER            ADDRESS                 METHOD
local   all            postgres                                peer
host    all            all             127.0.0.1/32            scram-sha-256
host    replication    repl            10.0.0.0/8              scram-sha-256
```

### 4. Install MCP Servers

The agent uses these MCP servers (installed automatically via npx):

- **@modelcontextprotocol/server-postgres** - Direct PostgreSQL access
- **@modelcontextprotocol/server-filesystem** - Access config files and logs
- **@modelcontextprotocol/server-github** - Track schema changes
- **@context-labs/mcp-server** - Research documentation

### 5. Restart PostgreSQL

After configuration changes:
```bash
# Linux
sudo systemctl restart postgresql

# macOS (Homebrew)
brew services restart postgresql

# macOS (manual)
pg_ctl restart -D /usr/local/var/postgres
```

## Usage Examples

### Performance Tuning

```
User: My queries are slow. Can you help optimize them?

Agent: I'll analyze your database performance using /pg-analyze.

[Runs performance analysis]

I found 3 critical issues:
1. Missing index on orders.user_id (affecting 15K queries/day)
2. Inefficient JOIN order in dashboard query
3. Bloat in users table (35% dead tuples)

Let me optimize each:

[Creates indexes with CONCURRENTLY]
[Rewrites queries]
[Runs VACUUM ANALYZE]

Results:
- Dashboard query: 287ms → 18ms (16x faster)
- User lookup: 156ms → 4ms (39x faster)
- Overall latency reduced by 89%
```

### Replication Setup

```
User: Set up streaming replication with automatic failover

Agent: I'll configure high availability with streaming replication
and Patroni for automatic failover.

Step 1: Configure Primary
[Modifies postgresql.conf]
- wal_level = replica
- max_wal_senders = 10
- hot_standby = on

Step 2: Create Replication User
[Creates replication role]

Step 3: Setup Standby
[Runs pg_basebackup]
[Configures recovery settings]

Step 4: Install Patroni
[Configures Patroni with etcd]
[Sets up HAProxy]

Verification:
✓ Replication lag: 89ms
✓ Standby is hot (accepting read queries)
✓ Automatic failover configured
✓ Health checks passing

Your HA cluster is ready!
```

### Migration Planning

```
User: I need to add a new column and index to a large table

Agent: I'll create a safe migration using /pg-migrate that
minimizes downtime.

[Analyzes table: 50M rows, 15GB]

Migration Strategy:
1. Add column with DEFAULT (requires table rewrite in PG < 11)
2. Backfill in batches to avoid blocking
3. Create index with CONCURRENTLY
4. Update application code
5. Make column NOT NULL

Generated migration with:
- Lock timeout protections
- Batch processing scripts
- Rollback procedures
- Monitoring queries
- Estimated time: 45 minutes

Risk assessment:
- Low risk: Using CONCURRENTLY prevents table locks
- Moderate I/O impact during backfill
- Replication lag may increase temporarily

Testing plan included.
```

## Performance Targets

The agent aims to achieve:

- Query performance: < 50ms
- Replication lag: < 500ms
- Backup RPO: < 5 minutes
- Recovery RTO: < 1 hour
- Uptime: > 99.95%
- Cache hit ratio: > 95%

## Common Tasks

### Query Optimization
1. Identify slow queries via pg_stat_statements
2. Run EXPLAIN ANALYZE
3. Analyze query plans
4. Recommend index or query changes
5. Validate improvements

### Replication Monitoring
```sql
-- Check replication status
SELECT * FROM pg_stat_replication;

-- Check replication lag
SELECT EXTRACT(EPOCH FROM (now() - pg_last_xact_replay_timestamp()))
AS lag_seconds;
```

### Backup Verification
```bash
# Full backup
pg_dump -Fc dbname > backup.dump

# Parallel backup
pg_dump -Fd -j 8 dbname -f backup_dir

# Base backup for replication
pg_basebackup -D backup -Ft -z -P
```

### Vacuum Management
```sql
-- Check bloat
SELECT schemaname, tablename, n_dead_tup, n_live_tup
FROM pg_stat_user_tables
WHERE n_dead_tup > 1000
ORDER BY n_dead_tup DESC;

-- Manual vacuum
VACUUM ANALYZE tablename;
```

## Advanced Features

### JSONB Optimization
```sql
-- Create GIN index for JSONB
CREATE INDEX idx_data ON table USING GIN (data);

-- Query with containment
SELECT * FROM table WHERE data @> '{"status": "active"}';

-- Query with key existence
SELECT * FROM table WHERE data ? 'email';
```

### Partitioning
```sql
-- Create partitioned table
CREATE TABLE orders (
    id BIGSERIAL,
    created_at TIMESTAMPTZ,
    ...
) PARTITION BY RANGE (created_at);

-- Create partitions
CREATE TABLE orders_2024_q4 PARTITION OF orders
FOR VALUES FROM ('2024-10-01') TO ('2025-01-01');
```

### Full-Text Search
```sql
-- Create tsvector column
ALTER TABLE documents ADD COLUMN tsv tsvector;

-- Create GIN index
CREATE INDEX idx_tsv ON documents USING GIN(tsv);

-- Search
SELECT * FROM documents
WHERE tsv @@ to_tsquery('postgresql & performance');
```

## Integration with Other Agents

The PostgreSQL Expert works seamlessly with:

- **database-optimizer**: General database optimization strategies
- **backend-developer**: Query pattern recommendations
- **data-engineer**: ETL pipeline optimization
- **devops-engineer**: Deployment automation
- **sre-engineer**: Reliability and monitoring
- **cloud-architect**: Cloud PostgreSQL (RDS, Cloud SQL)
- **security-auditor**: Security hardening
- **performance-engineer**: System-level tuning

## Troubleshooting

### Connection Issues
```bash
# Test connection
psql -h $PGHOST -p $PGPORT -U $PGUSER -d $PGDATABASE

# Check PostgreSQL is running
pg_isready -h $PGHOST -p $PGPORT
```

### Permission Issues
```sql
-- Grant monitoring role
GRANT pg_monitor TO your_user;

-- Check current permissions
\du your_user
```

### Extension Issues
```sql
-- List installed extensions
\dx

-- Install pg_stat_statements
CREATE EXTENSION pg_stat_statements;

-- Verify extension works
SELECT * FROM pg_stat_statements LIMIT 1;
```

## Best Practices

1. **Always backup before major changes**
2. **Use CONCURRENTLY for index creation on production**
3. **Test migrations on staging first**
4. **Monitor replication lag during high-load operations**
5. **Regular VACUUM and ANALYZE**
6. **Keep statistics up to date**
7. **Use connection pooling (PgBouncer)**
8. **Document all configuration changes**

## Resources

- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [PostgreSQL Wiki](https://wiki.postgresql.org/)
- [pg_stat_statements Guide](https://www.postgresql.org/docs/current/pgstatstatements.html)
- [Patroni Documentation](https://patroni.readthedocs.io/)
- [PgBouncer Documentation](https://www.pgbouncer.org/)

## Support

For issues or questions:
- GitHub Issues: [claude-code-agent-marketplace/issues](https://github.com/claude-code-agent-marketplace/issues)
- Documentation: [Agent Marketplace](https://github.com/claude-code-agent-marketplace)

## License

MIT License - See LICENSE file for details
