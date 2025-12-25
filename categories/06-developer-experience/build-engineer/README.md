# Build Engineer Agent

Expert build engineer specializing in build system optimization, compilation strategies, and developer productivity. Masters modern build tools, caching mechanisms, and creating fast, reliable build pipelines that scale with team growth.

## Overview

The Build Engineer agent is designed to optimize build systems, reduce compilation times, and maximize developer productivity. It specializes in modern build tools like Webpack, Vite, esbuild, and Turbopack, with expertise in caching strategies, CI/CD optimization, and monorepo build orchestration.

## Core Capabilities

### Build System Optimization
- Analyze and profile build performance
- Identify bottlenecks and optimization opportunities
- Configure incremental compilation and parallel processing
- Implement advanced caching strategies
- Optimize bundle size and load times

### Build Tool Expertise
- **Webpack**: Configuration optimization, persistent caching, parallel builds
- **Vite**: Dependency pre-bundling, HMR optimization, build configuration
- **esbuild**: High-speed transpilation and bundling
- **Turbopack**: Next.js optimization and migration
- **Rollup**: Library bundling and tree shaking
- **Monorepo Tools**: Turborepo, Nx, Rush build orchestration

### Performance Targets
- Build time < 30 seconds (cold start)
- Rebuild time < 5 seconds (incremental)
- Cache hit rate > 90%
- Bundle size reduction 40-60%
- Zero flaky builds

## Installation

1. Clone the repository:
```bash
git clone https://github.com/anthropics/claude-code-agent-marketplace.git
cd claude-code-agent-marketplace/categories/06-developer-experience/build-engineer
```

2. Ensure you have the required MCP servers installed:
```bash
# Filesystem server
npx @modelcontextprotocol/server-filesystem

# GitHub server (requires GITHUB_TOKEN)
npx @modelcontextprotocol/server-github

# Context7 server
npx @upaya.ai/context7-mcp-server
```

3. Set up environment variables:
```bash
export GITHUB_TOKEN="your_github_token"
```

## Configuration

The agent uses three MCP servers:

### Filesystem Server
Accesses build configuration files:
- `webpack.config.js`, `vite.config.ts`, `rollup.config.js`
- `turbo.json`, `nx.json` (monorepo configs)
- `.github/workflows/*.yml` (CI/CD pipelines)
- `package.json`, `tsconfig.json`, `babel.config.js`

### GitHub Server
Manages CI/CD workflows:
- Analyzes workflow performance
- Tracks build metrics over time
- Optimizes GitHub Actions caching
- Creates PRs for build improvements

### Context7 Server
Queries build tool documentation:
- Webpack optimization techniques
- Vite configuration best practices
- esbuild performance tuning
- Build tool comparisons

## Usage

### Slash Commands

#### /build-analyze
Analyze current build performance and identify bottlenecks.

```bash
/build-analyze
```

**Output**:
- Build time metrics (cold start, incremental, hot reload)
- Bundle size analysis and composition
- Cache hit rates and effectiveness
- Dependency analysis and slow modules
- Resource utilization (CPU, memory, I/O)
- Detailed bottleneck report
- Optimization recommendations

#### /build-optimize
Optimize build configuration for maximum speed and efficiency.

```bash
/build-optimize
```

**Actions**:
- Configure incremental compilation
- Enable parallel processing
- Setup persistent caching
- Optimize module resolution
- Configure code splitting
- Enable tree shaking
- Minimize bundle size
- Update build scripts

**Output**:
- Optimized build configuration files
- Before/after performance metrics
- Implementation documentation
- Recommended next steps

#### /build-cache
Configure advanced build caching strategies.

```bash
/build-cache
```

**Actions**:
- Setup filesystem cache
- Configure remote cache (Turborepo/Nx Cloud)
- Implement content-based hashing
- Configure cache invalidation rules
- Setup distributed caching
- Optimize CI/CD cache usage
- Document cache strategy

**Output**:
- Complete caching configuration
- Expected performance improvements
- Cache management documentation
- Monitoring setup

### Example Workflows

#### 1. Optimize Webpack Build
```bash
# Analyze current performance
/build-analyze

# Review recommendations and optimize
/build-optimize

# Setup advanced caching
/build-cache
```

**Expected Results**:
- 60-80% reduction in build time
- 90%+ cache hit rate
- 40-50% smaller bundles
- Sub-second incremental rebuilds

#### 2. Migrate to Vite
```bash
# Analyze current Webpack setup
/build-analyze

# Get Vite migration guidance
"Help me migrate from Webpack to Vite while maintaining all current features"

# Optimize Vite configuration
/build-optimize
```

#### 3. Setup Monorepo Builds
```bash
# Analyze monorepo structure
/build-analyze

# Configure Turborepo/Nx
"Setup Turborepo with remote caching for this monorepo"

# Optimize parallel execution
/build-optimize
```

## Build Tool Configurations

### Webpack Optimization
```javascript
// webpack.config.js optimizations
module.exports = {
  cache: {
    type: 'filesystem',
    buildDependencies: {
      config: [__filename],
    },
  },
  optimization: {
    moduleIds: 'deterministic',
    runtimeChunk: 'single',
    splitChunks: {
      cacheGroups: {
        vendor: {
          test: /[\\/]node_modules[\\/]/,
          name: 'vendors',
          chunks: 'all',
        },
      },
    },
  },
  parallelism: 4,
};
```

### Vite Optimization
```typescript
// vite.config.ts optimizations
export default defineConfig({
  build: {
    target: 'esnext',
    minify: 'esbuild',
    cssMinify: true,
    rollupOptions: {
      output: {
        manualChunks: {
          vendor: ['react', 'react-dom'],
        },
      },
    },
  },
  optimizeDeps: {
    include: ['react', 'react-dom'],
  },
});
```

### Turborepo Configuration
```json
{
  "pipeline": {
    "build": {
      "dependsOn": ["^build"],
      "outputs": ["dist/**", ".next/**"],
      "cache": true
    },
    "test": {
      "dependsOn": ["build"],
      "cache": true
    }
  },
  "remoteCache": {
    "enabled": true
  }
}
```

## Performance Metrics

### Key Metrics Tracked
- **Build Time**: Cold start, incremental, and hot reload times
- **Bundle Size**: Total size, chunk sizes, vendor bundles
- **Cache Hit Rate**: Filesystem and remote cache effectiveness
- **Resource Usage**: CPU, memory, disk I/O
- **CI/CD Time**: Pipeline duration, cache usage
- **Developer Satisfaction**: Feedback on build experience

### Monitoring Setup
```bash
# Add build timing to package.json
{
  "scripts": {
    "build:analyze": "webpack-bundle-analyzer dist/stats.json",
    "build:profile": "tsc --diagnostics --extendedDiagnostics"
  }
}
```

## Integration with Other Agents

The Build Engineer works closely with:

- **tooling-engineer**: Build tool selection and configuration
- **dx-optimizer**: Developer experience improvements
- **devops-engineer**: CI/CD pipeline optimization
- **frontend-developer**: Bundle optimization and lazy loading
- **backend-developer**: Compilation and transpilation
- **dependency-manager**: Package optimization
- **refactoring-specialist**: Code structure for build efficiency
- **performance-engineer**: Runtime and build performance

## Best Practices

### 1. Measure Before Optimizing
Always profile your build before making changes:
```bash
# Webpack
webpack --profile --json > stats.json

# Vite
vite build --debug

# Turborepo
turbo build --profile
```

### 2. Cache Aggressively
Implement multiple cache layers:
- Filesystem cache (Webpack persistent cache)
- Remote cache (Turborepo Cloud, Nx Cloud)
- CI/CD cache (GitHub Actions cache)
- Browser cache (asset fingerprinting)

### 3. Parallelize Everything
- Use all CPU cores for compilation
- Parallelize CI/CD jobs
- Enable concurrent task execution in monorepos
- Use worker threads for asset processing

### 4. Optimize Dependencies
- Remove unused dependencies
- Use lightweight alternatives
- Enable tree shaking
- Split vendor bundles
- Pre-bundle dependencies (Vite)

### 5. Monitor Continuously
Set up build analytics to track:
- Build time trends
- Cache hit rates
- Bundle size changes
- CI/CD costs
- Developer feedback

## Troubleshooting

### Slow Build Times
1. Profile the build to identify bottlenecks
2. Check cache hit rates
3. Review dependency graph for circular dependencies
4. Optimize module resolution
5. Enable parallel processing

### Large Bundle Sizes
1. Analyze bundle composition
2. Enable tree shaking
3. Configure code splitting
4. Lazy load heavy dependencies
5. Use dynamic imports

### Flaky Builds
1. Ensure reproducible builds
2. Lock dependency versions
3. Configure cache invalidation properly
4. Use content-based hashing
5. Validate build environment

### Cache Misses
1. Review cache invalidation rules
2. Check content-based hashing
3. Verify dependency tracking
4. Optimize cache key generation
5. Monitor cache storage

## Advanced Topics

### Module Federation
Share code between micro-frontends:
```javascript
// webpack.config.js
new ModuleFederationPlugin({
  name: 'app1',
  remotes: {
    app2: 'app2@http://localhost:3002/remoteEntry.js',
  },
  shared: {
    react: { singleton: true },
    'react-dom': { singleton: true },
  },
});
```

### Remote Caching
Setup distributed caching for teams:
```bash
# Turborepo with Vercel Remote Cache
turbo login
turbo link
turbo build --force --cache-dir=.turbo

# Nx Cloud
nx connect-to-nx-cloud
```

### Build Monitoring
Implement comprehensive monitoring:
```javascript
// webpack.config.js
plugins: [
  new webpack.ProgressPlugin(),
  new SpeedMeasurePlugin(),
  new BundleAnalyzerPlugin(),
],
```

## Resources

### Documentation
- [Webpack Documentation](https://webpack.js.org/)
- [Vite Documentation](https://vitejs.dev/)
- [esbuild Documentation](https://esbuild.github.io/)
- [Turborepo Documentation](https://turbo.build/)
- [Nx Documentation](https://nx.dev/)

### Build Tool Comparisons
- [Webpack vs Vite](https://vitejs.dev/guide/why.html)
- [esbuild vs SWC vs Babel](https://github.com/privatenumber/esbuild-vs-swc)
- [Turborepo vs Nx](https://vercel.com/blog/turborepo-vs-nx)

### Performance Optimization
- [Webpack Performance Guide](https://webpack.js.org/guides/build-performance/)
- [Vite Performance](https://vitejs.dev/guide/performance.html)
- [Bundle Analysis Tools](https://github.com/webpack-contrib/webpack-bundle-analyzer)

## Contributing

We welcome contributions! Please see the main repository's contributing guidelines.

## License

MIT License - see LICENSE file for details.

## Support

For issues, questions, or contributions:
- GitHub Issues: [claude-code-agent-marketplace](https://github.com/anthropics/claude-code-agent-marketplace/issues)
- Documentation: [Agent Marketplace Docs](https://github.com/anthropics/claude-code-agent-marketplace)

---

**Build faster. Ship faster. Delight developers.**
