# SEO Specialist Agent

Expert SEO strategist specializing in technical SEO, content optimization, and search engine rankings. Masters both on-page and off-page optimization, structured data implementation, and performance metrics to drive organic traffic and improve search visibility.

## Overview

The SEO Specialist agent is a senior-level SEO professional with deep expertise in:

- **Technical SEO**: Crawlability, indexation, site architecture, and performance optimization
- **Content Strategy**: Keyword research, on-page optimization, and content gap analysis
- **Structured Data**: Schema.org implementation and rich snippet optimization
- **Analytics**: Performance tracking, reporting, and data-driven decision making
- **Algorithm Compliance**: Staying current with search engine updates and best practices

## Prerequisites

### Required
- Node.js and npx installed
- Access to the website/codebase you want to optimize

### Optional
- `GITHUB_TOKEN`: For GitHub integration (managing SEO-related code changes)
- Access to SEO tools: Google Search Console, Google Analytics, Screaming Frog, etc.

## Installation

1. Copy the `seo-specialist` directory to your Claude Code agents location
2. Configure the MCP servers (see MCP Configuration below)
3. Load the agent using the CLAUDE.md instructions

## MCP Configuration

This agent uses four MCP servers for enhanced capabilities:

### 1. Filesystem
Access to read/write SEO configuration files, sitemaps, robots.txt, and schema markup.

```json
"filesystem": {
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "${PWD}"]
}
```

### 2. GitHub
Manage SEO-related code changes and create pull requests for technical implementations.

```json
"github": {
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-github"],
  "env": {
    "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_TOKEN}"
  }
}
```

**Setup**: Set the `GITHUB_TOKEN` environment variable with your personal access token.

### 3. Memory
Maintain context about SEO strategies, ranking data, and optimization history across sessions.

```json
"memory": {
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-memory"]
}
```

### 4. Fetch
Retrieve web content for analysis, competitor research, and validation.

```json
"fetch": {
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-fetch"]
}
```

## Slash Commands

The agent provides four specialized slash commands for common SEO tasks:

### `/seo-audit`
Perform a comprehensive technical SEO audit with actionable recommendations.

**Example:**
```
/seo-audit https://example.com
```

**Analyzes:**
- Crawl errors and indexation issues
- Site structure and internal linking
- Page speed and Core Web Vitals
- Mobile-friendliness
- Schema markup implementation
- Security and HTTPS
- Duplicate content
- Robots.txt and sitemap configuration

### `/keyword-analyze`
Conduct deep keyword research and opportunity analysis.

**Example:**
```
/keyword-analyze for "project management software"
```

**Provides:**
- Search volume and keyword difficulty
- Search intent classification
- Competitor keyword analysis
- Long-tail opportunities
- Content gap identification
- Seasonal trends
- Related keywords and topics

### `/schema-markup`
Generate and validate structured data markup for rich snippets.

**Example:**
```
/schema-markup for product pages
```

**Generates:**
- JSON-LD structured data
- Product, Article, or Organization schema
- FAQ and HowTo schemas
- Local business markup
- Breadcrumb navigation
- Validation and testing

### `/sitemap-gen`
Generate or optimize XML sitemaps for better crawling.

**Example:**
```
/sitemap-gen for the entire website
```

**Creates:**
- XML sitemap with proper structure
- Image sitemaps
- Video sitemaps
- News sitemaps
- Robots.txt optimization
- Sitemap index for large sites

## Usage Examples

### Example 1: Technical SEO Audit

```
Please perform a comprehensive technical SEO audit of our e-commerce site at https://shop.example.com
```

**What the agent does:**
1. Analyzes site structure and crawlability
2. Checks for technical issues (broken links, redirects, errors)
3. Evaluates Core Web Vitals performance
4. Reviews schema markup implementation
5. Provides prioritized recommendations with implementation steps

### Example 2: Keyword Strategy Development

```
Develop a keyword strategy for our SaaS product targeting enterprise project management
```

**What the agent does:**
1. Conducts comprehensive keyword research
2. Analyzes competitor keyword positioning
3. Maps search intent to content types
4. Identifies content gaps and opportunities
5. Creates a content optimization roadmap

### Example 3: Schema Implementation

```
Implement product schema markup for our online bookstore catalog
```

**What the agent does:**
1. Generates JSON-LD schema for products
2. Includes pricing, availability, reviews
3. Validates markup against Google's Rich Results Test
4. Provides implementation code
5. Documents testing and monitoring steps

### Example 4: Core Web Vitals Optimization

```
Our blog has poor Core Web Vitals scores. Please optimize for LCP, FID, and CLS.
```

**What the agent does:**
1. Analyzes current performance metrics
2. Identifies issues affecting each metric
3. Implements image optimization and lazy loading
4. Optimizes JavaScript and CSS delivery
5. Improves layout stability
6. Provides before/after comparisons

## Collaboration with Other Agents

The SEO Specialist works closely with other agents:

- **frontend-developer**: Implements technical SEO recommendations in code
- **content-marketer**: Collaborates on content strategy and optimization
- **wordpress-master**: Optimizes CMS-specific SEO settings
- **performance-engineer**: Works together on Core Web Vitals and speed optimization
- **ui-designer**: Ensures SEO-friendly design patterns
- **data-analyst**: Analyzes SEO metrics and performance data
- **business-analyst**: Evaluates ROI and business impact of SEO efforts

## Best Practices

### White-Hat SEO Only
The agent follows ethical SEO practices:
- Compliance with search engine guidelines
- User-first approach
- Natural link building
- Quality content standards
- No manipulative tactics

### Data-Driven Decisions
All recommendations are based on:
- Analytics data
- Search Console insights
- Competitive analysis
- Industry benchmarks
- Algorithm updates

### Measurable Results
Track and report on:
- Organic traffic growth
- Keyword ranking improvements
- Click-through rate increases
- Conversion rate optimization
- Core Web Vitals scores
- Backlink quality and quantity

## SEO Tools Integration

The agent leverages industry-standard tools:

- **Google Search Console**: Indexation and search performance
- **Google Analytics 4**: Traffic analysis and user behavior
- **Screaming Frog**: Technical SEO audits
- **SEMrush/Ahrefs**: Competitive analysis and backlink research
- **Moz Pro**: Domain authority and keyword tracking
- **PageSpeed Insights**: Performance metrics
- **Rich Results Test**: Schema validation
- **Mobile-Friendly Test**: Mobile optimization

## Deliverables

Expect comprehensive documentation:

1. **Technical SEO Audit Reports**: Prioritized recommendations with impact analysis
2. **Keyword Research Documents**: Search intent mapping and opportunity identification
3. **Content Optimization Guides**: On-page checklists and best practices
4. **Link Building Strategies**: Outreach templates and target identification
5. **Performance Dashboards**: KPI tracking and trend analysis
6. **Implementation Code**: Schema markup, sitemap XML, robots.txt
7. **Monthly Reports**: Progress tracking and strategic insights

## Troubleshooting

### Common Issues

**Issue: Low organic traffic**
- Run `/seo-audit` to identify technical issues
- Use `/keyword-analyze` to find better keyword opportunities
- Check Core Web Vitals and page speed

**Issue: Poor rich snippet performance**
- Use `/schema-markup` to implement or fix structured data
- Validate with Google's Rich Results Test
- Check for schema errors in Search Console

**Issue: Indexation problems**
- Review robots.txt and sitemap configuration
- Check for crawl errors in Search Console
- Use `/sitemap-gen` to optimize sitemaps

## Support and Contribution

- **Repository**: [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents)
- **Issues**: Report bugs or request features via GitHub Issues
- **License**: MIT

## Version History

- **2.0.0** (2025-12-24): Transformed to structured agent format with MCP servers and slash commands
- **1.0.0** (2024-01-01): Initial release

---

**Note**: This agent prioritizes sustainable, white-hat SEO strategies that improve user experience while achieving measurable search visibility and organic traffic growth. Always follow search engine guidelines and ethical practices.
