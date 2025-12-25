# Research Analyst Agent

Expert research analyst specializing in comprehensive information gathering, synthesis, and insight generation. Masters research methodologies, data analysis, and report creation with focus on delivering actionable intelligence that drives informed decision-making.

## Overview

The Research Analyst agent is designed to conduct thorough research across diverse domains, from market analysis to academic investigations. It excels at gathering information from multiple sources, evaluating credibility, synthesizing findings, and generating actionable insights that support strategic decision-making.

## Key Capabilities

### Research Methodology
- **Objective Definition**: Clear articulation of research goals and questions
- **Source Identification**: Locating relevant and credible information sources
- **Data Collection**: Systematic gathering of information from multiple channels
- **Quality Assessment**: Evaluating reliability and validity of sources
- **Information Synthesis**: Integrating findings into coherent narratives
- **Pattern Recognition**: Identifying trends and relationships in data
- **Insight Extraction**: Deriving meaningful conclusions from analysis
- **Report Generation**: Creating comprehensive, actionable deliverables

### Research Domains
- Market research and competitive intelligence
- Technology trends and innovation tracking
- Industry analysis and sector research
- Academic research and literature reviews
- Policy analysis and regulatory research
- Social trends and consumer behavior
- Economic indicators and forecasting

### Analysis Techniques
- Qualitative and quantitative methods
- Mixed methodology approaches
- Comparative and historical analysis
- Predictive modeling and scenario planning
- Risk assessment and opportunity identification

## Slash Commands

### `/research-plan`
Create a comprehensive research strategy.

**What it does:**
- Clarifies research objectives and scope
- Defines methodology and approach
- Identifies sources and resources
- Establishes timeline and milestones
- Sets quality standards and criteria
- Designs deliverable format

**Example use:**
```
/research-plan
Topic: AI adoption in healthcare
Scope: North American market, 2020-2025
Deliverable: Executive report with recommendations
```

### `/literature-review`
Conduct systematic review of existing sources.

**What it does:**
- Identifies relevant academic and industry sources
- Assesses quality and relevance of materials
- Extracts key findings and themes
- Identifies knowledge gaps
- Summarizes current state of research
- Creates annotated bibliography

**Example use:**
```
/literature-review
Topic: Machine learning in medical diagnostics
Focus: Peer-reviewed studies from 2020-2025
Output: Annotated bibliography with gap analysis
```

### `/synthesis-report`
Generate comprehensive research report.

**What it does:**
- Creates executive summary
- Presents detailed findings
- Includes data visualizations
- Documents methodology
- Provides source citations
- Delivers recommendations and action items

**Example use:**
```
/synthesis-report
Research: Customer satisfaction analysis
Format: Executive presentation with appendices
Audience: C-suite and product leadership
```

### `/methodology`
Document research approach and rationale.

**What it does:**
- Describes research design
- Documents data collection methods
- Explains analysis techniques
- Outlines quality controls
- Discusses limitations
- Addresses ethical considerations

**Example use:**
```
/methodology
Study: User behavior analysis
Methods: Mixed methods (surveys + interviews)
Purpose: Methodology section for research proposal
```

## MCP Servers

The agent uses three MCP servers to enhance its capabilities:

### Filesystem
- **Purpose**: Access and manage research files and documents
- **Use cases**: Reading source materials, saving reports, organizing research archives
- **Configuration**: Provides access to the current working directory

### Memory
- **Purpose**: Maintain research context and track findings across sessions
- **Use cases**: Storing interim findings, building knowledge base, tracking source citations
- **Configuration**: Persistent memory for research continuity

### Fetch
- **Purpose**: Retrieve web content and API data
- **Use cases**: Accessing online sources, fetching industry reports, gathering real-time data
- **Configuration**: Web content retrieval for comprehensive research

## Usage Guide

### Getting Started

1. **Define Your Research Objective**
   ```
   I need to research [topic] to understand [specific aspect].
   The goal is to [intended outcome].
   ```

2. **Use `/research-plan` to Create Strategy**
   - The agent will help define scope, methodology, and timeline
   - Clarify quality standards and deliverable format

3. **Conduct Research**
   - Agent gathers information from multiple sources
   - Evaluates credibility and relevance
   - Documents findings systematically

4. **Generate Deliverables**
   - Use `/literature-review` for source summaries
   - Use `/synthesis-report` for comprehensive findings
   - Use `/methodology` for research documentation

### Best Practices

**For Market Research:**
```
/research-plan
- Define target market and segments
- Identify key competitors and trends
- Set data collection methods (surveys, interviews, secondary research)
- Plan competitive analysis framework
```

**For Technology Trends:**
```
/literature-review
- Focus on recent publications (last 2-3 years)
- Include academic and industry sources
- Track patent filings and product launches
- Monitor thought leader perspectives
```

**For Competitive Intelligence:**
```
/synthesis-report
- Analyze competitor positioning and strategies
- Identify strengths, weaknesses, opportunities, threats
- Map competitive landscape
- Provide strategic recommendations
```

### Quality Assurance

The agent maintains high standards through:
- **Accuracy**: Thorough fact verification and cross-referencing
- **Credibility**: Rigorous source evaluation and validation
- **Comprehensiveness**: Multiple perspectives and triangulation
- **Clarity**: Clear synthesis and compelling narratives
- **Actionability**: Strategic insights and specific recommendations
- **Documentation**: Complete citations and methodology notes
- **Bias Control**: Critical awareness and balanced analysis

### Output Examples

**Research Plan Output:**
```
Research Objective: Analyze AI adoption in healthcare
Scope: North American market, 2020-2025
Methodology: Mixed methods (literature review + expert interviews)
Timeline: 4 weeks
Sources: Academic journals, industry reports, interviews (n=15)
Deliverables: 50-page report with executive summary
Quality Standards: Peer-reviewed sources, triangulated findings
```

**Synthesis Report Output:**
```
Executive Summary:
- Analyzed 234 sources yielding 12.4K data points
- Generated 47 actionable insights with 94% confidence
- Identified 3 major trends and 5 strategic opportunities

Key Findings:
1. [Trend 1]: Supporting evidence and implications
2. [Trend 2]: Market impact and recommendations
3. [Trend 3]: Strategic opportunities and risks

Recommendations:
- [Action 1]: Specific steps and expected outcomes
- [Action 2]: Implementation timeline and resources
```

## Collaboration

The Research Analyst works effectively with other agents:

- **Data Researcher**: Collaboration on data gathering and validation
- **Market Researcher**: Support for market-specific analysis
- **Competitive Analyst**: Partnership on competitor insights
- **Trend Analyst**: Coordination on pattern identification
- **Business Analyst**: Integration of strategic implications
- **Product Manager**: Research support for product decisions

## Advanced Features

### Multi-Source Integration
- Combines primary and secondary research
- Integrates qualitative and quantitative data
- Cross-references findings for validation

### Pattern Recognition
- Identifies emerging trends and anomalies
- Recognizes correlations and causations
- Spots opportunities and risks

### Knowledge Management
- Maintains research archives
- Tracks source databases
- Enables research reuse and updates

### Visualization Support
- Creates data visualizations
- Develops infographics
- Produces visual reports

## Tips for Success

1. **Be Specific**: Clearly define research objectives and scope
2. **Set Standards**: Establish quality criteria upfront
3. **Multiple Sources**: Use diverse, credible sources for triangulation
4. **Document Everything**: Maintain thorough citations and notes
5. **Stay Critical**: Question assumptions and identify biases
6. **Think Strategic**: Focus on actionable insights and recommendations
7. **Iterate**: Refine approach based on interim findings
8. **Communicate Clearly**: Present findings in accessible formats

## Limitations

- Research quality depends on source availability and credibility
- Time-sensitive topics may require frequent updates
- Some specialized domains may need subject matter expert validation
- Predictive analysis carries inherent uncertainty
- Access to proprietary databases may be limited

## Support

For questions or issues:
- Review agent capabilities in CLAUDE.md
- Check MCP server configurations in mcp-config.json
- Verify agent metadata in agent-manifest.json
- Consult example workflows above

---

**Version**: 1.0.0
**Last Updated**: 2025-12-24
**Category**: Research & Analysis
