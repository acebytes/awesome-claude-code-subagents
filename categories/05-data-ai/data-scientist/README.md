# Data Scientist Agent

Expert data scientist specializing in statistical analysis, machine learning, and business insights. Masters exploratory data analysis, predictive modeling, and data storytelling with focus on delivering actionable insights that drive business value.

## Overview

The Data Scientist agent helps you uncover insights from data through rigorous statistical analysis, build accurate predictive models, and communicate findings effectively to drive business decisions. From exploratory analysis to production-ready models, this agent brings comprehensive expertise in modern data science practices.

### Key Capabilities

- **Statistical Analysis**: Hypothesis testing, regression, ANOVA, time series, causal inference with p<0.05 rigor
- **Machine Learning**: Build models achieving 87%+ accuracy using scikit-learn, XGBoost, neural networks
- **Predictive Modeling**: Classification, regression, clustering, time series forecasting with cross-validation
- **Exploratory Data Analysis**: Comprehensive data profiling, distribution analysis, correlation studies, outlier detection
- **Feature Engineering**: Domain-driven feature creation, encoding, scaling, dimensionality reduction
- **A/B Testing**: Experimental design, sample size calculation, statistical testing, impact measurement
- **Model Interpretation**: SHAP values, feature importance, partial dependence plots, bias detection
- **Business Communication**: Executive summaries, data storytelling, ROI quantification, actionable recommendations

## Quick Start

### Installation

1. Clone this repository
2. Navigate to the data-scientist directory
3. Configure MCP servers in `mcp-config.json`
4. Start using the agent via Claude Desktop or CLI

### Basic Usage

```bash
# Exploratory data analysis
/ds-explore ./data/customer_churn.csv --target churn --report

# Build predictive model
/ds-model ./data/sales.csv revenue regression

# Generate business insights
/ds-insight ./results/churn_analysis --retention
```

## Technology Stack

### Statistical Methods
- **Hypothesis Testing**: t-tests, chi-square, ANOVA, Mann-Whitney
- **Regression Analysis**: Linear, Ridge, Lasso, ElasticNet, polynomial
- **Time Series**: ARIMA, Prophet, seasonal decomposition, trend analysis
- **Survival Analysis**: Kaplan-Meier, Cox proportional hazards
- **Bayesian Methods**: Prior specification, MCMC, posterior inference
- **Causal Inference**: RCTs, propensity scoring, DiD, instrumental variables

### Machine Learning Algorithms
- **Linear Models**: Linear/Logistic Regression, Ridge, Lasso
- **Tree-Based**: Random Forest, Gradient Boosting, XGBoost, LightGBM
- **Neural Networks**: Feedforward, CNN, RNN, LSTM, Transformers
- **Ensemble Methods**: Bagging, boosting, stacking
- **Clustering**: K-Means, DBSCAN, hierarchical, Gaussian mixtures
- **Dimensionality Reduction**: PCA, t-SNE, UMAP

### Python Data Science Stack
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **SciPy**: Statistical functions
- **Scikit-learn**: Machine learning algorithms
- **StatsModels**: Statistical models and hypothesis testing
- **XGBoost/LightGBM**: Gradient boosting frameworks
- **TensorFlow/PyTorch**: Deep learning
- **Prophet**: Time series forecasting

### Visualization Tools
- **Matplotlib**: Publication-quality plots
- **Seaborn**: Statistical visualizations
- **Plotly**: Interactive graphics
- **Altair**: Declarative visualization
- **Bokeh**: Interactive web-ready plots

## Slash Commands

### /ds-explore

Conduct comprehensive exploratory data analysis.

**Syntax**: `/ds-explore <dataset_path> [options]`

**Options**:
- `--target <column>`: Specify target variable for supervised learning context
- `--categorical`: Focus on categorical variable analysis
- `--timeseries`: Perform time series decomposition
- `--report`: Generate comprehensive EDA report

**What it does**:
1. Loads and profiles dataset (shape, types, missing values)
2. Analyzes distributions for each variable
3. Detects outliers and anomalies using statistical methods
4. Computes correlation matrix and identifies relationships
5. Identifies missing data patterns and mechanisms
6. Generates comprehensive statistical summaries
7. Creates visualizations (histograms, scatter plots, box plots, heatmaps)
8. Formulates hypotheses for further testing
9. Documents insights and recommendations

**Examples**:
```bash
# Basic exploratory analysis
/ds-explore ./data/customer_data.csv

# Focus on target variable for predictive modeling
/ds-explore ./data/customer_churn.csv --target churn --report

# Time series analysis
/ds-explore ./data/daily_sales.csv --timeseries --report

# Categorical analysis
/ds-explore ./data/survey_responses.csv --categorical
```

### /ds-model

Build and validate predictive models.

**Syntax**: `/ds-model <dataset_path> <target> [model_type]`

**Model Types**:
- `regression`: Linear, Ridge, Lasso, ElasticNet, Random Forest, XGBoost for continuous targets
- `classification`: Logistic Regression, Random Forest, XGBoost, Neural Networks for categorical targets
- `timeseries`: ARIMA, Prophet, LSTM for temporal forecasting
- `clustering`: K-Means, DBSCAN, Hierarchical for unsupervised grouping
- `auto`: Automatically select best model type based on data

**What it does**:
1. Loads data and performs train/validation/test split (60/20/20)
2. Engineers features based on domain knowledge and EDA insights
3. Handles missing values and outliers appropriately
4. Encodes categorical variables (one-hot, target encoding)
5. Scales/normalizes features as needed
6. Trains multiple model types for comparison
7. Performs hyperparameter optimization (grid search, Bayesian optimization)
8. Cross-validates with k-fold (k=5 or 10) for robust estimates
9. Evaluates on test set with multiple metrics
10. Analyzes feature importance and model interpretation
11. Checks for bias and fairness across subgroups
12. Generates model interpretation plots (SHAP, partial dependence)
13. Documents complete methodology and reproducible code

**Examples**:
```bash
# Regression model for sales prediction
/ds-model ./data/sales.csv revenue regression

# Classification for churn prediction
/ds-model ./data/customers.csv churn classification

# Time series forecasting
/ds-model ./data/daily_orders.csv order_count timeseries

# Auto-select best model type
/ds-model ./data/dataset.csv target_variable auto
```

### /ds-insight

Generate actionable insights and business recommendations.

**Syntax**: `/ds-insight <analysis_path> [business_context]`

**Business Context Options**:
- `--revenue`: Focus on revenue impact and optimization
- `--cost`: Emphasize cost reduction opportunities
- `--retention`: Customer retention and churn insights
- `--growth`: Growth opportunity analysis
- `--risk`: Risk assessment and mitigation strategies

**What it does**:
1. Reviews completed analysis and model results
2. Identifies key drivers and patterns with statistical significance
3. Quantifies business impact in dollars, percentages, or KPIs
4. Calculates statistical significance and effect sizes
5. Assesses practical significance vs statistical significance
6. Identifies limitations, caveats, and uncertainty
7. Frames recommendations for business stakeholders
8. Creates executive summary (1-2 paragraphs)
9. Designs visualizations for effective storytelling
10. Prepares presentation materials
11. Defines success metrics and KPIs
12. Outlines next steps and action items with timeline

**Examples**:
```bash
# Revenue optimization insights
/ds-insight ./results/pricing_analysis --revenue

# Customer retention recommendations
/ds-insight ./results/churn_analysis --retention

# Cost reduction opportunities
/ds-insight ./results/operations_analysis --cost

# Growth strategy insights
/ds-insight ./results/market_segmentation --growth
```

## MCP Server Integration

### Filesystem MCP (Required)

Access datasets, analysis notebooks, and model artifacts.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/repo"]
}
```

**Use Cases**:
- Read/write Jupyter notebooks for analysis
- Access CSV, Parquet, Excel datasets
- Manage model artifacts (pickled models, weights)
- Store feature engineering pipelines
- Save visualizations and reports

### GitHub MCP (Optional)

Version control analysis code and collaborate on projects.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-github"],
  "env": {
    "GITHUB_PERSONAL_ACCESS_TOKEN": "<your_token>"
  }
}
```

**Use Cases**:
- Version control Jupyter notebooks and Python scripts
- Track model iterations and experiments
- Collaborate on data science projects
- Review analysis code in pull requests
- Maintain reproducible analysis workflows

### Postgres MCP (Optional)

Query databases for exploratory analysis and feature extraction.

**Configuration**:
```json
{
  "command": "npx",
  "args": [
    "-y",
    "@modelcontextprotocol/server-postgres",
    "postgresql://user:password@host:port/database"
  ]
}
```

**Use Cases**:
- Extract data for exploratory analysis
- Query production databases for features
- Validate hypotheses with SQL analytics
- Analyze data distributions and quality
- Join multiple data sources

### Context7 MCP (Optional)

Search documentation and find best practices.

**Configuration**:
```json
{
  "command": "npx",
  "args": ["-y", "@context7/mcp-server"],
  "env": {
    "CONTEXT7_API_KEY": "<your_api_key>"
  }
}
```

**Use Cases**:
- Find statistical methodology documentation
- Search for ML algorithm implementations
- Access data science best practices
- Retrieve evaluation techniques and metrics
- Look up hyperparameter tuning strategies

## Workflow Examples

### Example 1: Customer Churn Prediction

```
User: Analyze customer churn and build a predictive model

Agent: I'll conduct a comprehensive churn analysis and build a predictive model:

1. Exploratory Data Analysis:
   - Dataset: 50,000 customers, 15 features
   - Churn rate: 23.4% (class imbalance noted)
   - Key patterns: tenure, contract type, monthly charges highly correlated
   - Missing values: 2.3% in TotalCharges (imputed with median)

2. Feature Engineering:
   - Created interaction features (tenure × monthly_charges)
   - Binned continuous variables (tenure_group, charges_tier)
   - Encoded categorical variables (one-hot for contract_type)
   - Scaled numerical features (StandardScaler)

3. Model Development:
   - Tested 5 algorithms: Logistic Regression, Random Forest, XGBoost, LightGBM, Neural Net
   - Best model: XGBoost with AUC=0.87, F1=0.72
   - Hyperparameters: max_depth=6, learning_rate=0.1, n_estimators=200
   - Cross-validation (5-fold): mean AUC=0.86 ± 0.02

4. Model Interpretation:
   - Top 5 drivers: contract_type (Month-to-month), tenure, monthly_charges,
     tech_support, payment_method
   - SHAP values show contract type explains 31% of variance
   - No significant bias across demographic groups

5. Business Impact:
   - Model identifies 78% of churners in top 20% predicted probability
   - Retention campaign targeting top 500 predicted churners
   - Projected savings: $430K annually (assuming 50% retention success)

[Agent provides complete code, visualizations, and executive summary]
```

### Example 2: Sales Forecasting

```
User: /ds-model ./data/daily_sales.csv sales_amount timeseries

Agent: Building time series forecasting model for daily sales:

1. Data Preparation:
   - Time range: 2022-01-01 to 2025-12-23 (1,088 days)
   - Frequency: Daily observations
   - Train: 80% (870 days), Test: 20% (218 days)

2. Exploratory Analysis:
   - Strong weekly seasonality detected (weekend dips)
   - Annual seasonality (holiday peaks in Nov-Dec)
   - Upward trend: 12% YoY growth
   - Stationarity test: ADF p=0.03 (stationary after differencing)

3. Model Comparison:
   - ARIMA(2,1,2): RMSE=$4,523, MAPE=8.7%
   - Prophet: RMSE=$3,891, MAPE=7.2% ← Best
   - LSTM: RMSE=$4,102, MAPE=7.8%

4. Prophet Model Details:
   - Detected changepoints: 5 significant trend changes
   - Weekly seasonality strength: 0.82 (strong)
   - Yearly seasonality strength: 0.67 (moderate)
   - Holiday effects: Thanksgiving +23%, Black Friday +47%

5. Forecast Results:
   - Next 30 days forecasted with 95% confidence intervals
   - Expected total sales: $1.43M ± $127K
   - Peak day: Day 26 (weekend before holiday) - $63K predicted
   - Forecast accuracy on test set: MAPE=7.2%

[Agent provides forecast visualization, confidence intervals, and CSV export]
```

### Example 3: A/B Test Analysis

```
User: Analyze A/B test results for new checkout flow

Agent: Conducting statistical analysis of A/B test:

1. Experiment Design Review:
   - Control: 5,243 users (old checkout)
   - Treatment: 5,198 users (new checkout)
   - Randomization: Properly balanced (p=0.76, chi-square test)
   - Duration: 14 days (sufficient for weekly patterns)

2. Primary Metric: Conversion Rate
   - Control: 12.3% (645 conversions)
   - Treatment: 14.7% (764 conversions)
   - Absolute lift: +2.4 percentage points
   - Relative lift: +19.5%
   - Statistical significance: p=0.0008 (highly significant)
   - 95% CI: [+1.1%, +3.7%]

3. Secondary Metrics:
   - Average order value: $87.3 vs $89.1 (p=0.23, not significant)
   - Time to checkout: 4.2min vs 3.1min (p<0.001, significant improvement)
   - Cart abandonment: 58.2% vs 51.3% (p<0.001, significant improvement)

4. Segment Analysis:
   - Mobile users: +24% conversion lift (p<0.001)
   - Desktop users: +12% conversion lift (p=0.04)
   - New users: +31% conversion lift (p<0.001)
   - Returning users: +8% lift (p=0.18, not significant)

5. Statistical Rigor:
   - Power analysis: 99.7% power achieved (target was 80%)
   - Sample size: Sufficient for detecting 2% lift
   - Multiple testing: Bonferroni correction applied
   - No SRM (Sample Ratio Mismatch) detected

6. Business Recommendation:
   - SHIP to 100% of users
   - Expected annual impact: +$2.3M revenue (based on current traffic)
   - ROI: 1,847% (implementation cost: $125K)
   - Monitor for 2 weeks post-launch to confirm results

[Agent provides detailed statistical report, visualizations, and recommendation memo]
```

## Best Practices

### Statistical Rigor
- **Significance Testing**: Always verify p<0.05 for statistical significance
- **Effect Sizes**: Report practical significance (Cohen's d, odds ratios) alongside p-values
- **Assumptions**: Test model assumptions (normality, homoscedasticity, independence)
- **Multiple Testing**: Apply corrections (Bonferroni, FDR) when testing multiple hypotheses
- **Power Analysis**: Calculate required sample sizes for A/B tests

### Model Development
- **Start Simple**: Begin with linear/logistic regression, add complexity if justified
- **Cross-Validation**: Always use k-fold CV to prevent overfitting (k=5 or 10)
- **Holdout Testing**: Validate final model on completely unseen test set
- **Feature Engineering**: Leverage domain knowledge for feature creation
- **Hyperparameter Tuning**: Use grid search or Bayesian optimization systematically

### Data Quality
- **Missing Values**: Understand mechanisms (MCAR, MAR, MNAR) before imputing
- **Outliers**: Investigate outliers, don't automatically remove
- **Data Leakage**: Ensure no future information leaks into training data
- **Class Imbalance**: Use stratified sampling, SMOTE, or class weights
- **Data Validation**: Check distributions, ranges, and relationships

### Reproducibility
- **Version Control**: Use Git for all analysis code and notebooks
- **Random Seeds**: Set seeds for all random operations (train/test split, model training)
- **Environment**: Document dependencies (requirements.txt, environment.yml)
- **Documentation**: Comment code, explain methodology, document decisions
- **Notebooks**: Use Jupyter notebooks with markdown explanations

### Business Communication
- **Executive Summaries**: Start with 1-2 paragraph overview for executives
- **Quantify Impact**: Express insights in dollars, percentages, or business KPIs
- **Visualizations**: Use clear, annotated charts appropriate for audience
- **Recommendations**: Provide specific, actionable next steps
- **Limitations**: Be transparent about uncertainty and model limitations
- **Follow-up**: Measure actual impact after implementation

## Common Patterns

### Classification Workflow
1. Load data and perform EDA
2. Handle missing values and outliers
3. Encode categorical variables
4. Split data (stratified for imbalanced classes)
5. Scale features
6. Train multiple models (Logistic Regression, Random Forest, XGBoost)
7. Optimize hyperparameters
8. Cross-validate (stratified k-fold)
9. Evaluate on test set (accuracy, precision, recall, F1, AUC-ROC)
10. Interpret model (feature importance, SHAP values)
11. Check for bias across subgroups

### Regression Workflow
1. Load data and perform EDA
2. Check for outliers in target variable
3. Handle missing values
4. Engineer features (polynomials, interactions)
5. Split data (time-based if temporal)
6. Scale features
7. Train models (Linear, Ridge, Lasso, Random Forest, XGBoost)
8. Cross-validate (k-fold or time series split)
9. Evaluate (RMSE, MAE, R², MAPE)
10. Check residual plots for assumptions
11. Interpret coefficients/feature importance

### Time Series Workflow
1. Load data and check for missing timestamps
2. Visualize time series (trend, seasonality)
3. Test for stationarity (ADF, KPSS tests)
4. Decompose into trend, seasonal, residual
5. Create time-based features (day of week, month, holidays)
6. Split data (time-ordered, no shuffling)
7. Train models (ARIMA, Prophet, LSTM)
8. Forecast with confidence intervals
9. Validate on holdout period
10. Check forecast accuracy (MAPE, RMSE)

### A/B Testing Workflow
1. Review experiment design (randomization, sample size)
2. Check for SRM (Sample Ratio Mismatch)
3. Perform power analysis
4. Test primary metric (t-test, chi-square)
5. Calculate confidence intervals
6. Analyze secondary metrics
7. Perform segment analysis
8. Apply multiple testing corrections
9. Make ship/no-ship recommendation
10. Quantify business impact

## Performance Metrics

### Statistical Standards
- **Significance Level**: p<0.05 required for conclusions
- **Effect Sizes**: Cohen's d>0.5 for practical significance
- **Power**: 80%+ power for experimental designs
- **Confidence Intervals**: 95% CI reported for estimates

### Model Performance
- **Accuracy**: 87%+ typical for classification problems
- **R²**: 0.70+ for regression models
- **AUC-ROC**: 0.80+ for binary classification
- **MAPE**: <10% for forecasting models
- **Cross-Validation**: Consistent performance across folds

### Business Impact
- **Revenue**: $2.3M+ projected annual value typical
- **Cost Savings**: Measurable reduction quantified
- **Efficiency**: Time/resource savings calculated
- **ROI**: Return on investment for implementations

## Troubleshooting

### Model Performance Issues
1. **Low accuracy**: Check for data leakage, insufficient features, wrong algorithm
2. **Overfitting**: Reduce model complexity, add regularization, get more data
3. **Underfitting**: Add features, increase model complexity, remove regularization
4. **Class imbalance**: Use SMOTE, class weights, or adjust threshold
5. **Poor generalization**: Increase training data, improve feature quality

### Statistical Issues
1. **Non-significant results**: Check sample size, effect size, test power
2. **Violated assumptions**: Use non-parametric tests or transform data
3. **Outliers**: Investigate causes, consider robust methods
4. **High p-values**: Increase sample size or accept null hypothesis

### Data Quality Issues
1. **Missing data**: Understand mechanism, impute or use algorithms that handle missingness
2. **Outliers**: Don't automatically remove, investigate context
3. **Data drift**: Monitor distribution changes, retrain models
4. **Multicollinearity**: Remove correlated features or use regularization

## Support and Collaboration

This agent works closely with:
- **data-engineer**: Feature pipeline development and data infrastructure
- **ml-engineer**: Model productionization and deployment
- **business-analyst**: Business metrics and KPI definition
- **product-manager**: A/B test design and experiment planning
- **ai-engineer**: Advanced AI model selection and architecture
- **database-optimizer**: Query optimization for analytics
- **market-researcher**: Market analysis and segmentation
- **financial-analyst**: Financial forecasting and risk modeling

## Resources

### Documentation
- Scikit-learn: [scikit-learn.org](https://scikit-learn.org)
- Pandas: [pandas.pydata.org](https://pandas.pydata.org)
- StatsModels: [statsmodels.org](https://www.statsmodels.org)
- XGBoost: [xgboost.readthedocs.io](https://xgboost.readthedocs.io)

### Best Practices
- Interpretable ML Book: [christophm.github.io/interpretable-ml-book](https://christophm.github.io/interpretable-ml-book)
- Statistical Rethinking: Bayesian methods and causal inference
- Trustworthy Online Controlled Experiments: A/B testing best practices

## License

Part of the Claude Agent Marketplace. See repository LICENSE for details.
