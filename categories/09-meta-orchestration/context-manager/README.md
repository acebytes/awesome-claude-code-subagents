# Context Manager Agent

Expert context manager specializing in information storage, retrieval, and synchronization across multi-agent systems. Masters state management, version control, and data lifecycle with focus on ensuring consistency, accessibility, and performance at scale.

## Overview

The Context Manager agent provides enterprise-grade context management capabilities for distributed agent systems. It focuses on maintaining shared knowledge and state across multiple agents with emphasis on fast retrieval, strong consistency, and secure storage.

### Key Features

- **Fast Retrieval**: Sub-100ms query response times
- **Strong Consistency**: 100% data consistency guarantee
- **High Availability**: 99.9%+ uptime target
- **Version Control**: Complete version tracking and history
- **Access Control**: Robust security and privacy compliance
- **Cache Optimization**: Intelligent multi-tier caching
- **Sync Protocols**: Real-time and eventual consistency models
- **Audit Trails**: Complete audit logging and compliance

## Installation

### Prerequisites

- Claude Desktop App or Claude Code CLI
- Node.js 16+ (for MCP servers)
- GitHub Personal Access Token (optional, for GitHub integration)

### Setup

1. Copy the `context-manager` directory to your agents folder
2. Set up environment variables:
   ```bash
   export GITHUB_TOKEN="your-github-token"
   ```
3. The MCP servers will be automatically installed on first use via npx

### MCP Servers

The agent uses three MCP servers:

- **filesystem**: Access and manage local files and directories
- **github**: Integrate with GitHub for version control and collaboration
- **memory**: Persistent memory storage for context management

## Usage

### Starting the Agent

Launch the agent through Claude Desktop or Claude Code:

```bash
claude-code --agent context-manager
```

### Slash Commands

#### /context-save

Save current context state to persistent storage. Captures project metadata, agent interactions, task history, and decision logs.

```
/context-save [scope] [tags]
```

**Parameters:**
- `scope`: Context scope - `project`, `session`, or `global` (default: session)
- `tags`: Optional comma-separated tags for organization

**Examples:**
```
/context-save
/context-save project authentication,security
/context-save global deployment
```

#### /context-restore

Restore previously saved context from storage. Retrieves and rehydrates context data with version management.

```
/context-restore [version] [scope]
```

**Parameters:**
- `version`: Specific version identifier or `latest` (default: latest)
- `scope`: Context scope - `project`, `session`, or `global` (default: session)

**Examples:**
```
/context-restore
/context-restore v1.2.3
/context-restore latest project
```

#### /context-sync

Synchronize context across multiple agents or systems. Manages conflict resolution and ensures consistency.

```
/context-sync [target] [mode]
```

**Parameters:**
- `target`: Agent identifier or `all` (default: all)
- `mode`: Sync mode - `realtime`, `eventual`, or `snapshot` (default: eventual)

**Examples:**
```
/context-sync
/context-sync all realtime
/context-sync workflow-orchestrator eventual
```

#### /context-query

Query stored context using advanced search capabilities. Supports filters, ranking, and aggregations.

```
/context-query [query] [options]
```

**Parameters:**
- `query`: Search query (natural language or structured)
- `options`: JSON object with filters, sorting, pagination

**Examples:**
```
/context-query authentication decisions
/context-query performance metrics {"timeRange": "7d", "limit": 50}
/context-query error patterns {"severity": "high", "sort": "recent"}
```

## Workflow

### 1. Architecture Analysis

The agent starts by designing a robust context storage architecture:

- Analyzing data models and access patterns
- Planning indices and partitions
- Setting up replication and caching strategies
- Defining lifecycle policies

### 2. Implementation Phase

Building the high-performance context management system:

- Deploying storage infrastructure
- Configuring synchronization protocols
- Implementing multi-tier caching
- Enabling monitoring and security
- Testing performance benchmarks

### 3. Context Excellence

Delivering exceptional context management:

- Optimizing retrieval performance
- Maintaining data consistency
- Ensuring high availability
- Enforcing security and compliance
- Providing continuous monitoring

## Performance Targets

- **Retrieval Time**: < 100ms average
- **Data Consistency**: 100% guaranteed
- **Availability**: > 99.9% uptime
- **Cache Hit Rate**: > 85%
- **Storage Efficiency**: Optimized compression and tiering

## Context Types Managed

- **Project Metadata**: Configuration, dependencies, structure
- **Agent Interactions**: Communication logs, handoffs, decisions
- **Task History**: Completed tasks, outcomes, timelines
- **Decision Logs**: Key decisions, rationale, alternatives
- **Performance Metrics**: System performance, bottlenecks, trends
- **Resource Usage**: Memory, CPU, storage consumption
- **Error Patterns**: Error logs, patterns, resolutions
- **Knowledge Base**: Accumulated insights, best practices

## Storage Patterns

- **Hierarchical Organization**: Tree-based data structures
- **Tag-Based Retrieval**: Flexible tagging system
- **Time-Series Data**: Temporal data management
- **Graph Relationships**: Connected data modeling
- **Vector Embeddings**: Semantic search capabilities
- **Full-Text Search**: Advanced text search
- **Metadata Indexing**: Fast metadata queries
- **Compression Strategies**: Storage optimization

## Integration with Other Agents

The Context Manager integrates seamlessly with other meta-orchestration agents:

- **agent-organizer**: Provides context access for agent coordination
- **multi-agent-coordinator**: Manages shared state across agents
- **workflow-orchestrator**: Stores process context and workflow state
- **task-distributor**: Maintains workload data and task history
- **performance-monitor**: Stores and retrieves performance metrics
- **error-coordinator**: Manages error context and patterns
- **knowledge-synthesizer**: Provides data for insight generation

## Best Practices

1. **Design for Scale**: Plan for growth in data volume and access patterns
2. **Optimize Early**: Index strategically and cache intelligently
3. **Security First**: Enforce access control and encryption from the start
4. **Monitor Continuously**: Track performance metrics and usage patterns
5. **Version Everything**: Maintain complete version history
6. **Document Thoroughly**: Keep clear documentation of schemas and APIs
7. **Test Performance**: Regularly benchmark and optimize
8. **Plan for Evolution**: Design for schema migration and updates

## Troubleshooting

### Slow Retrieval Times

- Check index utilization
- Review cache hit rates
- Analyze query patterns
- Consider adding indices or partitions

### Consistency Issues

- Verify synchronization protocols
- Check conflict resolution strategies
- Review version control mechanisms
- Examine replication status

### Storage Growth

- Review retention policies
- Enable compression strategies
- Implement archive procedures
- Optimize data lifecycle

### Access Control Errors

- Verify authentication configuration
- Check authorization rules
- Review role assignments
- Examine audit logs

## Advanced Configuration

### Custom Storage Backends

The agent can be configured to use different storage backends:

- Local filesystem (default)
- GitHub repositories
- Memory server for persistence
- Custom database integration (requires extension)

### Synchronization Modes

- **Real-time**: Immediate propagation with strong consistency
- **Eventual**: Optimized for performance with eventual consistency
- **Snapshot**: Point-in-time consistency for batch operations

### Cache Strategies

- **Write-through**: Immediate persistence with cache update
- **Write-back**: Deferred persistence for performance
- **Cache-aside**: Lazy loading on cache miss

## Contributing

Contributions are welcome! Please follow the standard contribution guidelines for the Claude Agent Marketplace.

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or feature requests, please open an issue in the Claude Agent Marketplace repository.

## Version History

- **1.0.0**: Initial release with core context management capabilities
  - Fast retrieval (< 100ms)
  - Strong consistency guarantees
  - Multi-tier caching
  - Access control and security
  - Version tracking
  - Synchronization protocols
  - Slash commands support
