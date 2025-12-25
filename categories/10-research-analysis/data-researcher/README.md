# Data Researcher Agent

Expert data researcher specializing in discovering, collecting, and analyzing diverse data sources. Masters data mining, statistical analysis, and pattern recognition with focus on extracting meaningful insights from complex datasets to support evidence-based decisions.

## Overview

The Data Researcher agent is designed to handle comprehensive data research workflows, from initial data discovery through advanced statistical analysis to actionable insight generation. It combines systematic data collection with rigorous analytical methods to uncover meaningful patterns and deliver evidence-based recommendations.

## Key Capabilities

- **Data Discovery**: Identify and catalog diverse data sources including APIs, databases, public datasets, and web sources
- **Source Validation**: Assess data quality, reliability, completeness, and accessibility
- **Data Extraction**: Automated collection via API integration, web scraping, and database queries
- **Quality Assurance**: Comprehensive validation including completeness, accuracy, consistency checks
- **Statistical Analysis**: Descriptive statistics, inferential testing, correlation, regression, and time series analysis
- **Pattern Recognition**: Trend identification, anomaly detection, seasonality analysis, and relationship mapping
- **Data Visualization**: Interactive dashboards, charts, geographic mapping, and story-driven displays
- **Insight Generation**: Transform data into actionable findings, predictions, and strategic recommendations

## Slash Commands

### `/data-discover`
Discover and catalog available data sources relevant to research questions.

**Usage:**
```
/data-discover [research topic or question]
```

**What it does:**
- Identifies relevant APIs, databases, and public datasets
- Catalogs web sources and real-time data streams
- Assesses data availability and accessibility
- Documents source metadata and quality indicators
- Provides recommendations for optimal data sources

**Example:**
```
/data-discover customer behavior patterns in e-commerce
```

### `/source-validate`
Validate data source quality, reliability, and accessibility.

**Usage:**
```
/source-validate [source name or URL]
```

**What it does:**
- Checks data completeness and coverage
- Validates accuracy and reliability
- Verifies consistency across datasets
- Assesses timeliness and update frequency
- Evaluates relevance to research questions
- Detects duplicates and outliers

**Example:**
```
/source-validate https://api.example.com/sales-data
```

### `/data-extract`
Extract and collect data from validated sources.

**Usage:**
```
/data-extract [source identifier] [parameters]
```

**What it does:**
- Implements automated data gathering pipelines
- Executes API integration with proper authentication
- Performs web scraping with rate limiting
- Runs database queries with optimization
- Applies data validation and quality checks
- Handles error recovery and logging

**Example:**
```
/data-extract sales-api dateRange=2024-01-01:2024-12-31
```

### `/insight-report`
Generate comprehensive insight reports from analyzed data.

**Usage:**
```
/insight-report [dataset or analysis context]
```

**What it does:**
- Synthesizes key findings and patterns
- Performs trend and predictive analysis
- Identifies causal relationships and risk factors
- Creates visualizations and dashboards
- Generates actionable recommendations
- Documents methodology and confidence levels

**Example:**
```
/insight-report quarterly-sales-analysis
```

## MCP Servers

### Filesystem
Provides access to local file system for reading and writing data files, analysis results, and reports.

**Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "${PWD}"]
}
```

### Memory
Enables persistent storage of research findings, data catalogs, and analytical insights across sessions.

**Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-memory"]
}
```

### Fetch
Enables web data fetching, API interactions, and web scraping capabilities for data collection.

**Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-fetch"]
}
```

## Workflows

### 1. Data Planning Workflow

Design comprehensive data research strategy before collection begins.

**Steps:**
1. **Question Formulation**: Define clear research questions and hypotheses
2. **Data Inventory**: Catalog available internal and external sources
3. **Source Assessment**: Evaluate quality, accessibility, and relevance
4. **Collection Planning**: Design automated pipelines and schedules
5. **Analysis Design**: Plan statistical methods and visualization approaches

**Output**: Research plan document with timelines, resources, and quality standards

### 2. Data Collection Workflow

Conduct thorough data research and analysis with quality controls.

**Steps:**
1. **Collect Data**: Execute automated gathering from validated sources
2. **Validate Quality**: Run completeness, accuracy, and consistency checks
3. **Process Datasets**: Clean, transform, normalize, and integrate data
4. **Analyze Patterns**: Apply statistical methods and pattern recognition
5. **Generate Insights**: Synthesize findings into actionable recommendations

**Output**: Processed datasets, analysis results, and preliminary insights

### 3. Data Excellence Workflow

Deliver exceptional data-driven insights with confidence.

**Steps:**
1. **Quality Assurance**: Comprehensive validation and peer review
2. **Pattern Validation**: Confirm statistical significance and reproducibility
3. **Visualization Creation**: Develop interactive dashboards and charts
4. **Documentation Completion**: Detail methodology, sources, and limitations
5. **Impact Demonstration**: Show business value and actionable outcomes

**Output**: Final reports, dashboards, and presentation materials

## Integration Examples

### Working with Research Analyst
```javascript
// Data Researcher discovers and validates sources
/data-discover market trends in renewable energy

// Research Analyst uses findings for strategic analysis
// Collaboration on interpreting patterns and implications
```

### Supporting Data Scientist
```javascript
// Data Researcher extracts and prepares datasets
/data-extract energy-consumption-api region=north-america

// Data Scientist builds advanced ML models on prepared data
// Partnership on feature engineering and model validation
```

### Coordinating with Business Analyst
```javascript
// Data Researcher generates insights
/insight-report customer-churn-analysis

// Business Analyst translates to business recommendations
// Joint presentation to decision-makers
```

## Best Practices

### Data Quality
- Always verify completeness before analysis
- Document data lineage and transformations
- Maintain version control for datasets
- Implement automated quality checks
- Handle missing data systematically

### Statistical Rigor
- Use hypothesis-driven approaches
- Apply multiple analytical methods
- Perform sensitivity analysis
- Cross-validate findings
- Document confidence levels

### Reproducibility
- Document all data sources and access methods
- Version control analysis scripts
- Record parameters and configurations
- Enable peer review processes
- Provide replication instructions

### Visualization Excellence
- Choose appropriate chart types for data
- Ensure accessibility and color-blind friendly
- Create interactive elements for exploration
- Optimize for mobile and desktop
- Tell compelling data stories

## Common Use Cases

### Market Research
```
/data-discover consumer sentiment on product X
/source-validate social-media-analytics-api
/data-extract twitter-api keywords=productX
/insight-report brand-perception-analysis
```

### Business Intelligence
```
/data-discover sales performance metrics
/data-extract crm-database dateRange=Q4-2024
/insight-report revenue-trends-forecast
```

### Scientific Research
```
/data-discover climate change datasets
/source-validate noaa-weather-api
/data-extract weather-stations region=pacific
/insight-report temperature-trend-analysis
```

### Competitive Analysis
```
/data-discover competitor pricing strategies
/data-extract market-intelligence-sources
/insight-report competitive-positioning
```

## Tips for Effective Use

1. **Start with Clear Questions**: Define specific research questions before data discovery
2. **Validate Early**: Check data quality before investing in large-scale collection
3. **Automate Pipelines**: Build reusable data collection and processing workflows
4. **Document Everything**: Maintain comprehensive records of sources, methods, and decisions
5. **Iterate Analysis**: Use exploratory analysis to refine hypotheses and methods
6. **Visualize Continuously**: Create visualizations throughout analysis, not just at the end
7. **Seek Peer Review**: Have findings reviewed by domain experts and statisticians
8. **Focus on Action**: Ensure insights lead to concrete, implementable recommendations

## Troubleshooting

### Data Quality Issues
- Run `/source-validate` to identify specific quality problems
- Check for missing data patterns and systematic biases
- Verify data freshness and update frequency
- Cross-reference with alternative sources

### API Access Problems
- Verify authentication credentials and permissions
- Check API rate limits and quotas
- Review error logs for specific failure messages
- Implement retry logic with exponential backoff

### Analysis Challenges
- Ensure sufficient sample size for statistical power
- Check for confounding variables and biases
- Apply appropriate transformations for non-normal data
- Consider alternative analytical methods

### Performance Optimization
- Sample large datasets for exploratory analysis
- Use incremental processing for streaming data
- Implement caching for frequently accessed data
- Optimize database queries with proper indexing

## Related Agents

- **research-analyst**: Strategic research and analysis
- **data-scientist**: Advanced machine learning and modeling
- **business-analyst**: Business implications and recommendations
- **data-engineer**: Data pipeline and infrastructure
- **visualization-specialist**: Advanced dashboard creation
- **statistician**: Statistical methodology and validation

## Additional Resources

- [Data Quality Framework](https://example.com/data-quality)
- [Statistical Analysis Guide](https://example.com/statistics)
- [Visualization Best Practices](https://example.com/viz-guide)
- [Research Methodology](https://example.com/research-methods)

## Support

For questions or issues with the Data Researcher agent:
- Review the troubleshooting section above
- Check agent logs for detailed error messages
- Consult related agents for collaborative workflows
- Refer to MCP server documentation for integration issues
