# CLI Developer Agent

Expert CLI developer specializing in command-line interface design, developer tools, and terminal applications. Masters user experience, cross-platform compatibility, and building efficient CLI tools that developers love to use.

## Overview

The CLI Developer agent is a senior specialist in creating intuitive, efficient command-line interfaces and developer tools. With expertise spanning argument parsing, interactive prompts, terminal UI, and cross-platform compatibility, this agent helps you build CLI tools that integrate seamlessly into developer workflows.

## Key Capabilities

### CLI Architecture
- Command hierarchy planning and organization
- Subcommand structure design
- Flag and option design patterns
- Configuration management strategies
- Plugin architecture implementation
- State management and exit code handling

### Developer Experience
- Intuitive argument parsing
- Interactive terminal prompts
- Progress indicators and spinners
- Beautiful terminal UI design
- Helpful error messages
- Shell completions (bash, zsh, fish, PowerShell)

### Performance & Quality
- Startup time < 50ms
- Memory usage < 50MB
- Cross-platform compatibility (Linux, macOS, Windows)
- Comprehensive testing strategies
- Performance optimization techniques

### Distribution
- NPM global packages
- Homebrew formulas
- Binary releases
- Docker images
- Auto-update mechanisms

## Supported Frameworks & Libraries

### Node.js
- **Commander.js** - Simple and flexible command-line interface
- **yargs** - Feature-rich argument parsing
- **oclif** - Full-featured CLI framework
- **Ink** - React for interactive CLIs
- **Inquirer.js** - Interactive prompts
- **chalk** - Terminal string styling
- **cli-table3** - Beautiful table output

### Python
- **Click** - Composable command-line interface toolkit
- **argparse** - Built-in argument parsing
- **rich** - Rich text and beautiful formatting
- **typer** - Modern CLI framework with type hints

### Go
- **Cobra** - Powerful CLI framework
- **urfave/cli** - Simple CLI library

### Rust
- **Clap** - Command-line argument parser
- **structopt** - Parse command-line arguments by defining a struct

## Slash Commands

### `/cli-init`
Initialize a new CLI project with best practices.

**What it does:**
- Prompts for project configuration (name, runtime, framework)
- Generates project structure
- Sets up package configuration
- Creates entry point with argument parsing
- Adds help and version commands
- Includes basic tests
- Generates comprehensive README

**Example usage:**
```
/cli-init
```

Then follow the prompts for:
- Project name and description
- Target runtime (Node.js, Python, Go, Rust)
- Framework preference
- Package manager
- Testing framework
- Distribution method

### `/cli-command`
Add a new command to an existing CLI.

**What it does:**
- Prompts for command details
- Generates command file with boilerplate
- Adds argument parsing logic
- Creates help text
- Generates tests
- Updates documentation

**Example usage:**
```
/cli-command
```

Then specify:
- Command name
- Description
- Arguments (positional)
- Options (flags)
- Subcommands (if any)
- Interactive prompts needed
- Validation rules

### `/cli-publish`
Prepare CLI tool for publishing and distribution.

**What it does:**
- Checks package version
- Audits dependencies
- Verifies test coverage
- Validates documentation
- Confirms shell completions
- Tests cross-platform compatibility
- Generates distribution packages
- Creates installation instructions
- Guides through publishing process

**Example usage:**
```
/cli-publish
```

Supports:
- NPM publishing (Node.js)
- PyPI publishing (Python)
- Homebrew formula creation
- Binary releases
- GitHub releases

## MCP Integration

This agent uses three MCP servers for enhanced functionality:

### filesystem
Access and manage CLI project files, read/write source code, and navigate directory structures.

### github
Access GitHub for CLI examples, best practices, issue tracking, and repository management.

### context7
Maintain CLI development context, track architectural decisions, and store performance benchmarks.

## Performance Targets

The CLI Developer agent helps you achieve:

- **Startup time:** < 50ms
- **Memory usage:** < 50MB
- **Test coverage:** > 80%
- **Cross-platform:** Linux, macOS, Windows support

## Use Cases

1. **Creating New CLI Tools**
   - Build from scratch with best practices
   - Choose optimal framework for your use case
   - Implement intuitive command structure

2. **Enhancing Existing CLIs**
   - Add new commands and features
   - Improve user experience
   - Optimize performance

3. **Interactive Workflows**
   - Build guided setup wizards
   - Create configuration tools
   - Implement interactive debugging tools

4. **Developer Tools**
   - Build custom build tools
   - Create deployment scripts
   - Develop testing utilities

5. **Package Distribution**
   - Publish to npm, PyPI, etc.
   - Create Homebrew formulas
   - Build binary releases

## Example Projects

### Simple CLI with Commander.js
```javascript
#!/usr/bin/env node
const { Command } = require('commander');
const program = new Command();

program
  .name('my-cli')
  .description('CLI tool for awesome things')
  .version('1.0.0');

program
  .command('init')
  .description('Initialize a new project')
  .option('-t, --template <type>', 'project template')
  .action((options) => {
    console.log('Initializing project with template:', options.template);
  });

program.parse();
```

### Interactive CLI with Inquirer
```javascript
const inquirer = require('inquirer');

inquirer
  .prompt([
    {
      type: 'input',
      name: 'name',
      message: 'What is your project name?'
    },
    {
      type: 'list',
      name: 'framework',
      message: 'Choose a framework:',
      choices: ['React', 'Vue', 'Angular']
    }
  ])
  .then((answers) => {
    console.log(`Creating ${answers.name} with ${answers.framework}`);
  });
```

### CLI with Progress Indicators
```javascript
const ora = require('ora');

const spinner = ora('Loading...').start();

setTimeout(() => {
  spinner.color = 'yellow';
  spinner.text = 'Processing...';
}, 1000);

setTimeout(() => {
  spinner.succeed('Done!');
}, 2000);
```

## Best Practices

### Command Design
- Use clear, descriptive command names
- Follow common conventions (--verbose, --help, --version)
- Provide sensible defaults
- Make common tasks easy, complex tasks possible

### Error Handling
- Provide clear error messages
- Suggest solutions when possible
- Include debug mode for detailed information
- Use proper exit codes

### Documentation
- Comprehensive help text for each command
- Examples for common use cases
- Installation instructions
- Troubleshooting guide

### Testing
- Unit tests for command logic
- Integration tests for CLI execution
- Cross-platform compatibility tests
- Performance benchmarks

### Performance
- Lazy load dependencies
- Minimize startup time
- Stream large files
- Cache expensive operations

## Integration with Other Agents

The CLI Developer works seamlessly with:

- **tooling-engineer** - Building comprehensive developer toolchains
- **documentation-engineer** - Creating CLI documentation
- **devops-engineer** - Automation and deployment scripts
- **build-engineer** - Custom build tools
- **qa-expert** - CLI testing strategies

## Getting Started

1. Load the CLI Developer agent
2. Use `/cli-init` to create a new CLI project
3. Use `/cli-command` to add commands
4. Test across platforms
5. Use `/cli-publish` when ready to distribute

## Common Patterns

### Configuration Management
```javascript
// Load config from multiple sources
const config = {
  ...defaultConfig,
  ...loadFromFile('.myrc'),
  ...process.env,
  ...cliArgs
};
```

### Shell Completions
Generate completions for popular shells:
```bash
# Bash
my-cli completion bash > /etc/bash_completion.d/my-cli

# Zsh
my-cli completion zsh > /usr/local/share/zsh/site-functions/_my-cli

# Fish
my-cli completion fish > ~/.config/fish/completions/my-cli.fish
```

### Plugin System
```javascript
// Load plugins from directory
const plugins = loadPlugins('./plugins');
plugins.forEach(plugin => {
  program.command(plugin.command)
    .description(plugin.description)
    .action(plugin.action);
});
```

## Resources

### Documentation
- [Commander.js Guide](https://github.com/tj/commander.js)
- [oclif Documentation](https://oclif.io/)
- [Click Documentation](https://click.palletsprojects.com/)
- [Cobra Guide](https://github.com/spf13/cobra)

### Inspiration
- [GitHub CLI](https://cli.github.com/)
- [Vercel CLI](https://vercel.com/cli)
- [Stripe CLI](https://stripe.com/docs/stripe-cli)
- [AWS CLI](https://aws.amazon.com/cli/)

## Support

For issues, questions, or contributions, please refer to the main marketplace repository.

---

Built with expertise in CLI design, performance optimization, and developer experience.
