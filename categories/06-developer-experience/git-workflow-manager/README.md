# Git Workflow Manager Agent

Expert Git workflow manager specializing in branching strategies, automation, and team collaboration. Masters Git workflows, merge conflict resolution, and repository management with focus on enabling efficient, clear, and scalable version control practices.

## Overview

The Git Workflow Manager agent helps teams optimize their version control workflows through strategic branching models, automated processes, and best practices. It reduces merge conflicts, accelerates code review cycles, and streamlines release management while maintaining clean git history.

## Key Features

- **Branching Strategy Implementation**: Git Flow, GitHub Flow, GitLab Flow, and trunk-based development
- **Pull Request Automation**: Automated PR creation, review assignment, and merge management
- **Merge Conflict Resolution**: Proactive strategies and resolution assistance
- **Release Management**: Automated versioning, changelog generation, and release coordination
- **Git Hooks**: Pre-commit validation, commit message formatting, and quality gates
- **Team Collaboration**: Code review workflows, commit conventions, and communication protocols

## Quick Start

### Prerequisites

1. **GitHub Personal Access Token** (required for full functionality)
   ```bash
   export GITHUB_PERSONAL_ACCESS_TOKEN="your_token_here"
   ```

   Required scopes:
   - `repo` - Full repository access
   - `workflow` - GitHub Actions workflow management
   - `admin:repo_hook` - Repository webhook management

2. **MCP Server Installation**
   ```bash
   # GitHub MCP server
   npm install -g @modelcontextprotocol/server-github

   # Filesystem MCP server (optional)
   npm install -g @modelcontextprotocol/server-filesystem
   ```

### Installation

1. Copy the agent directory to your MCP-enabled environment
2. Configure MCP servers using the provided `mcp-config.json`
3. Start your Claude Code session with the agent

### Basic Usage

```bash
# Invoke the agent
@git-workflow-manager "Help me set up a GitHub Flow workflow for my team"

# Create a feature branch
@git-workflow-manager /git-branch feature PROJ-123 "Add user authentication"

# Create a pull request
@git-workflow-manager /git-pr "Add user authentication feature" --base develop

# Sync branch with upstream
@git-workflow-manager /git-sync --rebase

# Prepare a release
@git-workflow-manager /git-release v1.2.0 --changelog
```

## Slash Commands

### /git-branch

Create a new branch following team naming conventions.

**Syntax:**
```
/git-branch <type> [ticket] <description>
```

**Types:**
- `feature` - New feature development
- `bugfix` - Bug fixes
- `hotfix` - Critical production fixes
- `release` - Release preparation

**Examples:**
```bash
# Feature branch with ticket number
@git-workflow-manager /git-branch feature TICKET-123 "Add user authentication"

# Bug fix branch
@git-workflow-manager /git-branch bugfix TICKET-456 "Fix login redirect"

# Hotfix without ticket
@git-workflow-manager /git-branch hotfix "Critical security patch"

# Release branch
@git-workflow-manager /git-branch release v1.2.0
```

**What it does:**
1. Validates current repository state
2. Pulls latest changes from base branch
3. Creates branch with proper naming convention
4. Pushes to remote with tracking
5. Provides next steps and recommendations

### /git-pr

Create a pull request with comprehensive description and proper metadata.

**Syntax:**
```
/git-pr <title> [--base <branch>] [--labels <labels>] [--milestone <milestone>] [--draft]
```

**Options:**
- `--base` - Target branch (default: main)
- `--labels` - Comma-separated labels
- `--milestone` - Associated milestone
- `--draft` - Create as draft PR

**Examples:**
```bash
# Basic PR to main
@git-workflow-manager /git-pr "Add user authentication feature"

# PR to develop with labels
@git-workflow-manager /git-pr "Fix critical bug" --base develop --labels bug,priority-high

# Release PR with milestone
@git-workflow-manager /git-pr "Release v1.2.0" --milestone v1.2.0

# Draft PR for early feedback
@git-workflow-manager /git-pr "WIP: New feature" --draft
```

**What it does:**
1. Analyzes all commits since branch diverged
2. Generates comprehensive PR description with:
   - Summary of changes
   - Test plan
   - Related issues
   - Breaking changes
   - Screenshots (if applicable)
3. Applies appropriate labels
4. Links related issues automatically
5. Assigns reviewers based on CODEOWNERS
6. Sets milestone if specified
7. Returns PR URL for review

### /git-sync

Synchronize current branch with upstream/base branch.

**Syntax:**
```
/git-sync [--rebase] [--from <branch>]
```

**Options:**
- `--rebase` - Use rebase instead of merge
- `--from` - Source branch (default: main)

**Examples:**
```bash
# Sync with main using merge
@git-workflow-manager /git-sync

# Sync with rebase
@git-workflow-manager /git-sync --rebase

# Sync from develop
@git-workflow-manager /git-sync --from develop

# Rebase from develop
@git-workflow-manager /git-sync --rebase --from develop
```

**What it does:**
1. Fetches latest changes from remote
2. Checks for potential conflicts
3. Performs merge or rebase based on strategy
4. Pushes changes if successful
5. Reports conflicts with resolution guidance

### /git-release

Prepare and create a release branch with full automation.

**Syntax:**
```
/git-release <version> [--from <branch>] [--changelog]
```

**Options:**
- `--from` - Source branch (default: develop)
- `--changelog` - Generate changelog automatically

**Examples:**
```bash
# Basic release
@git-workflow-manager /git-release v1.2.0

# Release from develop with changelog
@git-workflow-manager /git-release v2.0.0 --from develop --changelog

# Hotfix release from main
@git-workflow-manager /git-release v1.1.1 --from main
```

**What it does:**
1. Creates release branch with proper naming
2. Updates version numbers in package files
3. Generates changelog from commits (if requested)
4. Creates release PR to main
5. Prepares tag for after merge
6. Creates GitHub release with notes and assets
7. Plans merge back to develop

## Workflow Models

### Git Flow

Best for projects with scheduled releases and multiple versions in production.

**Branches:**
- `main` - Production-ready code
- `develop` - Integration branch
- `feature/*` - Feature development
- `release/*` - Release preparation
- `hotfix/*` - Emergency fixes

**Usage:**
```bash
# Start feature
@git-workflow-manager /git-branch feature PROJ-123 "New feature"

# Create PR to develop
@git-workflow-manager /git-pr "Add feature" --base develop

# Start release
@git-workflow-manager /git-release v1.2.0 --from develop --changelog

# Emergency hotfix
@git-workflow-manager /git-branch hotfix "Critical fix"
```

### GitHub Flow

Best for continuous deployment and web applications.

**Branches:**
- `main` - Always deployable
- `feature/*` - All development

**Usage:**
```bash
# Create feature branch
@git-workflow-manager /git-branch feature PROJ-123 "New feature"

# Create PR to main
@git-workflow-manager /git-pr "Add feature"

# Deploy from main after merge
```

### Trunk-Based Development

Best for teams practicing continuous integration.

**Branches:**
- `main` - Single integration branch
- Short-lived feature branches

**Usage:**
```bash
# Create short-lived branch
@git-workflow-manager /git-branch feature PROJ-123 "Quick fix"

# Sync frequently
@git-workflow-manager /git-sync --rebase

# Merge quickly
@git-workflow-manager /git-pr "Quick fix" --labels fast-track
```

## Common Workflows

### Feature Development

```bash
# 1. Create feature branch
@git-workflow-manager /git-branch feature PROJ-123 "User authentication"

# 2. Make changes and commit
git add .
git commit -m "feat(auth): add login endpoint"

# 3. Keep branch updated
@git-workflow-manager /git-sync --rebase

# 4. Create PR when ready
@git-workflow-manager /git-pr "Add user authentication" --labels enhancement

# 5. Address review feedback
git add .
git commit -m "fix(auth): address review comments"

# 6. Merge after approval
```

### Bug Fix

```bash
# 1. Create bugfix branch
@git-workflow-manager /git-branch bugfix PROJ-456 "Login redirect issue"

# 2. Fix the bug
git add .
git commit -m "fix(auth): correct redirect after login"

# 3. Create PR
@git-workflow-manager /git-pr "Fix login redirect" --labels bug,priority-high

# 4. Merge and deploy
```

### Hotfix

```bash
# 1. Create hotfix from main
@git-workflow-manager /git-branch hotfix "Security vulnerability"

# 2. Fix critical issue
git add .
git commit -m "fix(security): patch XSS vulnerability"

# 3. Create PR to main
@git-workflow-manager /git-pr "Security hotfix" --labels security,critical

# 4. Also merge to develop
@git-workflow-manager /git-pr "Security hotfix" --base develop

# 5. Tag and deploy
```

### Release Preparation

```bash
# 1. Create release branch
@git-workflow-manager /git-release v1.2.0 --from develop --changelog

# 2. Review generated changelog
# Agent will create CHANGELOG.md

# 3. Make final adjustments
git add .
git commit -m "chore(release): prepare v1.2.0"

# 4. Create release PR
# Agent handles this automatically

# 5. Merge and tag
# Agent creates tag after PR merge
```

## Configuration

### Branch Naming Conventions

Default patterns (configurable in `mcp-config.json`):

```
feature/TICKET-123-short-description
bugfix/TICKET-456-bug-description
hotfix/critical-security-fix
release/v1.2.0
```

### Commit Message Format

Following Conventional Commits:

```
type(scope): subject

body

footer
```

**Types:**
- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation
- `style` - Formatting
- `refactor` - Code restructuring
- `test` - Testing
- `chore` - Maintenance
- `perf` - Performance
- `ci` - CI/CD changes
- `build` - Build system

**Example:**
```
feat(auth): add OAuth2 authentication

Implement OAuth2 flow for third-party authentication.
Supports Google, GitHub, and Microsoft providers.

Closes #123
BREAKING CHANGE: Removes basic auth support
```

### Merge Strategies

Configure in repository or per PR:

- **Merge commit** - Preserves full history
- **Squash and merge** - Single commit per feature
- **Rebase and merge** - Linear history

### Branch Protection

Recommended settings:

```json
{
  "required_reviews": 1,
  "require_code_owner_reviews": true,
  "dismiss_stale_reviews": true,
  "require_status_checks": true,
  "enforce_admins": false,
  "required_checks": [
    "ci/tests",
    "ci/lint",
    "ci/security-scan"
  ]
}
```

## Git Hooks

### Pre-commit Hook

Installed via agent:

```bash
@git-workflow-manager "Set up pre-commit hooks for linting and formatting"
```

Example hook:
```bash
#!/bin/sh
# Run linter
npm run lint

# Check for secrets
git diff --cached --name-only | xargs git-secrets --scan

# Format code
npm run format
```

### Commit Message Hook

Validates commit message format:

```bash
#!/bin/sh
# Validate conventional commit format
commit_msg=$(cat $1)
pattern="^(feat|fix|docs|style|refactor|test|chore|perf|ci|build|revert)(\(.+\))?: .{1,72}"

if ! echo "$commit_msg" | grep -qE "$pattern"; then
  echo "ERROR: Commit message doesn't follow conventional format"
  exit 1
fi
```

### Pre-push Hook

Runs tests before push:

```bash
#!/bin/sh
# Run test suite
npm test

if [ $? -ne 0 ]; then
  echo "ERROR: Tests failed. Fix before pushing."
  exit 1
fi
```

## Best Practices

### Commits

- Write clear, descriptive messages
- Follow conventional commit format
- Make atomic commits (one logical change)
- Test before committing
- Sign commits when required

### Branches

- Use descriptive names
- Follow naming conventions
- Keep branches short-lived
- Delete after merging
- Protect important branches

### Pull Requests

- Keep PRs small and focused
- Write comprehensive descriptions
- Link related issues
- Request appropriate reviewers
- Respond to feedback promptly
- Ensure CI passes before merge

### Code Review

- Review your own code first
- Be constructive and respectful
- Focus on code quality
- Explain reasoning for suggestions
- Approve when standards are met

## Integration with Other Agents

The Git Workflow Manager collaborates with:

- **devops-engineer** - CI/CD pipeline integration
- **release-manager** - Version management
- **security-auditor** - Security policies
- **code-reviewer** - Code quality standards
- **documentation-engineer** - Documentation updates
- **qa-expert** - Testing workflows
- **team-lead** - Team optimization
- **project-manager** - Project tracking

## Metrics and Success

Track workflow effectiveness:

- **Merge conflict frequency** - Target: <5% of PRs
- **PR review time** - Target: <24 hours
- **Time to merge** - Target: <48 hours
- **Build success rate** - Target: >95%
- **Deployment frequency** - Target: Daily
- **Lead time for changes** - Target: <1 week
- **Change failure rate** - Target: <5%
- **Mean time to recovery** - Target: <1 hour

## Troubleshooting

### Common Issues

**Merge Conflicts**
```bash
# Get help resolving conflicts
@git-workflow-manager "I have merge conflicts in feature/auth-update"

# Sync before creating PR
@git-workflow-manager /git-sync --rebase
```

**Failed CI Checks**
```bash
# Review failures and get guidance
@git-workflow-manager "My PR failed CI checks, help me fix them"
```

**Branch Protection Issues**
```bash
# Configure branch protection
@git-workflow-manager "Set up branch protection for main and develop"
```

**Stale Branches**
```bash
# Clean up old branches
@git-workflow-manager "List and delete merged branches"
```

## Examples

### Setup New Repository Workflow

```bash
@git-workflow-manager "Set up a GitHub Flow workflow for my team. We deploy continuously to production."

# Agent will:
# 1. Configure branch protection for main
# 2. Set up PR templates
# 3. Configure required status checks
# 4. Install git hooks
# 5. Document workflow for team
```

### Optimize Existing Workflow

```bash
@git-workflow-manager "Our team has frequent merge conflicts and slow PR reviews. Help optimize our workflow."

# Agent will:
# 1. Analyze current workflow
# 2. Review merge conflict patterns
# 3. Assess PR review bottlenecks
# 4. Recommend improvements
# 5. Implement automation
# 6. Set up monitoring
```

### Release Management

```bash
@git-workflow-manager "Automate our release process with semantic versioning and changelog generation."

# Agent will:
# 1. Set up semantic versioning
# 2. Configure changelog automation
# 3. Create release templates
# 4. Set up tag automation
# 5. Configure GitHub releases
```

## Resources

- [Git Flow Documentation](https://nvie.com/posts/a-successful-git-branching-model/)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Semantic Versioning](https://semver.org/)
- [GitHub MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/github)

## Support

For issues or questions:
1. Check the troubleshooting section
2. Review the documentation
3. Consult with the agent for specific guidance

## License

MIT License - See repository for details
