# Risk Manager Agent

Expert risk manager specializing in comprehensive risk assessment, mitigation strategies, and compliance frameworks. Masters risk modeling, stress testing, and regulatory compliance with focus on protecting organizations from financial, operational, and strategic risks.

## Overview

The Risk Manager agent is a senior-level risk management specialist capable of identifying, quantifying, and mitigating enterprise risks across multiple categories including market risk, credit risk, operational risk, and regulatory risk. It implements industry-standard frameworks and provides data-driven risk management solutions.

## Key Capabilities

### Risk Assessment
- Comprehensive risk identification across all categories
- Threat assessment and vulnerability analysis
- Impact evaluation and likelihood estimation
- Risk mapping and categorization
- Emerging and interconnected risk analysis

### Risk Quantification
- VaR (Value at Risk) modeling
- Expected shortfall calculations
- Monte Carlo simulation
- Credit scoring and loss distribution
- Stress testing and scenario analysis

### Risk Categories Covered
- **Market Risk**: Price, interest rate, currency, commodity, equity, volatility
- **Credit Risk**: PD/LGD/EAD modeling, counterparty risk, concentration risk
- **Operational Risk**: Process controls, fraud prevention, business continuity
- **Liquidity Risk**: Funding and market liquidity analysis
- **Model Risk**: Validation, backtesting, governance
- **Cybersecurity Risk**: Threat assessment and controls
- **Regulatory Risk**: Compliance monitoring and gap analysis
- **Reputational Risk**: Impact assessment and mitigation

### Compliance & Frameworks
- Basel III compliance
- COSO framework
- ISO 31000
- Solvency II
- ORSA requirements
- FRTB standards
- IFRS 9
- Regulatory reporting

## Slash Commands

### `/risk-assess`
Conduct a comprehensive risk assessment across all risk categories.

**Example usage:**
```
/risk-assess
```

The agent will:
- Identify risks across market, credit, operational, and other categories
- Quantify exposure levels and potential impact
- Prioritize risks based on likelihood and impact matrices
- Provide detailed risk profiles with supporting data

### `/risk-matrix`
Generate a visual risk matrix plotting identified risks by likelihood and impact.

**Example usage:**
```
/risk-matrix
```

The agent will:
- Create heat maps showing risk distribution
- Plot risks on likelihood vs. impact axes
- Provide prioritization frameworks
- Generate executive-level visualizations

### `/mitigation-plan`
Develop detailed risk mitigation strategies with actionable recommendations.

**Example usage:**
```
/mitigation-plan
```

The agent will:
- Design control frameworks
- Recommend risk transfer strategies (insurance, hedging)
- Suggest risk avoidance and reduction measures
- Create contingency plans with timelines
- Provide cost-benefit analysis

### `/stress-test`
Execute comprehensive stress testing scenarios to assess resilience.

**Example usage:**
```
/stress-test
```

The agent will:
- Design historical and hypothetical scenarios
- Perform sensitivity analysis
- Execute reverse stress testing
- Test against regulatory scenarios
- Validate model performance
- Analyze results and provide recommendations

## MCP Servers

This agent uses the following MCP servers:

### Filesystem
Provides access to local filesystem for reading risk data, models, and reports.

### GitHub
Enables version control for risk models, frameworks, and compliance documentation.

### Memory
Maintains context about risk assessments, historical data, and ongoing risk management activities.

## Configuration

### Environment Variables

For GitHub integration, set:
```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

### MCP Setup

The agent is pre-configured with the necessary MCP servers in `mcp-config.json`. No additional setup required beyond environment variables.

## Usage Examples

### Example 1: Comprehensive Risk Assessment

```
/risk-assess

Please assess all risks for our fintech lending platform, focusing on:
- Credit risk from loan portfolio
- Operational risks in underwriting process
- Regulatory compliance with lending regulations
- Cybersecurity risks in customer data handling
```

### Example 2: Stress Testing

```
/stress-test

Run stress tests for our investment portfolio using:
- 2008 financial crisis scenario
- Interest rate shock (+200 bps)
- Market crash scenario (-30% equity markets)
- Credit spread widening scenario
```

### Example 3: Mitigation Planning

```
/mitigation-plan

We've identified high operational risk in our payment processing system. Please develop a mitigation plan including:
- Control enhancements
- Backup systems
- Insurance options
- Incident response procedures
```

### Example 4: Risk Matrix Generation

```
/risk-matrix

Generate a risk matrix for our Q4 2024 enterprise risk assessment covering all identified risks across market, credit, operational, and strategic categories.
```

## Integration with Other Agents

The Risk Manager agent collaborates effectively with:

- **Quant Analyst**: Risk model development and validation
- **Compliance Officer**: Regulatory compliance and monitoring
- **Security Auditor**: Cybersecurity risk assessment
- **Fintech Engineer**: Technical control implementation
- **CFO**: Financial risk management and reporting
- **Internal Auditor**: Risk assessment and audit support
- **Data Scientist**: Advanced analytics and modeling

## Best Practices

### For Risk Assessment
1. Provide comprehensive context about your organization, business model, and regulatory environment
2. Share historical loss data and existing risk frameworks
3. Specify risk appetite and tolerance levels
4. Include information about existing controls

### For Stress Testing
1. Define clear scenarios aligned with your risk profile
2. Specify confidence levels and time horizons
3. Provide historical data for backtesting
4. Include regulatory scenario requirements

### For Mitigation Planning
1. Clearly articulate risk tolerance and budget constraints
2. Prioritize risks by impact and likelihood
3. Share existing control frameworks
4. Specify implementation timelines and resources

### For Compliance
1. Identify all applicable regulatory frameworks
2. Share compliance gap assessments
3. Provide audit and examination history
4. Include remediation tracking requirements

## Output Examples

### Risk Assessment Output
- Detailed risk inventory with categorization
- Quantified exposure metrics (VaR, expected loss, etc.)
- Risk ratings and prioritization
- Control effectiveness assessment
- Gap analysis and recommendations

### Stress Test Results
- Scenario definitions and assumptions
- Impact analysis by scenario
- Model validation results
- Sensitivity analysis
- Recommendations for risk mitigation

### Mitigation Plan
- Prioritized risk treatment strategies
- Control design recommendations
- Cost-benefit analysis
- Implementation roadmap with timelines
- Key risk indicators (KRIs) for monitoring

### Risk Matrix
- Visual heat map of risks
- Likelihood vs. impact plotting
- Risk categorization
- Trend analysis
- Executive summary

## Technical Requirements

- Node.js (for MCP servers)
- Git (for version control integration)
- Access to risk data sources and historical loss data
- Regulatory framework documentation

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

Part of the Claude Code Agent Marketplace - refer to repository license.
