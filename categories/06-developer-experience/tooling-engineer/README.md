# Tooling Engineer Agent

Expert tooling engineer specializing in developer tool creation, CLI development, and productivity enhancement. Masters tool architecture, plugin systems, and user experience design with focus on building efficient, extensible tools that significantly improve developer workflows.

## Overview

The Tooling Engineer agent is your expert partner in creating powerful developer tools that enhance productivity and streamline workflows. From CLI applications to build systems, code generators to IDE extensions, this agent brings deep expertise in tool architecture, performance optimization, and user experience design.

## Core Capabilities

### Tool Development
- **CLI Tools**: Command-line interfaces with intuitive commands and excellent UX
- **Build Systems**: Compilation pipelines with caching, parallelization, and incremental builds
- **Code Generators**: Template-based and AST-driven code generation tools
- **IDE Extensions**: Language servers, code actions, and debugging integrations
- **Linters/Formatters**: Static analysis tools with auto-fixing capabilities
- **Migration Tools**: Automated code transformation and upgrade utilities
- **Testing Tools**: Test runners, coverage reporters, and benchmark suites
- **Performance Tools**: Profilers, analyzers, and optimization utilities

### Architecture Expertise
- **Plugin Systems**: Extensible architectures with hooks and event systems
- **Configuration Management**: Multi-layer config with validation and merging
- **Event-Driven Design**: Event emitters, middleware patterns, and pipelines
- **Error Recovery**: Graceful degradation and clear error handling
- **Auto-Updates**: Self-updating mechanisms with rollback support
- **Cross-Platform**: Windows, macOS, and Linux compatibility

### Performance Optimization
- **Startup Time**: Sub-100ms tool initialization
- **Memory Efficiency**: Streaming, pooling, and efficient resource usage
- **CPU Optimization**: Parallel processing and algorithm optimization
- **I/O Performance**: Async operations and batch processing
- **Caching**: Multi-level caching strategies for speed

## Quick Start

### Using with Claude Desktop

1. **Add to your Claude Desktop config** (`claude_desktop_config.json`):

```json
{
  "agents": {
    "tooling-engineer": {
      "path": "/path/to/categories/06-developer-experience/tooling-engineer"
    }
  }
}
```

2. **Configure MCP servers** (optional but recommended):

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "your-token-here"
      }
    }
  }
}
```

3. **Invoke the agent** in your conversation:
```
@tooling-engineer help me create a CLI tool for project scaffolding
```

## Slash Commands

### /tool-create
Create a new developer tool from scratch.

**Usage**: `/tool-create <tool-type> <tool-name>`

**Examples**:
```
/tool-create cli project-initializer
/tool-create linter code-quality-checker
/tool-create generator api-scaffold
/tool-create build-tool fast-bundler
```

**What it does**:
1. Analyzes tool requirements and target audience
2. Designs optimal command structure and API
3. Implements core functionality with best practices
4. Adds configuration system and environment support
5. Creates comprehensive documentation
6. Sets up testing infrastructure
7. Optimizes for performance (< 100ms startup)
8. Packages for distribution

**Tool types**:
- `cli` - Command-line interface tools
- `build-tool` - Build systems and bundlers
- `linter` - Code analysis and linting tools
- `formatter` - Code formatting utilities
- `generator` - Code generation and scaffolding tools
- `migration-tool` - Code transformation utilities
- `testing-tool` - Test runners and frameworks
- `debug-tool` - Debugging and profiling tools

### /tool-plugin
Add a plugin system to an existing tool.

**Usage**: `/tool-plugin <tool-path>`

**Examples**:
```
/tool-plugin ./my-cli-tool
/tool-plugin /path/to/build-system
```

**What it does**:
1. Analyzes existing tool architecture
2. Designs plugin API with hooks and events
3. Implements plugin discovery and loader
4. Creates plugin registry and lifecycle management
5. Adds plugin configuration and validation
6. Documents plugin development guide
7. Creates example plugins
8. Sets up plugin testing framework

**Features added**:
- Hook system for extensibility
- Plugin discovery mechanism
- Dependency resolution between plugins
- Version compatibility checking
- Plugin lifecycle management
- Comprehensive plugin API documentation

### /tool-distribute
Package and distribute a tool across multiple platforms.

**Usage**: `/tool-distribute <tool-path> <targets>`

**Examples**:
```
/tool-distribute ./my-tool npm,homebrew
/tool-distribute ./cli-app github-releases,docker
/tool-distribute ./build-tool npm,cargo,pip
```

**Distribution targets**:
- `npm` - Node.js package registry
- `cargo` - Rust crate registry
- `pip` - Python package index
- `homebrew` - macOS package manager
- `apt` / `yum` - Linux package managers
- `chocolatey` - Windows package manager
- `docker` - Container images
- `github-releases` - GitHub release binaries

**What it does**:
1. Validates tool completeness and quality
2. Runs full test suite
3. Updates version and generates changelog
4. Builds for target platforms
5. Creates distribution packages
6. Generates checksums and signatures
7. Creates release notes
8. Publishes to specified registries

## Example Usage Scenarios

### Creating a Project Scaffolding CLI

```
@tooling-engineer I need a CLI tool that scaffolds new projects with templates.
It should support multiple frameworks (React, Vue, Next.js) and include
interactive prompts for configuration.

/tool-create cli project-scaffold
```

The agent will:
- Design an intuitive command structure (`scaffold init`, `scaffold add`, etc.)
- Implement template engine with variable interpolation
- Create interactive prompts with framework selection
- Add configuration management
- Generate comprehensive documentation
- Set up testing with multiple scenarios
- Optimize for fast startup (< 100ms)
- Package for npm distribution

### Adding Plugins to a Build Tool

```
@tooling-engineer I have a build tool at ./my-bundler and want to make it
extensible with plugins. Users should be able to add custom transformers,
loaders, and optimization plugins.

/tool-plugin ./my-bundler
```

The agent will:
- Analyze the build tool's architecture
- Design a plugin API with hooks at key stages
- Implement plugin loader with priority support
- Add plugin configuration and validation
- Create example plugins (transformer, loader, optimizer)
- Document the plugin development guide
- Set up plugin testing framework

### Distributing Across Platforms

```
@tooling-engineer My CLI tool is ready for distribution. Please package it
for npm, homebrew, and docker.

/tool-distribute ./my-cli npm,homebrew,docker
```

The agent will:
- Validate tool quality and completeness
- Run comprehensive tests
- Build cross-platform binaries
- Create npm package with proper metadata
- Generate homebrew formula
- Build optimized docker image
- Create release notes and documentation
- Publish to specified registries

## MCP Server Integration

### Filesystem Server
**Purpose**: Access and manage tool files, configurations, and templates

**Use cases**:
- Read/write package.json and tool manifests
- Manage plugin directories
- Access template files for code generation
- Handle build scripts and configuration files
- Modify CLI command definitions

### GitHub Server
**Purpose**: Publish tools and manage releases

**Use cases**:
- Publish CLI tools as GitHub releases
- Create and manage version tags
- Track feature requests and bug reports
- Review tool improvement PRs
- Manage changelogs and release notes
- Set up GitHub Actions for distribution

### Context7 Server
**Purpose**: Search tool documentation and best practices

**Use cases**:
- Find CLI framework documentation (commander, yargs, oclif)
- Search plugin architecture patterns
- Discover build tool implementations
- Research code generation techniques
- Find performance optimization strategies
- Look up tool distribution best practices

### Fetch Server
**Purpose**: Download templates and access package registries

**Use cases**:
- Download CLI tool templates and boilerplates
- Access npm/cargo/pip registries for package info
- Fetch tool documentation and guides
- Download example plugin implementations
- Retrieve configuration schemas
- Access build tool examples

## Performance Targets

All tools created by this agent aim to meet or exceed these targets:

- **Startup Time**: < 100ms (CLI tools)
- **Memory Usage**: < 50MB baseline
- **Install Size**: < 10MB (CLI tools)
- **Test Coverage**: > 80%
- **Build Time**: Optimized for incremental builds
- **Cross-Platform**: Full Windows, macOS, Linux support

## Best Practices

### CLI Development
1. **Intuitive Commands**: Use clear, discoverable command names
2. **Progressive Disclosure**: Start simple, reveal complexity as needed
3. **Helpful Errors**: Provide actionable error messages with suggestions
4. **Shell Completions**: Support bash, zsh, and fish completions
5. **Configuration**: Support env vars, config files, and CLI flags
6. **Updates**: Implement auto-update checks

### Tool Architecture
1. **Plugin System**: Design for extensibility from day one
2. **Event-Driven**: Use hooks and events for flexibility
3. **Layered Config**: Support multiple configuration sources
4. **Error Recovery**: Fail gracefully with clear recovery paths
5. **Logging**: Structured logging with appropriate levels
6. **Testing**: High coverage with unit, integration, and E2E tests

### Performance
1. **Lazy Loading**: Load modules only when needed
2. **Caching**: Multi-level caching for speed
3. **Parallel Processing**: Use workers for CPU-intensive tasks
4. **Streaming**: Process large files without loading into memory
5. **Resource Pooling**: Reuse allocated resources
6. **Profiling**: Regular performance measurement

### User Experience
1. **Clear Feedback**: Progress bars and status messages
2. **Sensible Defaults**: Works great out of the box
3. **Help Discovery**: Contextual help and examples
4. **Error Handling**: Clear messages with recovery suggestions
5. **Documentation**: Comprehensive guides and references
6. **Examples**: Real-world usage examples

## Integration with Other Agents

The Tooling Engineer collaborates effectively with:

- **dx-optimizer**: On workflow analysis and productivity improvements
- **cli-developer**: On CLI patterns and best practices
- **build-engineer**: On build system design and optimization
- **documentation-engineer**: On tool documentation
- **devops-engineer**: On deployment automation
- **refactoring-specialist**: On code transformation tools
- **dependency-manager**: On package management tools
- **git-workflow-manager**: On Git-related tools

## Common Tool Categories

### CLI Tools
Command-line interfaces for various tasks:
- Project scaffolding and initialization
- Code generation and boilerplate creation
- Development workflow automation
- Configuration management
- Deployment and release automation

### Build Tools
Compilation and bundling systems:
- Fast bundlers with caching
- Incremental build systems
- Multi-target compilation
- Asset optimization
- Source map generation

### Linters/Formatters
Code quality and style tools:
- Custom linting rules
- Auto-fixing capabilities
- IDE integration
- Git hook integration
- Configurable rulesets

### Code Generators
Template-based generation:
- Component scaffolding
- API client generation
- Type generation from schemas
- Migration script generation
- Boilerplate reduction

### Migration Tools
Code transformation utilities:
- API migration helpers
- Dependency upgrade automation
- Breaking change detection
- Codebase-wide refactoring
- Version migration scripts

## Technical Stack

### Recommended Tools

**CLI Frameworks**:
- commander - Full-featured CLI framework
- yargs - Powerful argument parser
- oclif - Extensible CLI framework
- inquirer - Interactive prompts
- chalk - Terminal string styling

**Build Tools**:
- esbuild - Extremely fast bundler
- rollup - Module bundler
- webpack - Feature-rich bundler
- vite - Fast development build tool
- tsup - TypeScript bundler

**Code Generation**:
- plop - Micro-generator framework
- hygen - Code generator with templates
- yeoman-generator - Scaffolding tool
- ejs - Template engine
- handlebars - Template engine

**Testing**:
- jest - JavaScript testing framework
- vitest - Vite-native test runner
- ava - Test runner with concurrency
- mocha - Flexible testing framework
- chai - Assertion library

## Support and Documentation

### Getting Help
- Check agent documentation in CLAUDE.md
- Review example tools and templates
- Consult slash command guides
- Ask the agent for specific scenarios

### Contributing
- Share tool templates and examples
- Report issues and suggest improvements
- Contribute plugin examples
- Improve documentation

### Resources
- Tool architecture patterns
- Performance optimization guides
- Distribution best practices
- Plugin development guides

## License

MIT License - See LICENSE file for details

## Version

1.0.0

---

Built with expertise in developer tooling, CLI development, and productivity enhancement. Optimized for creating tools that developers love to use.
