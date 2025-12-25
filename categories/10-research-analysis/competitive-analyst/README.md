# Competitive Analyst Agent

A senior competitive analyst agent specializing in competitor intelligence, strategic analysis, and market positioning. This agent excels at competitive benchmarking, SWOT analysis, and delivering strategic recommendations that create sustainable competitive advantages.

## Overview

The Competitive Analyst agent provides comprehensive competitive intelligence services including competitor profiling, market positioning analysis, feature comparisons, and strategic recommendations. It combines systematic intelligence gathering with deep analytical capabilities to deliver actionable insights for competitive strategy.

## Features

- **Competitor Intelligence**: Comprehensive monitoring and profiling of direct, indirect, and emerging competitors
- **SWOT Analysis**: Thorough analysis of strengths, weaknesses, opportunities, and threats
- **Market Positioning**: Detailed positioning analysis with differentiation insights
- **Feature Comparison**: Side-by-side feature and capability benchmarking
- **Strategic Recommendations**: Actionable strategies for competitive advantage
- **Continuous Monitoring**: Ongoing competitor and market intelligence tracking
- **Multi-source Validation**: Cross-referenced data from multiple sources for accuracy
- **Ethical Intelligence**: Strict adherence to ethical intelligence gathering practices

## Installation

1. Ensure Node.js 18 or higher is installed
2. Clone this agent directory to your Claude Code workspace
3. The agent will automatically install required MCP servers on first use

## MCP Servers

This agent uses three MCP servers:

- **filesystem**: Access to local files for storing and retrieving competitive intelligence data
- **memory**: Persistent storage for competitor profiles and historical analysis
- **fetch**: Web content retrieval for gathering public competitive information

## Slash Commands

### `/competitor-scan`
Conduct comprehensive competitor scanning and profiling across the market landscape.

**Usage**: `/competitor-scan [market/industry]`

**Examples**:
```
/competitor-scan SaaS CRM market
/competitor-scan e-commerce platforms
/competitor-scan fintech startups
```

**What it does**:
- Identifies direct and indirect competitors
- Profiles potential market entrants
- Analyzes emerging threats
- Gathers intelligence across multiple dimensions
- Creates comprehensive competitor database

### `/swot-analysis`
Perform thorough SWOT analysis for specified competitors or market positions.

**Usage**: `/swot-analysis [competitor/company]`

**Examples**:
```
/swot-analysis Salesforce
/swot-analysis our current position
/swot-analysis top 3 competitors
```

**What it does**:
- Evaluates competitive strengths
- Identifies weaknesses and vulnerabilities
- Maps market opportunities
- Assesses competitive threats
- Provides strategic implications
- Delivers actionable recommendations

### `/market-position`
Analyze market positioning across competitors with differentiation analysis.

**Usage**: `/market-position [scope]`

**Examples**:
```
/market-position enterprise segment
/market-position vs top competitors
/market-position SMB market
```

**What it does**:
- Maps competitive positioning
- Analyzes differentiation strategies
- Creates value curves
- Studies market perception
- Evaluates brand strength
- Identifies positioning gaps

### `/feature-compare`
Execute detailed feature-by-feature comparison across competing products.

**Usage**: `/feature-compare [products/features]`

**Examples**:
```
/feature-compare our platform vs competitors
/feature-compare pricing models
/feature-compare integration capabilities
```

**What it does**:
- Compares product features and capabilities
- Assesses technology stacks
- Identifies functionality gaps
- Analyzes innovation rates
- Evaluates quality metrics
- Highlights differentiation opportunities

## Use Cases

### Strategic Planning
- Conduct quarterly competitive reviews
- Identify market opportunities and threats
- Develop competitive response strategies
- Guide product roadmap decisions

### Product Development
- Benchmark against competitor features
- Identify innovation opportunities
- Assess technology trends
- Prioritize development initiatives

### Marketing & Sales
- Develop competitive positioning
- Create battlecards and messaging
- Support competitive selling
- Guide differentiation strategies

### Executive Reporting
- Deliver executive competitive briefings
- Track market dynamics
- Monitor competitive threats
- Provide strategic recommendations

## Workflow

### 1. Intelligence Planning
The agent begins by understanding your competitive intelligence needs:
- Business objectives
- Key competitors
- Market position
- Strategic priorities
- Intelligence requirements

### 2. Data Collection
Systematic gathering of competitive intelligence:
- Public information research
- Financial data analysis
- Product and feature research
- Marketing and messaging monitoring
- Partnership and executive tracking
- Customer feedback analysis

### 3. Analysis & Benchmarking
Comprehensive competitive analysis:
- Multi-dimensional competitor profiling
- Objective performance benchmarking
- Pattern and trend identification
- Strategic assessment
- Opportunity mapping

### 4. Strategic Recommendations
Actionable insights and strategies:
- Competitive positioning recommendations
- Differentiation strategies
- Defense and attack strategies
- Innovation priorities
- Partnership opportunities

### 5. Continuous Monitoring
Ongoing intelligence updates:
- Change tracking and alerts
- Trend monitoring
- News aggregation
- Market intelligence updates

## Best Practices

### Ethical Intelligence
- Use only publicly available information
- Respect intellectual property
- Maintain objectivity
- Document sources clearly
- Follow legal guidelines

### Analysis Quality
- Validate data from multiple sources
- Maintain systematic approach
- Apply objective assessment
- Focus on strategic relevance
- Provide clear documentation

### Strategic Value
- Align with business objectives
- Deliver actionable insights
- Prioritize opportunities
- Consider implementation feasibility
- Track competitive impact

## Integration

### Agent Collaboration
Works seamlessly with other agents:
- **market-researcher**: Market dynamics and trends
- **product-manager**: Product strategy and roadmap
- **business-analyst**: Strategic planning and analysis
- **research-analyst**: Deep-dive investigations

### Tools
Leverages core tools:
- **Read/Grep/Glob**: Local file analysis
- **WebFetch**: Web content retrieval
- **WebSearch**: Market intelligence gathering

## Output Formats

The agent delivers intelligence in various formats:
- **Competitive Profiles**: Detailed competitor dossiers
- **SWOT Reports**: Comprehensive strength/weakness analysis
- **Positioning Maps**: Visual market positioning
- **Feature Matrices**: Side-by-side comparisons
- **Strategic Briefs**: Executive-level recommendations
- **Monitoring Alerts**: Ongoing intelligence updates

## Configuration

The agent operates with these default settings:
- **Analysis Depth**: Comprehensive
- **Update Frequency**: Continuous
- **Ethical Guidelines**: Strict
- **Data Validation**: Multi-source

## Example Session

```
User: /competitor-scan cloud storage market

Agent: Initiating comprehensive competitor scan of the cloud storage market...

[Analyzes market landscape]
- Identified 12 direct competitors
- Mapped 8 indirect competitors
- Profiled 5 emerging threats
- Collected 2.8K data points

Key Findings:
1. Market Leaders: Dropbox, Google Drive, OneDrive
2. Emerging Players: 3 high-growth startups
3. Market Trends: AI integration, security focus
4. Opportunity Gaps: Enterprise collaboration features

Would you like a detailed SWOT analysis of top competitors?

User: /swot-analysis Dropbox

Agent: Conducting SWOT analysis for Dropbox...

[Delivers comprehensive analysis with strategic implications and recommendations]
```

## Support

For issues or questions:
- Review agent documentation in CLAUDE.md
- Check MCP server configurations
- Verify Node.js and dependency versions
- Consult the Claude Code Agent Marketplace

## License

Part of the Claude Code Agent Marketplace. See repository root for license information.

## Version

Current version: 1.0.0

## Updates

This agent is maintained as part of the Claude Code Agent Marketplace. Check for updates regularly to access the latest competitive analysis capabilities and intelligence methodologies.
