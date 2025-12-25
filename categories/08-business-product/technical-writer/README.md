# Technical Writer Agent

Expert technical writer specializing in clear, accurate documentation and content creation. Masters API documentation, user guides, and technical content with focus on making complex information accessible and actionable for diverse audiences.

## Overview

The Technical Writer agent is a senior-level documentation expert that helps create comprehensive, user-friendly documentation across various formats. From API references to user guides, this agent ensures clarity, accuracy, and user success through well-structured, accessible content.

## Features

### Documentation Types
- **API Documentation**: Endpoint descriptions, parameters, request/response examples, authentication guides
- **User Guides**: Getting started guides, feature documentation, task-based guides, troubleshooting
- **Developer Documentation**: SDK documentation, integration guides, code samples, best practices
- **Administrator Manuals**: Configuration guides, security documentation, deployment procedures

### Core Capabilities
- Technical writing and content creation
- Information architecture and content planning
- Style guide creation and enforcement
- Glossary management and terminology consistency
- Documentation review and quality assurance
- SEO optimization and accessibility compliance
- Visual communication (diagrams, screenshots, flowcharts)
- Documentation automation and workflow integration

### Quality Standards
- Readability score target: >60
- Technical accuracy: 100%
- User satisfaction target: >90%
- Comprehensive examples and visuals
- Version control and peer review
- SEO optimized content

## Slash Commands

### /doc-create
Create new documentation from scratch with proper structure, examples, and visuals.

**Usage:**
```
/doc-create [documentation type] [topic]
```

**Examples:**
```
/doc-create api-reference authentication
/doc-create user-guide getting-started
/doc-create tutorial deployment
```

**What it does:**
- Identifies the appropriate documentation type
- Determines target audience
- Creates structured outline
- Writes clear, comprehensive content
- Adds relevant examples and visuals
- Ensures accessibility and SEO optimization

### /doc-review
Review existing documentation for quality, accuracy, completeness, and provide actionable improvement suggestions.

**Usage:**
```
/doc-review [file or directory path]
```

**Examples:**
```
/doc-review docs/api/authentication.md
/doc-review docs/user-guide/
/doc-review README.md
```

**What it checks:**
- Technical accuracy verification
- Clarity and readability assessment
- Completeness and coverage
- Consistency validation
- Accessibility compliance
- SEO optimization
- Provides specific improvement recommendations

### /style-guide
Generate or apply style guide rules to ensure consistency in terminology, voice, tone, and formatting.

**Usage:**
```
/style-guide [action: create|apply|check] [scope]
```

**Examples:**
```
/style-guide create project
/style-guide check docs/
/style-guide apply docs/api/
```

**Actions:**
- **create**: Generate a new style guide template
- **check**: Validate documentation against style rules
- **apply**: Automatically apply style corrections

**What it covers:**
- Terminology consistency
- Voice and tone guidelines
- Formatting standards
- Style violations identification
- Correction suggestions

### /glossary
Manage project glossary and terminology to ensure consistent usage across all documentation.

**Usage:**
```
/glossary [action: create|update|check|export] [scope]
```

**Examples:**
```
/glossary create docs/api/
/glossary update project
/glossary check docs/
/glossary export markdown
```

**Actions:**
- **create**: Extract terms and build new glossary
- **update**: Add new terms to existing glossary
- **check**: Verify terminology consistency
- **export**: Generate glossary documentation in various formats

## MCP Servers

The Technical Writer agent uses the following MCP servers:

### filesystem
Access and manage documentation files in the project directory.

### github
- Access repositories for context
- Review pull requests
- Track documentation issues
- Collaborate on documentation updates

### memory
- Store documentation patterns
- Remember style preferences
- Maintain project-specific terminology
- Track documentation decisions

### fetch
- Retrieve external documentation
- Access API specifications
- Gather reference materials
- Research industry standards

## Use Cases

1. **API Documentation**: Create comprehensive API references with endpoints, parameters, examples, and error handling
2. **User Onboarding**: Write getting started guides that help new users succeed quickly
3. **Tutorial Creation**: Develop step-by-step tutorials for complex workflows
4. **Documentation Audit**: Review and improve existing documentation for clarity and completeness
5. **Style Standardization**: Establish and enforce documentation style across teams
6. **Terminology Management**: Maintain consistent terminology through project glossaries
7. **Feature Documentation**: Document new features as they're developed
8. **Troubleshooting Guides**: Create FAQs and troubleshooting documentation
9. **Release Documentation**: Write release notes and changelogs
10. **Technical Content**: Produce technical blog posts and articles

## Getting Started

### Prerequisites
- Node.js installed for MCP servers
- GitHub access token (for GitHub integration)
- Access to project documentation files

### Setup

1. **Configure MCP Servers**: The agent comes pre-configured with all necessary MCP servers in `mcp-config.json`

2. **Set Environment Variables**:
   ```bash
   export GITHUB_TOKEN=your_github_token_here
   ```

3. **Invoke the Agent**: Start using slash commands or interact directly with the agent for documentation tasks

### Quick Start Example

Create a new API documentation file:
```
/doc-create api-reference user-authentication
```

Review existing documentation:
```
/doc-review docs/api/
```

Generate a project glossary:
```
/glossary create docs/
```

## Workflow

### Planning Phase
1. Analyze documentation needs and audience
2. Audit existing content
3. Identify gaps and opportunities
4. Design information architecture
5. Plan content types and structure

### Implementation Phase
1. Research thoroughly
2. Write clear, concise content
3. Include practical examples
4. Add visual aids
5. Review for accuracy
6. Test usability
7. Gather feedback
8. Iterate based on input

### Excellence Phase
1. Verify technical accuracy
2. Test user experience
3. Incorporate feedback
4. Optimize for search
5. Plan maintenance schedule
6. Measure impact
7. Empower users

## Best Practices

### Writing Principles
- Use clear, concise language
- Write in active voice
- Focus on user tasks and goals
- Provide practical examples
- Use consistent terminology
- Break content into scannable sections
- Include visual aids where helpful

### API Documentation
- Document all endpoints completely
- Provide working code examples
- Explain authentication clearly
- Document error responses
- Include rate limiting information
- Show request/response examples
- Create quick start guides

### User Guides
- Start with getting started content
- Use task-based organization
- Provide step-by-step instructions
- Include troubleshooting sections
- Add screenshots and diagrams
- Create quick reference guides
- Document best practices

### Quality Assurance
- Verify technical accuracy with subject matter experts
- Test all code examples
- Check all links
- Validate accessibility
- Review readability scores
- Gather user feedback
- Monitor documentation analytics

## Integration with Other Agents

The Technical Writer agent collaborates effectively with:
- **product-manager**: Feature documentation and product updates
- **developers**: API documentation and code examples
- **ux-researcher**: User needs and pain points
- **support teams**: FAQ creation and troubleshooting guides
- **marketing**: Content creation and messaging
- **sales-engineer**: Technical materials and presentations
- **customer-success**: User guides and onboarding materials
- **legal-advisor**: Compliance and legal review

## Metrics and Success

Track documentation success through:
- **Readability Score**: Target >60 (Flesch Reading Ease)
- **User Satisfaction**: Target >90%
- **Support Ticket Reduction**: Measure decrease in documentation-related tickets
- **Documentation Coverage**: Percentage of features documented
- **Search Analytics**: Most searched terms and pages
- **User Feedback**: Ratings and comments
- **Adoption Metrics**: Documentation-driven feature adoption

## Continuous Improvement

The agent supports ongoing documentation excellence through:
- Regular content audits
- User feedback collection
- Analytics monitoring
- Broken link checking
- Accuracy verification
- Content refresh cycles
- Performance optimization
- New feature documentation

## Tips for Effective Use

1. **Be Specific**: Provide clear context about the documentation type and target audience
2. **Leverage Memory**: The agent remembers your style preferences and terminology
3. **Iterate**: Use the review command to continuously improve documentation
4. **Maintain Glossaries**: Keep terminology consistent across all documentation
5. **Use Style Guides**: Establish standards early and enforce them consistently
6. **Gather Feedback**: Regularly review user feedback and analytics
7. **Update Regularly**: Keep documentation current with product changes

## Support

For issues, questions, or contributions related to this agent, please refer to the main Claude Code Agent Marketplace repository.

## License

This agent is part of the Claude Code Agent Marketplace and follows the repository's licensing terms.
