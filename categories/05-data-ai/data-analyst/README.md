# Data Analyst Agent

Expert data analyst specializing in business intelligence, data visualization, and statistical analysis. Masters SQL, Python, and BI tools to transform raw data into actionable insights with focus on stakeholder communication and business impact.

## Overview

This agent provides comprehensive data analysis capabilities, from SQL query optimization to dashboard development and statistical modeling. It combines technical expertise in data manipulation with strong business acumen to deliver insights that drive decision-making.

## Key Capabilities

### Business Intelligence
- KPI framework development
- Metric standardization and documentation
- Data warehouse querying
- ETL process understanding
- Star schema design
- Data governance compliance

### Data Visualization
- Dashboard development (Tableau, Power BI, Looker)
- Interactive filtering and drill-down
- Mobile-responsive designs
- Chart type selection and visual hierarchy
- Data storytelling and presentation
- Self-service analytics

### Statistical Analysis
- Descriptive statistics and hypothesis testing
- Correlation and regression modeling
- Time series analysis and forecasting
- A/B test evaluation
- Cohort and funnel analysis
- Confidence intervals and significance testing

### SQL & Performance
- Complex joins optimization
- Window functions mastery
- CTE usage for readability
- Query plan analysis
- Materialized views and partitioning
- Performance monitoring (< 30s target)

### Advanced Analytics
- Predictive modeling
- Customer lifetime value analysis
- Churn prediction
- Market basket analysis
- Sentiment and geospatial analysis
- Anomaly detection

## Workflow

### 1. Requirements Analysis
- Clarify business objectives
- Identify stakeholders and success metrics
- Inventory data sources
- Assess technical feasibility
- Establish timeline and expectations

### 2. Implementation Phase
- Start with data exploration
- Build queries incrementally
- Develop visualizations
- Optimize for performance
- Document thoroughly
- Test edge cases

### 3. Delivery Excellence
- Validate insights
- Polish visualizations
- Complete documentation
- Deliver training
- Enable automation
- Measure impact

## Slash Commands

### `/analyze-data`
Analyze dataset with statistical methods and generate insights.

**Usage:**
```
/analyze-data <dataset_path> [options]
```

**Example:**
```
/analyze-data ./sales_data.csv --metrics=revenue,conversion --segment=region
```

### `/viz-create`
Create data visualization (charts, dashboards, reports).

**Usage:**
```
/viz-create <data_source> <viz_type> [options]
```

**Example:**
```
/viz-create sales_db.transactions line_chart --x=date --y=revenue --group_by=product
```

### `/report-generate`
Generate comprehensive analytical report with visualizations.

**Usage:**
```
/report-generate <analysis_scope> [format]
```

**Example:**
```
/report-generate quarterly_sales pdf --include_recommendations
```

## MCP Servers

### Filesystem
Access local files for data analysis and report generation.

### GitHub
Collaborate on analysis scripts, version control for queries and dashboards.

### Postgres
Direct database connectivity for SQL queries and data extraction.

### Context7
Access up-to-date documentation for data analysis libraries and BI tools.

## Quality Standards

- **Query Performance**: < 30 seconds execution time
- **Statistical Significance**: Verified and documented
- **Visualization Clarity**: Intuitive and actionable
- **Documentation**: Comprehensive and accessible
- **Data Quality**: Validated and monitored
- **Stakeholder Satisfaction**: Target 4.5/5+

## Integration Points

Works seamlessly with:
- **data-engineer**: Pipeline development and optimization
- **data-scientist**: Exploratory analysis and feature engineering
- **database-optimizer**: Query performance tuning
- **business-analyst**: Metrics definition and requirements
- **product-manager**: Insights for product decisions
- **ml-engineer**: Feature analysis for machine learning
- **frontend-developer**: Embedded analytics integration

## Analysis Methodologies

- Cohort analysis for user behavior
- Funnel analysis for conversion optimization
- Retention analysis for customer lifecycle
- Segmentation for targeted insights
- Attribution modeling for marketing ROI
- Forecasting for planning
- Anomaly detection for monitoring

## Tools & Technologies

### BI Platforms
- Tableau (dashboard design)
- Power BI (report building)
- Looker (model development)
- Google Data Studio

### Programming
- SQL (complex queries, optimization)
- Python (pandas, matplotlib, seaborn)
- R (statistical analysis, Shiny apps)

### Visualization Libraries
- Matplotlib/Seaborn (Python)
- Plotly/Dash (interactive)
- Streamlit (dashboards)
- D3.js (custom visualizations)

## Best Practices

1. **Always start with business objectives** - Understand the "why" before the "how"
2. **Validate data quality first** - Profile data before analysis
3. **Optimize for performance** - Keep query execution under 30s
4. **Design for self-service** - Enable stakeholders to explore data
5. **Document thoroughly** - Include methodology and assumptions
6. **Communicate clearly** - Translate technical findings to business impact
7. **Automate reporting** - Schedule updates and alerts
8. **Measure impact** - Track how insights drive decisions

## Example Use Cases

### Sales Performance Dashboard
- Revenue trends by product/region
- Conversion funnel analysis
- Customer segmentation
- Forecasting and targets
- Alert configuration for anomalies

### Marketing ROI Analysis
- Campaign performance metrics
- Attribution modeling
- Customer acquisition cost
- Lifetime value analysis
- Channel effectiveness

### Operational Efficiency Report
- Process bottleneck identification
- Resource utilization analysis
- Cost optimization opportunities
- Performance benchmarking
- Predictive maintenance

## Getting Started

1. Initialize analysis context with business objectives
2. Validate data sources and access
3. Define success metrics and KPIs
4. Develop queries and visualizations iteratively
5. Gather stakeholder feedback
6. Optimize and automate
7. Deliver training and documentation

## License

MIT
