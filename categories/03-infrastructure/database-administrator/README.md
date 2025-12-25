# Database Administrator Agent

Expert database administrator specializing in high-availability systems, performance optimization, and disaster recovery. Masters PostgreSQL, MySQL, MongoDB, and Redis with focus on reliability, scalability, and operational excellence.

## Overview

This agent provides comprehensive database administration services across major database platforms, ensuring 99.99% uptime, sub-second query performance, and robust disaster recovery capabilities.

## Key Capabilities

### Database Systems
- **PostgreSQL**: Streaming replication, partitioning, VACUUM optimization, extensions
- **MySQL**: InnoDB optimization, replication topologies, ProxySQL, group replication
- **MongoDB**: Replica sets, sharding, document modeling, aggregation pipelines
- **Redis**: Clustering, memory optimization, persistence strategies

### High Availability
- Master-slave and multi-master replication
- Streaming and logical replication
- Automatic failover configuration
- Load balancing and read replica routing
- Split-brain prevention

### Performance Optimization
- Query performance analysis and optimization
- Index strategy design and implementation
- Cache configuration and tuning
- Buffer pool and memory optimization
- Connection pooling setup
- Resource allocation and tuning

### Backup & Recovery
- Automated backup strategies
- Point-in-time recovery (PITR)
- Incremental and full backup management
- Backup verification and testing
- RTO < 1 hour, RPO < 5 minutes
- Disaster recovery planning and testing

### Monitoring & Alerting
- Performance metrics collection
- Custom dashboards and alerts
- Slow query tracking
- Replication lag monitoring
- Capacity forecasting
- Lock and deadlock detection

### Security
- Access control and privilege management
- Encryption at rest and in transit
- SSL/TLS configuration
- Audit logging
- Row-level security
- Compliance adherence

## Slash Commands

### /dba-backup
Configure comprehensive backup strategy with automated testing and retention policies.

**Features:**
- Automated full and incremental backups
- Point-in-time recovery setup
- Backup verification testing
- Offsite replication configuration
- Retention policy management
- Recovery time objective (RTO) optimization

**Example usage:**
```
/dba-backup
```

### /dba-replication
Setup replication topology with automated failover and monitoring.

**Features:**
- Streaming replication configuration
- Multi-master setup
- Automatic failover implementation
- Replication lag monitoring
- Split-brain prevention
- Read replica routing

**Example usage:**
```
/dba-replication
```

### /dba-performance
Tune database performance with query optimization and resource allocation.

**Features:**
- Query performance analysis
- Index optimization
- Cache tuning
- Memory allocation
- Connection pooling
- Slow query identification
- Resource limit configuration

**Example usage:**
```
/dba-performance
```

## MCP Servers

### filesystem
Access database configuration files, logs, and backup locations.

### github
Manage database schema migrations, runbooks, and documentation in version control.

### postgres
Direct PostgreSQL database access for administration, monitoring, and optimization.

### context7
Access documentation and best practices for database administration across all supported platforms.

## SLA Targets

- **Uptime**: 99.99% (less than 53 minutes downtime per year)
- **RTO**: < 1 hour (Recovery Time Objective)
- **RPO**: < 5 minutes (Recovery Point Objective)
- **Query Response**: < 100ms average for typical queries

## Workflow

### 1. Infrastructure Analysis
- Database inventory audit
- Performance baseline review
- Replication topology assessment
- Backup strategy evaluation
- Security posture check
- Capacity planning review

### 2. Implementation Phase
- High availability setup
- Automated backup configuration
- Monitoring and alerting setup
- Performance optimization
- Security hardening
- Runbook creation

### 3. Operational Excellence
- Continuous monitoring
- Performance tuning
- Backup testing
- Disaster recovery drills
- Capacity management
- Documentation maintenance

## Database Administration Checklist

- [ ] High availability configured (99.99%)
- [ ] RTO < 1 hour, RPO < 5 minutes
- [ ] Automated backup testing enabled
- [ ] Performance baselines established
- [ ] Security hardening completed
- [ ] Monitoring and alerting active
- [ ] Documentation up to date
- [ ] Disaster recovery tested quarterly

## Integration with Other Agents

- **backend-developer**: Query optimization support
- **sql-pro**: Performance tuning guidance
- **sre-engineer**: Reliability collaboration
- **security-engineer**: Data protection
- **devops-engineer**: Automation assistance
- **cloud-architect**: Database architecture
- **platform-engineer**: Self-service platforms
- **data-engineer**: Pipeline coordination

## Best Practices

### Performance
- Establish baseline metrics before optimization
- Implement changes incrementally
- Test in staging environment first
- Monitor impact closely
- Document all changes

### Reliability
- Automate repetitive tasks
- Maintain rollback plans
- Schedule maintenance windows
- Test disaster recovery regularly
- Keep documentation current

### Security
- Follow principle of least privilege
- Enable audit logging
- Encrypt sensitive data
- Regular security audits
- Compliance monitoring

## Example Use Cases

1. **High Availability Setup**: Configure PostgreSQL streaming replication with automatic failover
2. **Performance Crisis**: Diagnose and resolve slow queries causing application timeouts
3. **Disaster Recovery**: Implement and test backup/recovery procedures meeting RTO/RPO targets
4. **Migration**: Execute zero-downtime migration from MySQL 5.7 to 8.0
5. **Scaling**: Design and implement database sharding strategy for MongoDB
6. **Monitoring**: Deploy comprehensive monitoring with predictive alerting
7. **Security Audit**: Harden database security and implement compliance controls

## Getting Started

1. Ensure MCP servers are configured with appropriate credentials
2. Run initial database inventory assessment
3. Establish baseline performance metrics
4. Configure monitoring and alerting
5. Implement backup and recovery procedures
6. Test disaster recovery capabilities

## Support

For issues, questions, or contributions, please refer to the main repository documentation.

---

**Version**: 1.0.0
**Category**: Infrastructure
**Maintained by**: Claude Code Agent Marketplace
