# Content Marketer Agent

Expert content marketer specializing in content strategy, SEO optimization, and engagement-driven marketing. Masters multi-channel content creation, analytics, and conversion optimization with focus on building brand authority and driving measurable business results.

## Overview

The Content Marketer agent is designed to help teams create and execute comprehensive content marketing strategies that drive traffic, engagement, and conversions. It combines expertise in SEO, content creation, social media, email marketing, and analytics to deliver measurable ROI.

## Features

### Content Strategy
- Audience research and persona development
- Competitive content analysis
- Content pillar and topic cluster planning
- Editorial calendar creation and management
- Multi-channel distribution strategy
- Performance goal setting and tracking

### SEO Optimization
- Comprehensive keyword research
- On-page SEO optimization
- Meta tag optimization
- Internal linking strategy
- Schema markup implementation
- Featured snippet optimization

### Content Creation
- SEO-optimized blog posts
- Long-form content (white papers, ebooks)
- Case studies and testimonials
- Social media content
- Email marketing campaigns
- Video scripts and podcast outlines

### Analytics & Optimization
- Traffic and engagement analysis
- Conversion tracking and optimization
- A/B testing execution
- Performance reporting
- ROI calculation
- Continuous improvement cycles

## Installation

### Prerequisites
- Node.js >= 18.0.0
- npm >= 9.0.0
- GitHub personal access token (for GitHub MCP server)

### Setup

1. **Clone the agent configuration**
   ```bash
   cd ~/.config/claude-code/agents
   mkdir -p content-marketer
   cp /path/to/content-marketer/* content-marketer/
   ```

2. **Configure MCP servers**

   The agent uses four MCP servers. Ensure your environment variables are set:

   ```bash
   export GITHUB_TOKEN="your_github_personal_access_token"
   export PWD="$(pwd)"
   ```

3. **Install MCP dependencies**

   The MCP servers will be automatically installed when first invoked via npx. No manual installation required.

4. **Activate the agent**
   ```bash
   claude-code --agent content-marketer
   ```

## Usage

### Slash Commands

The Content Marketer agent provides four powerful slash commands:

#### `/content-plan`
Develop a comprehensive content strategy and editorial calendar.

```bash
/content-plan
```

**Outputs:**
- Target audience analysis and personas
- Competitive content landscape review
- Content pillars and topic clusters
- 90-day editorial calendar
- Distribution channel strategy
- Performance KPIs and success metrics
- Resource allocation plan

#### `/blog-draft`
Create an SEO-optimized blog post draft.

```bash
/blog-draft
```

**Outputs:**
- Keyword research and analysis
- SEO-optimized outline
- Complete blog post draft
- Meta title and description
- Internal linking suggestions
- Visual content recommendations
- CTA placement and copy

#### `/seo-optimize`
Optimize existing content for search engines and engagement.

```bash
/seo-optimize
```

**Outputs:**
- SEO audit and current performance
- Keyword opportunity analysis
- Optimized title tags and meta descriptions
- Improved content structure and headings
- Internal linking enhancements
- Schema markup recommendations
- Expected traffic impact estimation

#### `/content-audit`
Analyze content performance and identify optimization opportunities.

```bash
/content-audit
```

**Outputs:**
- Complete content inventory
- Traffic and engagement metrics analysis
- High and low performer identification
- SEO effectiveness assessment
- Content gap analysis
- Update and consolidation recommendations
- Prioritized action plan

### Example Workflows

#### Creating a New Blog Post

1. Research and plan:
   ```bash
   /content-plan
   ```

2. Create the draft:
   ```bash
   /blog-draft
   ```

3. Optimize for SEO:
   ```bash
   /seo-optimize
   ```

#### Improving Existing Content

1. Audit current performance:
   ```bash
   /content-audit
   ```

2. Optimize underperforming content:
   ```bash
   /seo-optimize
   ```

3. Update content strategy:
   ```bash
   /content-plan
   ```

## MCP Server Configuration

### Filesystem
Manages content assets, drafts, and documentation.

**Key directories:**
- `content-calendar.md` - Editorial planning
- `blog-drafts/` - Draft content
- `seo-research/` - Keyword and competitive research
- `campaign-briefs/` - Campaign documentation
- `analytics-reports/` - Performance data

### GitHub
Handles content workflow and version control.

**Operations:**
- Track content revisions
- Collaborate on drafts
- Review and approve content
- Automate publishing workflows
- Document campaign strategies

### Memory
Maintains marketing context and learnings.

**Stored information:**
- Brand voice guidelines
- Audience insights
- Successful content patterns
- Campaign performance history
- Competitive intelligence

### Fetch
Supports content research and competitive analysis.

**Operations:**
- Research trending topics
- Analyze competitor content
- Gather industry statistics
- Monitor brand mentions
- Research influencer partnerships

## Performance Targets

The Content Marketer agent aims to achieve:

- **SEO Score**: > 80/100
- **Engagement Rate**: > 5%
- **Conversion Rate**: > 2%
- **Content ROI**: > 300%
- **Traffic Growth**: > 50% YoY
- **Lead Quality Score**: > 70/100

## Integration with Other Agents

The Content Marketer works seamlessly with:

- **product-manager** - Product feature launches and updates
- **ux-researcher** - User insights and behavior analysis
- **seo-specialist** - Technical SEO optimization
- **social-media-manager** - Content distribution
- **pr-manager** - Thought leadership content
- **data-analyst** - Performance metrics and analytics
- **brand-manager** - Voice and messaging consistency
- **copywriter** - Content creation collaboration

## Best Practices

1. **Value First**: Always prioritize audience value over self-promotion
2. **Data-Driven**: Base decisions on analytics and performance data
3. **Consistency**: Maintain regular publishing schedule and brand voice
4. **Quality Over Quantity**: Better to publish less high-quality content
5. **SEO Integration**: Build SEO into content creation process
6. **Multi-Format**: Repurpose content across multiple formats
7. **Engagement Focus**: Create content that sparks conversation
8. **Continuous Learning**: Stay current with content marketing trends

## Troubleshooting

### MCP Server Connection Issues

If you encounter MCP server connection issues:

```bash
# Verify Node.js version
node --version  # Should be >= 18.0.0

# Clear npx cache
npx clear-npx-cache

# Verify environment variables
echo $GITHUB_TOKEN
echo $PWD
```

### GitHub Authentication

If GitHub MCP server fails to authenticate:

1. Verify your GitHub token has the required scopes:
   - `repo` (for repository access)
   - `read:org` (for organization data)

2. Update the token in your environment:
   ```bash
   export GITHUB_TOKEN="your_new_token"
   ```

### Performance Issues

If content generation is slow:

1. Check your internet connection (required for fetch operations)
2. Verify MCP servers are running: Check Claude Code logs
3. Consider breaking large tasks into smaller commands

## Support

For issues, questions, or contributions:

- GitHub Issues: [claude-code-agent-marketplace](https://github.com/anthropics/claude-code-agent-marketplace/issues)
- Documentation: [CLAUDE.md](./CLAUDE.md)
- MCP Configuration: [mcp-config.json](./mcp-config.json)

## License

MIT License - See repository root for details.

## Version History

### 1.0.0 (Current)
- Initial release
- Four core slash commands
- Four MCP server integrations
- Comprehensive content marketing capabilities
- SEO optimization features
- Analytics and performance tracking
