# Documentation Engineer Agent

Expert documentation engineer specializing in technical documentation systems, API documentation, and developer-friendly content. Masters documentation-as-code, automated generation, and creating maintainable documentation that developers actually use.

## Overview

The Documentation Engineer agent is designed to help teams build, maintain, and improve technical documentation systems. It excels at creating API documentation, developer guides, tutorials, and establishing documentation-as-code workflows that keep documentation synchronized with code changes.

## Key Features

### API Documentation
- **OpenAPI/Swagger Integration**: Generate comprehensive API docs from OpenAPI specifications
- **Multiple Format Support**: JSDoc, TSDoc, Sphinx, rustdoc, Javadoc, and more
- **Interactive Playgrounds**: Create interactive API explorers for testing endpoints
- **Code Examples**: Auto-generate request/response examples with proper error handling
- **Authentication Guides**: Document authentication flows and security requirements

### Documentation Architecture
- **Information Hierarchy**: Design intuitive documentation structure
- **Multi-Version Support**: Maintain documentation for multiple product versions
- **Search Optimization**: Implement full-text search with faceting and suggestions
- **Cross-Referencing**: Auto-link related documentation sections
- **Localization Framework**: Support multi-language documentation

### Content Creation
- **Tutorial Systems**: Create progressive learning paths with hands-on exercises
- **Quick Start Guides**: Build effective onboarding documentation
- **Reference Documentation**: Comprehensive API, CLI, and configuration references
- **Troubleshooting Guides**: Common issues and solutions
- **Migration Guides**: Version upgrade documentation

### Documentation Automation
- **Documentation-as-Code**: Keep docs in sync with code through automation
- **Link Validation**: Automatically check for broken links
- **Code Example Testing**: Validate that all code examples actually work
- **Screenshot Automation**: Auto-update screenshots when UI changes
- **SEO Optimization**: Implement best practices for search visibility

### Quality Assurance
- **Style Guide Enforcement**: Ensure consistency across documentation
- **Accessibility Testing**: WCAG AA compliance checking
- **Performance Monitoring**: Optimize page load times
- **Analytics Integration**: Track usage and identify improvement areas

## MCP Integration

This agent leverages several MCP servers for enhanced functionality:

### Filesystem Server (Required)
- Read and write documentation files
- Manage documentation structure and assets
- Process markdown, MDX, and other documentation formats

### GitHub Server (Recommended)
- Access repository documentation
- Review and manage documentation PRs
- Sync documentation with code changes
- Track documentation issues

### Context7 Server (Recommended)
- Semantic search across documentation
- Find related content automatically
- Identify outdated or duplicate content
- Suggest documentation improvements

### Fetch Server (Recommended)
- Retrieve external documentation
- Validate external links
- Import API schemas (OpenAPI, GraphQL)
- Check documentation references

## Slash Commands

### /docs-generate

Generate documentation from code using available documentation generators.

**Basic Usage:**
```
/docs-generate src/api --type api --format markdown
```

**Advanced Examples:**
```
# Generate component documentation with examples
/docs-generate components/ --type component --include-examples

# Generate CLI documentation with auto-linking
/docs-generate cli.ts --type cli --auto-link

# Use custom template
/docs-generate src/ --template custom-api-template --format html
```

**Options:**
- `--type`: Documentation type (api, component, cli)
- `--format`: Output format (markdown, html, pdf)
- `--template`: Custom documentation template
- `--include-examples`: Generate code examples
- `--auto-link`: Auto-link related documentation

### /docs-api

Create comprehensive API reference documentation from specifications or code.

**Basic Usage:**
```
/docs-api openapi.yaml --include-examples
```

**Advanced Examples:**
```
# Generate interactive API documentation
/docs-api openapi.yaml --include-examples --interactive

# Create TypeScript API docs with auth guide
/docs-api src/api/ --spec-format typescript --auth-guide

# GraphQL schema documentation
/docs-api schema.graphql --spec-format graphql --error-codes

# Python API docs with Sphinx
/docs-api src/ --spec-format python --include-examples
```

**Options:**
- `--spec-format`: Input format (openapi, graphql, jsdoc, typescript, python, rust)
- `--include-examples`: Generate request/response examples
- `--interactive`: Create interactive API playground
- `--auth-guide`: Include authentication documentation
- `--error-codes`: Document error codes and handling

### /docs-review

Review documentation quality and provide actionable improvement suggestions.

**Basic Usage:**
```
/docs-review docs/ --check-links --check-examples
```

**Advanced Examples:**
```
# Comprehensive quality review
/docs-review docs/ --check-links --check-examples --check-style --check-accessibility

# SEO and accessibility audit
/docs-review docs/api --check-accessibility --check-seo

# Quick style check with suggestions
/docs-review README.md --check-style --suggest-improvements
```

**Options:**
- `--check-links`: Validate all internal and external links
- `--check-examples`: Test all code examples
- `--check-style`: Verify style guide compliance
- `--check-accessibility`: Run WCAG AA accessibility checks
- `--check-seo`: Analyze SEO optimization
- `--suggest-improvements`: Provide detailed improvement suggestions

## Common Use Cases

### 1. Generate API Documentation

```
/docs-api openapi.yaml --include-examples --interactive --auth-guide
```

Creates comprehensive API documentation with:
- Interactive playground for testing endpoints
- Request/response examples
- Authentication and authorization guides
- Error code references

### 2. Set Up Documentation Site

Ask the agent to:
- Choose appropriate static site generator (Docusaurus, VitePress, etc.)
- Design information architecture
- Configure search functionality
- Set up version management
- Implement contribution workflow

### 3. Document TypeScript Project

```
/docs-generate src/ --spec-format typescript --include-examples --auto-link
```

Generates documentation from TypeScript code including:
- Type definitions
- Function signatures
- Code examples
- Cross-referenced links

### 4. Audit Existing Documentation

```
/docs-review docs/ --check-links --check-examples --check-accessibility --suggest-improvements
```

Comprehensive review that:
- Validates all links
- Tests code examples
- Checks accessibility compliance
- Provides improvement suggestions

### 5. Create Developer Onboarding

Ask the agent to create:
- Quick start guide
- Common use cases
- Troubleshooting guide
- FAQ section
- Video tutorials integration

## Best Practices

### Documentation-as-Code
- Keep documentation in version control alongside code
- Use automated generation where possible
- Test documentation in CI/CD pipeline
- Review documentation changes like code

### Content Organization
- Start with user needs and common tasks
- Structure for scanning (headings, lists, examples)
- Provide both tutorials and references
- Include visual aids (diagrams, screenshots)

### Code Examples
- Test all examples automatically
- Show complete, working examples
- Include error handling
- Specify dependency versions
- Provide expected output

### Maintenance
- Set up automated link checking
- Monitor search queries for gaps
- Track analytics to find popular content
- Regular content audits
- Update on code changes

### Accessibility
- Use semantic HTML
- Provide alt text for images
- Ensure keyboard navigation
- Maintain color contrast
- Test with screen readers

## Integration with Other Agents

The Documentation Engineer works seamlessly with:

- **Frontend Developer**: Document UI components and design systems
- **API Designer**: Generate API documentation from specifications
- **Backend Developer**: Create backend service documentation
- **Technical Writer**: Collaborate on content strategy and style
- **DevOps Engineer**: Document deployment and operations
- **Product Manager**: Align documentation with product roadmap
- **QA Expert**: Document testing procedures and requirements
- **CLI Developer**: Generate CLI documentation and usage guides

## Configuration

### Environment Variables

For GitHub integration:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN="your_token_here"
```

### MCP Setup

The agent automatically uses configured MCP servers. Ensure you have:
1. Node.js installed for MCP server execution
2. GitHub token configured (if using GitHub server)
3. Internet connection for fetch and context7 servers

## Supported Tools & Frameworks

### Static Site Generators
- Docusaurus
- VitePress
- Nextra
- MkDocs
- Hugo
- Jekyll
- Gatsby
- Astro

### API Documentation Tools
- Swagger UI
- Redoc
- Stoplight
- Postman
- Insomnia

### Documentation Formats
- Markdown
- MDX
- AsciiDoc
- reStructuredText
- HTML

### API Specification Formats
- OpenAPI 3.x
- Swagger 2.0
- GraphQL
- AsyncAPI
- RAML

## Examples

### Example 1: New API Documentation

```
User: I need to create documentation for our REST API. We have an OpenAPI 3.0 spec at api/openapi.yaml

Agent: /docs-api api/openapi.yaml --include-examples --interactive --auth-guide --error-codes

[Agent sets up comprehensive API documentation with interactive playground]
```

### Example 2: Documentation Site Setup

```
User: We need to set up a documentation site for our TypeScript library

Agent: I'll help you set up a modern documentation site. Let me:
1. Analyze your project structure
2. Generate API docs from your TypeScript code
3. Set up VitePress for the documentation site
4. Configure search and version management

/docs-generate src/ --spec-format typescript --include-examples

[Agent proceeds with full setup]
```

### Example 3: Documentation Audit

```
User: Our documentation needs improvement. Can you review it?

Agent: /docs-review docs/ --check-links --check-examples --check-style --check-accessibility --suggest-improvements

[Agent provides comprehensive review with actionable improvements]
```

## Output Examples

### Documentation Quality Report

```
Documentation Review Summary
============================

Coverage: 87% (123/141 modules documented)
Link Status: 94% valid (3 broken links found)
Code Examples: 89% passing (4 examples need updates)
Accessibility: WCAG AA compliant
SEO Score: 92/100
Performance: 1.3s average page load

Top Recommendations:
1. Fix broken links in API reference section
2. Update deprecated code examples in authentication guide
3. Add alt text to 7 images in tutorials
4. Improve mobile navigation experience
5. Add version switcher for multi-version support
```

## Troubleshooting

### Common Issues

**MCP servers not connecting:**
- Ensure Node.js is installed
- Check internet connection
- Verify MCP server paths in config

**Documentation generation fails:**
- Verify source code path is correct
- Check for supported documentation format
- Ensure code compiles successfully

**Link validation errors:**
- Check for correct relative paths
- Verify external URLs are accessible
- Review anchor links in headers

## Contributing

Contributions to improve the Documentation Engineer agent are welcome. Please:
1. Test your changes thoroughly
2. Update documentation
3. Follow existing code style
4. Submit pull request with clear description

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or contributions:
- GitHub Issues: [claude-code-agent-marketplace](https://github.com/anthropics/claude-code-agent-marketplace)
- Documentation: See CLAUDE.md for detailed agent instructions
