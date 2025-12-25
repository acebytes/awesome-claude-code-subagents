# Data Engineer Agent

Expert data engineer specializing in building scalable data pipelines, ETL/ELT processes, and data infrastructure. Masters big data technologies and cloud platforms with focus on reliable, efficient, and cost-optimized data platforms.

## Overview

The Data Engineer agent helps you design, build, and optimize data platforms that process TB-scale data with 99.9% reliability. From batch ETL pipelines to real-time streaming architectures, this agent brings comprehensive expertise in modern data engineering practices.

### Key Capabilities

- **Scalable Data Pipelines**: Build pipelines processing 2.3TB+ daily with 99.7% success rates
- **ETL/ELT Excellence**: Implement robust extract, transform, load processes with comprehensive error handling
- **Data Quality**: Deploy quality frameworks catching 99%+ of issues before they impact downstream systems
- **Cost Optimization**: Reduce infrastructure costs by 50-70% through intelligent tiering and resource management
- **Real-time Processing**: Design streaming pipelines with exactly-once semantics and sub-minute latency
- **Data Governance**: Establish lineage tracking, access controls, and compliance frameworks

## Quick Start

### Installation

1. Clone this repository
2. Navigate to the data-engineer directory
3. Configure MCP servers in `mcp-config.json`
4. Start using the agent via Claude Desktop or CLI

### Basic Usage

```bash
# Create a new data pipeline
/data-pipeline postgres-orders snowflake-analytics --incremental --quality-checks

# Implement data quality checks
/data-quality customer_data --completeness --uniqueness --freshness

# Document data assets
/data-catalog sales_fact --lineage --samples --stats
```

## Technology Stack

### Big Data Technologies
- **Apache Spark**: Distributed data processing
- **Apache Kafka**: Event streaming platform
- **Apache Flink**: Stream processing framework
- **Apache Beam**: Unified batch/stream processing
- **Presto/Trino**: Distributed SQL query engine

### Cloud Data Platforms
- **Snowflake**: Cloud data warehouse
- **Google BigQuery**: Serverless data warehouse
- **Amazon Redshift**: AWS data warehouse
- **Azure Synapse**: Microsoft analytics service
- **Databricks**: Unified analytics platform

### Orchestration Tools
- **Apache Airflow**: Workflow orchestration
- **Prefect**: Modern workflow management
- **Dagster**: Data orchestrator for ML/analytics
- **Kubernetes**: Container orchestration
- **AWS Step Functions**: Serverless workflows

### Storage Formats
- **Delta Lake**: ACID transactions on data lakes
- **Apache Iceberg**: Table format for huge datasets
- **Apache Parquet**: Columnar storage format
- **Apache Avro**: Row-based data serialization

## Slash Commands

### /data-pipeline

Create a new data pipeline with industry best practices.

**Syntax**: `/data-pipeline <source> <destination> [options]`

**Options**:
- `--incremental`: Incremental loading using watermarks
- `--streaming`: Real-time streaming pipeline
- `--quality-checks`: Implement data quality validations
- `--monitoring`: Setup comprehensive monitoring

**What it does**:
1. Analyzes source system and data characteristics
2. Designs optimal extraction strategy (full/incremental/CDC)
3. Defines transformation logic with quality checks
4. Configures loading pattern (batch/streaming/micro-batch)
5. Sets up orchestration and scheduling
6. Implements error handling and retry mechanisms
7. Creates documentation and operational runbook

**Examples**:
```bash
# Batch pipeline with incremental loading
/data-pipeline postgres-orders snowflake-analytics --incremental --quality-checks

# Real-time streaming pipeline
/data-pipeline kafka-events bigquery-streaming --streaming --monitoring

# Full load batch pipeline
/data-pipeline s3-logs redshift-warehouse --quality-checks
```

### /data-quality

Implement comprehensive data quality framework.

**Syntax**: `/data-quality <dataset> [rules]`

**Quality Dimensions**:
- `--completeness`: Check for missing/null values
- `--accuracy`: Validate data against business rules
- `--consistency`: Ensure referential integrity
- `--uniqueness`: Detect duplicates
- `--freshness`: Monitor data timeliness
- `--validity`: Check data types and formats

**What it does**:
1. Assesses current data quality state
2. Defines validation rules and thresholds
3. Implements schema validation
4. Configures anomaly detection
5. Sets up quality monitoring dashboards
6. Creates alerting for quality issues
7. Documents quality SLAs and metrics

**Examples**:
```bash
# Basic quality checks
/data-quality customer_data --completeness --uniqueness

# Comprehensive quality framework
/data-quality orders --completeness --accuracy --consistency --freshness

# Streaming quality checks
/data-quality realtime_events --validity --freshness
```

### /data-catalog

Document data assets with comprehensive metadata.

**Syntax**: `/data-catalog <dataset> [scope]`

**Documentation Scope**:
- `--lineage`: Document upstream sources and downstream consumers
- `--samples`: Include sample data rows
- `--stats`: Add statistical profiles (min/max/avg/distribution)
- `--glossary`: Define business terms and definitions
- `--quality`: Include quality metrics and SLAs
- `--usage`: Add query examples and patterns

**What it does**:
1. Extracts schema and column metadata
2. Maps data lineage (source-to-target)
3. Documents business context and glossary
4. Captures sample data and statistics
5. Records refresh schedules and SLAs
6. Adds data quality metrics
7. Creates usage examples and common queries

**Examples**:
```bash
# Basic documentation
/data-catalog sales_fact --lineage --samples

# Comprehensive catalog entry
/data-catalog customer_dim --lineage --stats --glossary --quality --usage

# Quick reference documentation
/data-catalog event_stream --samples --usage
```

## MCP Server Integration

### Filesystem MCP (Required)

Access pipeline configurations, ETL scripts, and orchestration DAGs.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/repo"]
}
```

**Use Cases**:
- Read/write Airflow DAG files
- Manage data quality rule definitions
- Access pipeline configuration YAML files
- Handle DBT transformation models

### GitHub MCP (Optional)

Version control pipeline code and track schema evolution.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-github"],
  "env": {
    "GITHUB_PERSONAL_ACCESS_TOKEN": "<your_token>"
  }
}
```

**Use Cases**:
- Review data pipeline pull requests
- Track data schema version changes
- Collaborate on pipeline development
- Manage CI/CD for data workflows

### Postgres MCP (Optional)

Query databases, analyze statistics, implement quality checks.

**Configuration**:
```json
{
  "command": "npx",
  "args": [
    "-y",
    "@modelcontextprotocol/server-postgres",
    "postgresql://user:password@host:port/database"
  ]
}
```

**Use Cases**:
- Query data warehouse schemas
- Analyze table statistics and row counts
- Run data quality validation queries
- Inspect dimensional model relationships

### Context7 MCP (Optional)

Search documentation and find best practices.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@context7/mcp-server"],
  "env": {
    "CONTEXT7_API_KEY": "<your_api_key>"
  }
}
```

**Use Cases**:
- Find Spark optimization techniques
- Search Kafka configuration best practices
- Access Airflow patterns and examples
- Retrieve data modeling guidelines

## Workflow Examples

### Example 1: Build Incremental ETL Pipeline

```
User: Build an incremental ETL pipeline from our Postgres orders table to Snowflake

Agent: I'll create a robust incremental ETL pipeline with the following approach:

1. Source Analysis:
   - Query Postgres orders schema
   - Identify watermark column (updated_at)
   - Estimate daily data volume

2. Pipeline Design:
   - Incremental extraction using max(updated_at)
   - Transformation: cleansing, enrichment, SCD Type 2
   - Upsert loading pattern in Snowflake

3. Implementation:
   - Create Airflow DAG with retry logic
   - Add data quality checks (completeness, duplicates)
   - Configure monitoring and alerts

4. Documentation:
   - Update data catalog with lineage
   - Document SLAs and dependencies
   - Create operational runbook

[Agent proceeds to implement pipeline, create DAG file, setup monitoring]
```

### Example 2: Implement Data Quality Framework

```
User: /data-quality customer_data --completeness --uniqueness --freshness

Agent: Implementing comprehensive data quality framework for customer_data:

1. Completeness Checks:
   - Required fields: customer_id, email, created_at
   - Threshold: 99.5% completeness required
   - Alert if > 0.5% nulls detected

2. Uniqueness Validation:
   - Primary key: customer_id must be unique
   - Email: duplicate detection with fuzzy matching
   - Alert on any duplicates found

3. Freshness Monitoring:
   - SLA: Data < 1 hour old
   - Check max(updated_at) timestamp
   - Alert if data staleness > 1 hour

4. Implementation:
   - Created quality check SQL queries
   - Configured Airflow sensor for scheduling
   - Setup PagerDuty alerts for failures
   - Built quality dashboard in Grafana

[Agent creates quality check code, configures monitoring, documents checks]
```

### Example 3: Document Data Asset

```
User: /data-catalog sales_fact --lineage --stats --glossary

Agent: Creating comprehensive documentation for sales_fact table:

1. Schema Documentation:
   - 15 columns documented with descriptions
   - Data types and constraints captured
   - Partitioned by order_date (daily)

2. Data Lineage:
   - Upstream sources: orders, customers, products (Postgres)
   - Transformation: orders_enriched_v2 (DBT model)
   - Downstream consumers: BI dashboard, ML model training

3. Statistical Profile:
   - Row count: 145M records
   - Date range: 2020-01-01 to 2025-12-23
   - Daily volume: ~50K orders
   - Total revenue: $2.3B

4. Business Glossary:
   - sales_amount: Total order value excluding tax
   - net_revenue: Sales amount minus discounts and returns
   - customer_ltv: Lifetime value calculated over 12 months

[Agent generates complete catalog entry with metadata, lineage, and examples]
```

## Best Practices

### Pipeline Design
- **Idempotency**: Design pipelines that can safely re-run without duplicating data
- **Incremental Processing**: Use watermarks and checkpoints for efficiency
- **Schema Evolution**: Handle schema changes gracefully with versioning
- **Error Handling**: Implement comprehensive retry logic and dead letter queues

### Data Quality
- **Validation Gates**: Check quality at ingestion, transformation, and loading stages
- **Automated Monitoring**: Continuously monitor quality metrics and trends
- **Alert Fatigue**: Set appropriate thresholds to avoid false positives
- **Documentation**: Document quality rules and their business rationale

### Performance Optimization
- **Partitioning**: Partition large tables by date or other high-cardinality columns
- **File Formats**: Use columnar formats (Parquet/ORC) for analytics
- **Compression**: Apply appropriate compression (snappy for speed, gzip for size)
- **Caching**: Cache intermediate results for complex multi-stage pipelines

### Cost Management
- **Resource Right-sizing**: Match cluster size to workload requirements
- **Spot Instances**: Use preemptible instances for fault-tolerant workloads
- **Storage Tiering**: Move cold data to cheaper storage classes
- **Query Optimization**: Optimize queries to reduce compute costs

### Operational Excellence
- **Monitoring**: Track pipeline metrics, data quality, and resource utilization
- **Alerting**: Configure alerts for failures, SLA breaches, and quality issues
- **Documentation**: Maintain runbooks, data catalogs, and architecture diagrams
- **Testing**: Test with realistic data volumes before production deployment

## Common Patterns

### Lambda Architecture
Combine batch and streaming for accuracy and low latency:
- **Batch Layer**: Historical data processing for accuracy
- **Speed Layer**: Real-time processing for low latency
- **Serving Layer**: Merge views for unified querying

### Medallion Architecture
Progressive data refinement through zones:
- **Bronze**: Raw data landing zone
- **Silver**: Cleansed and conformed data
- **Gold**: Business-ready aggregates and features

### CDC Pattern
Capture database changes in real-time:
- Use Debezium or database-native CDC
- Stream changes to Kafka
- Apply changes to target warehouse
- Maintain full history for auditing

### Slowly Changing Dimensions (SCD Type 2)
Track historical changes in dimensions:
- Add effective_date and end_date columns
- Create new row for each change
- Maintain current_flag for active records
- Join facts to dimensions using date ranges

## Performance Metrics

### Pipeline Reliability
- **SLA Compliance**: 99.9% uptime maintained
- **Success Rate**: 99.7% pipeline runs successful
- **MTTR**: Mean time to recovery < 15 minutes
- **Data Loss**: Zero data loss guarantee

### Data Freshness
- **Batch Latency**: < 1 hour for daily pipelines
- **Streaming Latency**: < 1 minute for real-time
- **End-to-End**: Source to consumption < 2 hours
- **Quality Checks**: < 5 minutes validation time

### Cost Efficiency
- **Cost Optimization**: 50-70% reduction typical
- **Storage Costs**: $20-25 per TB monthly
- **Compute Costs**: $0.50-2.00 per TB processed
- **Total Cost**: Reduced by intelligent tiering

### Scale
- **Daily Volume**: 2.3TB+ processed daily
- **Pipeline Count**: 47+ production pipelines
- **Table Count**: 500+ managed tables
- **Query Performance**: 95th percentile < 10 seconds

## Troubleshooting

### Pipeline Failures
1. Check Airflow logs for error messages
2. Verify source system connectivity
3. Validate schema compatibility
4. Review data quality check results
5. Check resource availability (memory/CPU)

### Performance Issues
1. Analyze query execution plans
2. Review partition pruning effectiveness
3. Check for data skew in joins
4. Verify appropriate file sizes
5. Monitor resource utilization

### Data Quality Issues
1. Review quality check failure details
2. Sample failed records for patterns
3. Check upstream source data
4. Validate transformation logic
5. Verify business rule accuracy

## Support and Collaboration

This agent works closely with:
- **data-scientist**: Feature engineering and ML pipelines
- **database-optimizer**: Query performance tuning
- **ai-engineer**: ML data infrastructure
- **cloud-architect**: Infrastructure planning and scaling
- **devops-engineer**: CI/CD for data pipelines

## Resources

### Documentation
- Apache Spark: [spark.apache.org](https://spark.apache.org)
- Apache Airflow: [airflow.apache.org](https://airflow.apache.org)
- Databricks: [docs.databricks.com](https://docs.databricks.com)
- Delta Lake: [delta.io](https://delta.io)

### Best Practices
- Data Engineering Cookbook: [github.com/andkret/Cookbook](https://github.com/andkret/Cookbook)
- Awesome Data Engineering: [github.com/igorbarinov/awesome-data-engineering](https://github.com/igorbarinov/awesome-data-engineering)

## License

Part of the Claude Agent Marketplace. See repository LICENSE for details.
