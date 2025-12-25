# DX Optimizer Agent

Expert developer experience optimizer specializing in build performance, tooling efficiency, and workflow automation. Masters development environment optimization with focus on reducing friction, accelerating feedback loops, and maximizing developer productivity and satisfaction.

## Overview

The DX Optimizer agent is designed to dramatically improve developer productivity by optimizing every aspect of the development environment. From build times to test execution, from IDE performance to workflow automation, this agent identifies bottlenecks and implements comprehensive solutions that make developers faster and happier.

## Key Capabilities

### Build Optimization
- **Build Performance**: Reduce build times through incremental compilation, parallel processing, and intelligent caching
- **Module Federation**: Configure module federation for faster builds and better code splitting
- **Asset Pipeline**: Optimize asset processing and bundling strategies
- **Watch Mode**: Enhance watch mode efficiency for faster rebuilds

### Development Server
- **Fast Startup**: Optimize dev server configuration for instant startup
- **HMR Excellence**: Achieve sub-100ms hot module replacement
- **Error Handling**: Configure error overlays and debugging tools
- **Mobile Support**: Enable mobile debugging and testing workflows

### Testing Optimization
- **Parallel Execution**: Configure parallel test execution and sharding
- **Smart Selection**: Implement intelligent test selection strategies
- **Coverage Optimization**: Optimize coverage collection and reporting
- **CI Integration**: Tune testing for CI/CD environments

### Workflow Automation
- **Pre-commit Hooks**: Setup automated code quality checks
- **Code Generation**: Implement code generation and scaffolding tools
- **Script Automation**: Create automation scripts for repetitive tasks
- **Onboarding**: Automate developer onboarding processes

### Metrics & Monitoring
- **Performance Tracking**: Track build times, test execution, and HMR latency
- **Developer Surveys**: Collect and analyze developer satisfaction metrics
- **Productivity Analytics**: Measure and improve developer productivity
- **Dashboard**: Create visualization dashboards for DX metrics

## Slash Commands

### /dx-analyze
Analyze developer workflow bottlenecks and pain points.

```
/dx-analyze
```

**Actions performed:**
- Profile current build times across different environments
- Measure test execution performance
- Analyze HMR and dev server latency
- Review IDE indexing speed
- Survey developer pain points
- Map workflow inefficiencies
- Identify optimization opportunities
- Generate comprehensive analysis report

**Example output:**
```
DX Analysis Report
==================

Build Performance:
- Production build: 2m 14s (Target: <30s)
- Development build: 48s (Target: <30s)
- Rebuild time: 12s (Target: <5s)

Test Performance:
- Full test suite: 4m 32s (Target: <2m)
- Unit tests: 1m 45s
- Integration tests: 2m 47s

HMR Performance:
- Average latency: 340ms (Target: <100ms)
- Slowest updates: 1.2s

Critical Issues:
1. No build caching configured
2. Single-threaded test execution
3. Large bundle sizes causing slow HMR
4. No incremental compilation

Recommendations:
- Implement Webpack persistent cache
- Configure Jest parallel execution
- Enable module federation
- Setup incremental TypeScript builds
```

### /dx-optimize
Optimize development environment for maximum productivity.

```
/dx-optimize [target]
```

**Targets:**
- `build` - Optimize build configuration and performance
- `test` - Optimize testing framework and execution
- `hmr` - Optimize hot module replacement
- `ide` - Optimize IDE configuration and extensions
- `all` - Comprehensive optimization (default)

**Example usage:**

```bash
# Optimize build performance
/dx-optimize build

# Optimize testing
/dx-optimize test

# Comprehensive optimization
/dx-optimize
```

**Actions performed:**
- Implement build caching strategies
- Configure parallel processing
- Setup incremental compilation
- Optimize test execution with parallelization
- Configure HMR efficiently
- Tune IDE settings and extensions
- Automate repetitive workflows
- Document all improvements

**Example output:**
```
Build Optimization Complete
===========================

Changes implemented:
1. Enabled Webpack persistent cache
   - Cache directory: node_modules/.cache/webpack
   - Estimated improvement: 60-70% faster rebuilds

2. Configured parallel compilation
   - Thread loader for TypeScript
   - Parallel workers: 4
   - Estimated improvement: 40% faster initial builds

3. Implemented module federation
   - Shared dependencies extracted
   - Lazy loaded routes
   - Estimated improvement: 50% smaller bundles

4. Optimized asset pipeline
   - Image compression
   - CSS optimization
   - Font subsetting

Results:
- Build time: 2m 14s → 32s (76% improvement)
- Rebuild time: 12s → 3s (75% improvement)
- Bundle size: 4.2MB → 1.8MB (57% reduction)
```

### /dx-metrics
Track and report developer experience metrics.

```
/dx-metrics [period]
```

**Periods:**
- `current` - Current snapshot (default)
- `daily` - Last 24 hours
- `weekly` - Last 7 days
- `monthly` - Last 30 days

**Example usage:**

```bash
# Current metrics snapshot
/dx-metrics

# Weekly trends
/dx-metrics weekly

# Monthly report
/dx-metrics monthly
```

**Actions performed:**
- Measure build time trends
- Track test execution time
- Monitor HMR latency
- Analyze error frequency
- Survey developer satisfaction
- Report productivity metrics
- Generate improvement recommendations
- Create visualization dashboard

**Example output:**
```
Developer Experience Metrics (Weekly)
=====================================

Build Performance:
- Average build time: 34s (↓ 68% vs previous week)
- Average rebuild time: 4s (↓ 71% vs previous week)
- Build failures: 2 (↓ 85% vs previous week)

Test Performance:
- Average test time: 1m 52s (↓ 58% vs previous week)
- Test failures: 12 (↓ 45% vs previous week)
- Flaky tests: 3 (↓ 60% vs previous week)

HMR Performance:
- Average latency: 72ms (↓ 79% vs previous week)
- HMR failures: 1 (↓ 90% vs previous week)

Developer Satisfaction:
- Overall score: 4.6/5 (↑ 35% vs previous week)
- Build speed satisfaction: 4.8/5
- Tool satisfaction: 4.5/5
- Workflow satisfaction: 4.4/5

Productivity Metrics:
- Average commits per day: 8.2 (↑ 45% vs previous week)
- Average PR time: 4.5h (↓ 38% vs previous week)
- Code review time: 2.1h (↓ 28% vs previous week)

Recommendations:
- Continue monitoring HMR performance
- Address remaining flaky tests
- Survey team on IDE performance
```

## Performance Targets

The agent optimizes toward these specific targets:

| Metric | Target | Industry Standard |
|--------|--------|-------------------|
| Build Time | < 30 seconds | 1-5 minutes |
| HMR Latency | < 100ms | 200-500ms |
| Test Execution | < 2 minutes | 5-15 minutes |
| IDE Indexing | Fast & responsive | Varies widely |
| Feedback Loop | Instant | Minutes to hours |

## Use Cases

### 1. Slow Build Times
**Problem**: Production builds take 5+ minutes, blocking deployments and CI/CD.

**Solution**:
```bash
/dx-analyze
/dx-optimize build
```

**Results**:
- Implement persistent caching
- Configure parallel compilation
- Enable incremental builds
- Optimize asset pipeline
- 75% reduction in build time

### 2. Slow Test Execution
**Problem**: Test suite takes 10+ minutes, discouraging frequent testing.

**Solution**:
```bash
/dx-analyze
/dx-optimize test
```

**Results**:
- Configure parallel test execution
- Implement test sharding
- Optimize snapshot testing
- Enable watch mode
- 80% reduction in test time

### 3. Poor HMR Performance
**Problem**: Hot module replacement takes 2-3 seconds, breaking flow.

**Solution**:
```bash
/dx-analyze
/dx-optimize hmr
```

**Results**:
- Configure fast refresh
- Optimize module boundaries
- Reduce bundle sizes
- Enable selective updates
- Sub-100ms HMR latency

### 4. Monorepo Performance
**Problem**: Monorepo builds entire workspace on every change.

**Solution**:
```bash
/dx-analyze
/dx-optimize all
```

**Results**:
- Implement Nx or Turbo
- Configure dependency graph
- Enable remote caching
- Setup affected detection
- 90% reduction in CI time

## MCP Server Configuration

The agent uses three MCP servers:

### Filesystem Server (Required)
Access build configurations, package.json files, and tooling setup.

```json
{
  "filesystem": {
    "command": "npx",
    "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
  }
}
```

**Used for**:
- Reading build configuration files
- Analyzing package.json dependencies
- Reviewing tooling setup files
- Accessing test configurations
- Reading IDE settings

### GitHub Server (Optional)
Track build performance improvements and CI/CD workflows.

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
- Reviewing CI/CD workflow files
- Analyzing build performance trends
- Tracking optimization PRs
- Monitoring developer workflows
- Accessing GitHub Actions logs

### Context7 Server (Optional)
Access DX best practices and optimization documentation.

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
- Accessing build tool documentation
- Retrieving performance optimization guides
- Learning workflow automation patterns
- Understanding monorepo best practices
- Researching tooling comparisons

## Integration with Other Agents

### build-engineer
Collaborate on build optimization and advanced configurations.

### tooling-engineer
Support development of custom developer tools and scripts.

### devops-engineer
Work together on CI/CD pipeline optimization and deployment workflows.

### refactoring-specialist
Guide workflow improvements during code refactoring efforts.

### documentation-engineer
Improve documentation access and developer onboarding materials.

### git-workflow-manager
Assist with Git workflow automation and hook setup.

### legacy-modernizer
Partner on tooling updates during legacy system modernization.

### cli-developer
Coordinate on CLI tool development for developer productivity.

## Best Practices

### Optimization Approach
1. **Measure First**: Always measure current performance before optimizing
2. **Biggest Impact**: Focus on changes with the highest impact first
3. **Iterate Rapidly**: Make incremental improvements and measure results
4. **Document Everything**: Document all changes for team awareness
5. **Monitor Continuously**: Track metrics to ensure improvements stick
6. **Communicate Wins**: Share improvements to build momentum

### Common Optimizations

#### Build Performance
- Enable persistent caching (Webpack, Rollup, esbuild)
- Configure parallel compilation with thread-loader
- Implement incremental TypeScript builds
- Use module federation for code splitting
- Optimize asset pipeline (compression, minification)

#### Test Performance
- Configure parallel test execution (Jest workers)
- Implement test sharding for large suites
- Use watch mode for rapid iteration
- Optimize snapshot testing
- Enable coverage caching

#### HMR Performance
- Configure fast refresh for React
- Optimize module boundaries
- Reduce bundle sizes with code splitting
- Enable selective updates
- Configure proper error boundaries

#### Monorepo Performance
- Implement Nx or Turborepo
- Configure dependency graph analysis
- Enable remote caching
- Setup affected package detection
- Optimize task orchestration

## Getting Started

1. **Install the agent** in your Claude Code environment
2. **Configure MCP servers** (at minimum, filesystem server)
3. **Run initial analysis**: `/dx-analyze`
4. **Review recommendations** and prioritize based on impact
5. **Apply optimizations**: `/dx-optimize all`
6. **Track progress**: `/dx-metrics weekly`
7. **Iterate and improve** based on metrics and feedback

## Example Workflow

```bash
# Step 1: Analyze current state
/dx-analyze

# Step 2: Optimize build performance
/dx-optimize build

# Step 3: Optimize test execution
/dx-optimize test

# Step 4: Check metrics
/dx-metrics current

# Step 5: Track weekly progress
/dx-metrics weekly

# Step 6: Comprehensive optimization
/dx-optimize all

# Step 7: Monitor long-term trends
/dx-metrics monthly
```

## Success Metrics

Track these metrics to measure DX improvements:

- **Build Time**: Target 70%+ reduction
- **Test Time**: Target 60%+ reduction
- **HMR Latency**: Target sub-100ms
- **Developer Satisfaction**: Target 4.5+/5.0
- **Productivity**: Measure commits, PRs, review time
- **Error Rate**: Target 80%+ reduction in build/test failures
- **Onboarding Time**: Target 50%+ reduction

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT
