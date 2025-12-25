# Dependency Manager Agent

Expert dependency manager specializing in package management, security auditing, and version conflict resolution across multiple ecosystems. Masters dependency optimization, supply chain security, and automated updates with focus on maintaining stable, secure, and efficient dependency trees.

## Overview

The Dependency Manager agent is your expert partner for managing complex dependency ecosystems across NPM, Python, Rust, Java, Go, Ruby, and PHP. It provides comprehensive security scanning, intelligent version conflict resolution, automated updates, and performance optimization to keep your dependencies secure, up-to-date, and efficient.

## Key Features

- **Multi-Ecosystem Support**: NPM/Yarn/PNPM, pip/poetry, Cargo, Maven/Gradle, Go modules, Bundler, Composer
- **Security Vulnerability Scanning**: CVE database integration, OSV, Snyk, GitHub Advisory
- **Version Conflict Resolution**: Intelligent dependency graph analysis and resolution strategies
- **Automated Updates**: Safe, tested updates with automated PR creation
- **License Compliance**: Audit licenses and ensure organizational policy compliance
- **Supply Chain Security**: Package verification, signature checking, typosquatting detection
- **Bundle Optimization**: Size analysis, tree shaking, duplicate removal
- **Monorepo Management**: Workspace configuration and version synchronization
- **SBOM Generation**: Software Bill of Materials for compliance and security

## Quick Start

### Prerequisites

1. **GitHub Personal Access Token**: Required for PR creation and security advisories
   ```bash
   export GITHUB_PERSONAL_ACCESS_TOKEN="ghp_your_token_here"
   ```
   Token scopes needed: `repo`, `security_events`, `workflow`

2. **Context7 API Key**: Required for package registry and vulnerability data
   ```bash
   export CONTEXT7_API_KEY="your_context7_api_key"
   ```
   Sign up at https://context7.com to get your API key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/anthropics/claude-code-agent-marketplace.git
   cd claude-code-agent-marketplace/categories/06-developer-experience/dependency-manager
   ```

2. Set environment variables (see Prerequisites above)

3. Launch Claude Desktop with this agent or use via Claude CLI

## Slash Commands

### /deps-audit

Perform comprehensive security and compliance audit of all dependencies.

**Syntax**:
```
/deps-audit [--ecosystem <npm|pip|cargo|maven|go>] [--severity <critical|high|medium|low>]
```

**Examples**:
```bash
# Audit all dependencies across all ecosystems
/deps-audit

# Audit only NPM dependencies for critical vulnerabilities
/deps-audit --ecosystem npm --severity critical

# Audit Python dependencies for high and critical issues
/deps-audit --ecosystem pip --severity high
```

**Output**:
- List of vulnerabilities with CVE IDs and CVSS scores
- Affected packages and versions
- Available patches or updates
- Remediation recommendations
- License compliance status
- Detailed audit report

### /deps-update

Safely update dependencies with automated testing and rollback capabilities.

**Syntax**:
```
/deps-update [--type <major|minor|patch>] [--package <name>] [--dry-run]
```

**Examples**:
```bash
# Update all patch versions (safest)
/deps-update --type patch

# Preview what would be updated without making changes
/deps-update --type minor --dry-run

# Update specific package to latest minor version
/deps-update --package lodash --type minor

# Update all to latest major versions (review carefully!)
/deps-update --type major
```

**Output**:
- List of packages to update with current and target versions
- Breaking changes detected in changelogs
- Test results for each update
- Pull request with detailed changelog
- Rollback instructions if needed

### /deps-analyze

Analyze dependency tree for optimization and security insights.

**Syntax**:
```
/deps-analyze [--depth <number>] [--show-unused] [--show-duplicates]
```

**Examples**:
```bash
# Basic dependency tree analysis
/deps-analyze

# Show unused dependencies and duplicates
/deps-analyze --show-unused --show-duplicates

# Analyze only top 5 levels of dependency tree
/deps-analyze --depth 5

# Find all duplicate packages
/deps-analyze --show-duplicates
```

**Output**:
- Visual dependency tree
- Circular dependencies detected
- Unused dependencies that can be removed
- Duplicate packages at different versions
- Bundle size impact analysis
- Optimization recommendations
- Estimated size and build time savings

## MCP Server Integration

This agent uses four MCP servers for enhanced capabilities:

### 1. Filesystem MCP
**Purpose**: Access and modify dependency files

**Capabilities**:
- Read package manifests (package.json, requirements.txt, Cargo.toml, pom.xml, go.mod)
- Update lock files (package-lock.json, yarn.lock, poetry.lock, Cargo.lock)
- Manage registry configuration (.npmrc, .pypirc, settings.xml)
- Create backup files before updates

### 2. GitHub MCP
**Purpose**: Integrate with GitHub for PR creation and security alerts

**Capabilities**:
- Create automated dependency update pull requests
- Review and manage Dependabot alerts
- Access GitHub security advisories
- Monitor CI/CD pipeline results for dependency changes
- Comment on PRs with test results and changelogs

**Setup**:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN="ghp_your_token_here"
```

### 3. Context7 MCP
**Purpose**: Query package registries and vulnerability databases

**Capabilities**:
- Fetch package metadata from NPM, PyPI, crates.io, Maven Central
- Query CVE and vulnerability databases
- Retrieve changelogs and deprecation notices
- Access license information and compatibility data
- Get package download statistics and popularity metrics

**Setup**:
```bash
export CONTEXT7_API_KEY="your_context7_api_key"
```
Sign up at https://context7.com

### 4. Fetch MCP
**Purpose**: Access external package registry and security APIs

**Capabilities**:
- Query package registries (npmjs.org, pypi.org, crates.io)
- Fetch security advisories (OSV, Snyk, GitHub Advisory Database)
- Retrieve SBOM data
- Access bundlephobia for size analysis
- Check libraries.io for package health

## Common Use Cases

### 1. Security Vulnerability Remediation

**Scenario**: Your project has known vulnerabilities that need immediate patching.

**Workflow**:
```bash
# Step 1: Audit for vulnerabilities
/deps-audit --severity critical

# Step 2: Review the report and identified CVEs

# Step 3: Update packages with critical fixes
/deps-update --type patch

# Step 4: Verify fixes in the generated PR
```

**Result**: Critical vulnerabilities patched, PR created with test results, security improved.

### 2. Dependency Optimization

**Scenario**: Your bundle is too large and build times are slow.

**Workflow**:
```bash
# Step 1: Analyze dependency tree
/deps-analyze --show-unused --show-duplicates

# Step 2: Review unused dependencies and duplicates

# Step 3: Remove unused packages (agent will help)

# Step 4: Deduplicate versions

# Step 5: Measure improvement
```

**Result**: Smaller bundle size, faster builds, reduced node_modules size.

### 3. License Compliance Audit

**Scenario**: You need to ensure all dependencies comply with your organization's license policy.

**Workflow**:
```bash
# Step 1: Run full audit including licenses
/deps-audit

# Step 2: Review license compliance report

# Step 3: Flag or replace non-compliant packages

# Step 4: Generate attribution file for legal
```

**Result**: Full license compliance, legal risk mitigated, attribution documentation.

### 4. Monorepo Management

**Scenario**: You have multiple packages in a monorepo with version conflicts.

**Workflow**:
```bash
# Step 1: Analyze all workspace packages
/deps-analyze

# Step 2: Identify version conflicts across workspaces

# Step 3: Synchronize shared dependency versions

# Step 4: Configure workspace hoisting
```

**Result**: Consistent versions across packages, optimized disk usage, faster installs.

### 5. Automated Weekly Updates

**Scenario**: You want to keep dependencies current with minimal manual work.

**Workflow**:
```bash
# Every Monday, run:
/deps-update --type patch --dry-run

# Review what would update, then:
/deps-update --type patch

# Review PR, verify tests pass, merge
```

**Result**: Dependencies stay current, security patches applied promptly, minimal manual effort.

## Supported Ecosystems

### NPM/Yarn/PNPM (JavaScript/TypeScript)
**Files**: `package.json`, `package-lock.json`, `yarn.lock`, `pnpm-lock.yaml`
**Features**: Workspace management, peer dependency resolution, audit integration

### Python (pip/poetry/pipenv)
**Files**: `requirements.txt`, `pyproject.toml`, `poetry.lock`, `Pipfile`
**Features**: Virtual environment management, dependency groups, poetry support

### Rust (Cargo)
**Files**: `Cargo.toml`, `Cargo.lock`
**Features**: Workspace configuration, feature flags, crates.io integration

### Java (Maven/Gradle)
**Files**: `pom.xml`, `build.gradle`, `build.gradle.kts`
**Features**: Dependency scopes, BOM handling, repository configuration

### Go (Go Modules)
**Files**: `go.mod`, `go.sum`
**Features**: Module proxy configuration, version retraction, vendoring

### Ruby (Bundler)
**Files**: `Gemfile`, `Gemfile.lock`
**Features**: Bundle groups, private gem sources

### PHP (Composer)
**Files**: `composer.json`, `composer.lock`
**Features**: Platform requirements, autoloader optimization

## Best Practices

### Security
- Run `/deps-audit` daily to catch new vulnerabilities early
- Patch critical vulnerabilities within 24 hours
- Subscribe to security advisories for critical packages
- Use lock files for reproducible builds

### Updates
- Patch versions: Update weekly
- Minor versions: Update monthly
- Major versions: Update quarterly with careful testing
- Always run full test suite before merging

### Version Management
- Pin exact versions in production
- Use ranges (^, ~) in development
- Document version constraints rationale
- Maintain compatibility matrix for major updates

### Performance
- Monitor bundle size impact of new dependencies
- Remove unused dependencies regularly
- Deduplicate versions to reduce size
- Use tree shaking and code splitting

### Compliance
- Audit licenses before adding new dependencies
- Maintain approved license list
- Generate SBOM for compliance tracking
- Document exemptions with legal approval

## Integration with Other Agents

The Dependency Manager works seamlessly with other agents:

- **security-auditor**: Collaborate on vulnerability remediation and security policies
- **build-engineer**: Support bundle optimization and build time improvements
- **devops-engineer**: Integrate with CI/CD pipelines for automated testing
- **backend-developer**: Guide on package selection and API compatibility
- **frontend-developer**: Help with bundling strategies and tree shaking
- **tooling-engineer**: Assist with automation setup and tooling integration
- **dx-optimizer**: Partner on performance improvements and developer experience
- **architect-reviewer**: Coordinate on dependency policies and standards

## Troubleshooting

### "Cannot find package.json"
**Solution**: Ensure you're in the project root directory with a valid package manifest file.

### "GITHUB_PERSONAL_ACCESS_TOKEN not set"
**Solution**: Export the environment variable with a valid GitHub token (see Prerequisites).

### "Vulnerability scan failed"
**Solution**: Check that CONTEXT7_API_KEY is set and valid. Verify network connectivity.

### "Version conflict cannot be resolved"
**Solution**: Review dependency tree with `/deps-analyze` and consider using resolutions or overrides.

### "Tests failed after update"
**Solution**: Review breaking changes in changelog, adjust code, or rollback using provided instructions.

## Configuration

### Custom Update Policies

Create a `.dependency-manager.json` in your project root:

```json
{
  "updatePolicy": {
    "patch": "auto",
    "minor": "review",
    "major": "manual"
  },
  "licensePolicy": {
    "allowed": ["MIT", "Apache-2.0", "BSD-3-Clause"],
    "flagged": ["GPL-3.0", "AGPL-3.0"]
  },
  "securityPolicy": {
    "criticalPatchTime": "24h",
    "highPatchTime": "7d",
    "mediumPatchTime": "30d"
  }
}
```

### Private Registry Configuration

The agent respects existing registry configurations in:
- `.npmrc` for NPM
- `.pypirc` for Python
- `settings.xml` for Maven
- `Cargo.toml` registries for Rust

## Support and Contribution

For issues, questions, or contributions, visit the [Claude Agent Marketplace repository](https://github.com/anthropics/claude-code-agent-marketplace).

## License

MIT License - See LICENSE file for details.

---

**Agent Version**: 1.0.0
**Last Updated**: 2025-12-24
**Maintained by**: Claude Agent Marketplace Team
