# Market Researcher Agent

Expert market researcher specializing in market analysis, consumer insights, and competitive intelligence. Masters market sizing, segmentation, and trend analysis with focus on identifying opportunities and informing strategic business decisions.

## Overview

The Market Researcher agent is a senior-level market research expert designed to provide comprehensive market intelligence that drives strategic business decisions. This agent excels at analyzing market dynamics, understanding consumer behavior, mapping competitive landscapes, and identifying emerging trends to uncover growth opportunities.

## Capabilities

- **Market Sizing**: Calculate TAM, SAM, and SOM using multiple methodologies
- **Market Segmentation**: Identify and analyze target customer segments
- **Consumer Research**: Deep analysis of consumer behavior and preferences
- **Competitive Intelligence**: Comprehensive competitor analysis and positioning
- **Trend Analysis**: Identify and validate emerging market trends
- **Opportunity Assessment**: Discover market gaps and growth opportunities
- **Strategic Recommendations**: Evidence-based strategic insights
- **Report Creation**: Professional research reports and presentations

## Installation

1. Navigate to the market-researcher directory:
```bash
cd categories/10-research-analysis/market-researcher
```

2. Ensure you have Node.js installed for MCP servers

3. The agent will automatically set up the required MCP servers on first run:
   - `filesystem`: For managing research files and reports
   - `memory`: For storing research insights and historical data
   - `fetch`: For retrieving market data from external sources

## Usage

### Basic Invocation

Invoke the Market Researcher agent for any market research needs:

```
I need to understand the market for [product/service] in [geography]
```

The agent will:
1. Query for market research objectives and scope
2. Review industry data, consumer trends, and competitive intelligence
3. Analyze market opportunities, threats, and strategic implications
4. Deliver comprehensive market insights with strategic recommendations

### Slash Commands

#### /market-size

Calculate total addressable market (TAM), serviceable available market (SAM), and serviceable obtainable market (SOM).

```bash
/market-size cloud storage enterprise North America
/market-size electric vehicles consumer global
```

**Output**:
- TAM/SAM/SOM breakdown with supporting data
- Market growth projections (3-5 years)
- Key assumptions and methodology
- Market sizing confidence intervals
- Strategic implications

#### /segment-analyze

Perform detailed market segmentation analysis to identify and prioritize target customer segments.

```bash
/segment-analyze SaaS productivity tools
/segment-analyze sustainable fashion
```

**Output**:
- Segment profiles with detailed characteristics
- Segment sizing and revenue potential
- Attractiveness scoring matrix
- Recommended target segments
- Positioning recommendations per segment

#### /trend-report

Generate comprehensive trend analysis covering emerging market, technology, and consumer trends.

```bash
/trend-report fintech 2024-2026
/trend-report healthcare technology next 3 years
```

**Output**:
- Categorized trend inventory
- Trend strength assessment (weak signals to megatrends)
- Impact analysis on industry/market
- Timeline and adoption projections
- Strategic recommendations
- Monitoring dashboard setup

#### /tam-sam-som

Detailed TAM/SAM/SOM calculation with multiple methodologies and validation.

```bash
/tam-sam-som AI chatbot platform global all
/tam-sam-som cybersecurity SMB EMEA bottom-up
```

**Methods**:
- `top-down`: Industry reports, analyst estimates, macroeconomic data
- `bottom-up`: Customer counts, pricing, purchase frequency
- `value-theory`: Customer value creation, willingness to pay
- `all`: Run all methods and triangulate

**Output**:
- Multi-method market size calculations
- Reconciliation of different approaches
- Confidence intervals and sensitivity analysis
- Market growth scenarios (conservative, base, optimistic)
- Geographic/segment breakdowns
- Key assumptions documentation

## Research Workflow

### 1. Research Planning

The agent designs a comprehensive research approach:
- Define research objectives
- Determine scope and boundaries
- Select appropriate methodologies
- Map data sources
- Plan timeline and allocate resources
- Set quality standards

### 2. Implementation Phase

Systematic market research execution:
- Collect data from multiple sources
- Analyze market dynamics and sizing
- Study consumer behavior patterns
- Assess competitive landscape
- Identify and validate trends
- Generate actionable insights
- Create comprehensive reports

### 3. Delivery

Deliver exceptional market intelligence:
- Comprehensive research reports
- Executive summaries
- Visual presentations
- Strategic recommendations
- Implementation roadmaps
- ROI projections

## Research Methodologies

### Primary Research
- Survey design and deployment
- Interview protocols
- Focus groups
- Observation studies
- Field studies

### Secondary Research
- Industry reports analysis
- Market databases
- Academic research
- News and media monitoring
- Social listening

### Analysis Techniques
- Quantitative analysis
- Qualitative synthesis
- Statistical modeling
- Pattern recognition
- Trend forecasting

## Deliverables

Standard research deliverables include:

- **Market Size Reports**: TAM/SAM/SOM calculations with growth projections
- **Segmentation Analysis**: Detailed segment profiles and prioritization
- **Consumer Insight Reports**: Behavior analysis, needs, and preferences
- **Competitive Assessments**: Competitor mapping, SWOT, positioning
- **Trend Reports**: Emerging trends with impact analysis
- **Opportunity Assessments**: Market gaps and growth potential
- **Strategic Recommendations**: Evidence-based action plans
- **Executive Summaries**: High-level insights for decision-makers
- **Visual Presentations**: Charts, graphs, and infographics
- **Methodology Documentation**: Research approach and data sources

## Integration with Other Agents

The Market Researcher collaborates with:

- **competitive-analyst**: Deep dive competitor research and analysis
- **product-manager**: Product-market fit assessment and validation
- **business-analyst**: Strategic implications and business planning
- **data-researcher**: Advanced data analysis and modeling
- **trend-analyst**: Future market direction and forecasting
- **Sales teams**: Market opportunity identification
- **Marketing teams**: Positioning and messaging insights
- **Executives**: Strategic market direction

## Quality Standards

The agent maintains high research quality through:

- **Accuracy**: Multi-source validation and fact-checking
- **Comprehensiveness**: Thorough coverage of all relevant aspects
- **Reliability**: Authoritative sources and proven methodologies
- **Actionability**: Clear insights that inform decisions
- **Timeliness**: Current data and relevant timeframes
- **Statistical Validity**: Appropriate sample sizes and confidence levels
- **Strategic Relevance**: Alignment with business objectives

## Example Use Cases

### 1. New Market Entry
```
I'm considering entering the smart home security market in Europe.
What's the market opportunity?
```

The agent will:
- Size the European smart home security market (TAM/SAM/SOM)
- Analyze market segments (residential, commercial, demographics)
- Map competitive landscape and market share
- Identify consumer trends and preferences
- Assess regulatory environment
- Provide entry strategy recommendations

### 2. Product Launch Planning
```
/segment-analyze wearable health tech
```

The agent will:
- Define customer segments (fitness enthusiasts, medical users, general wellness)
- Size each segment and revenue potential
- Analyze segment characteristics and needs
- Score segment attractiveness
- Recommend target segments and positioning

### 3. Strategic Planning
```
/trend-report artificial intelligence enterprise 2024-2027
```

The agent will:
- Scan AI trends across categories
- Validate trends through multiple sources
- Assess adoption curves and timeline
- Analyze business implications
- Provide strategic recommendations
- Set up monitoring systems

## Best Practices

1. **Clear Objectives**: Define specific research questions and goals
2. **Scope Definition**: Set clear boundaries for market and geography
3. **Multiple Sources**: Validate findings across different data sources
4. **Context Awareness**: Consider industry dynamics and constraints
5. **Stakeholder Input**: Incorporate internal knowledge and perspectives
6. **Iterative Refinement**: Update research as new data emerges
7. **Action Orientation**: Focus on insights that drive decisions
8. **Documentation**: Maintain clear methodology and assumption records

## Configuration

The agent uses three MCP servers configured in `mcp-config.json`:

- **filesystem**: Manages research files, reports, and documentation
- **memory**: Stores research insights, findings, and historical context
- **fetch**: Retrieves data from external market data sources and APIs

## Support and Feedback

For issues, enhancements, or questions about the Market Researcher agent:
- Review the agent manifest for detailed capabilities
- Check the CLAUDE.md file for complete instructions
- Consult integration guidelines for multi-agent workflows

## Version

Current version: 1.0.0

## License

Part of the Claude Code Agent Marketplace
