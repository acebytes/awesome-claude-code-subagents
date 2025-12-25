# Quant Analyst Agent

Expert quantitative analyst specializing in financial modeling, algorithmic trading, and risk analytics. Masters statistical methods, derivatives pricing, and high-frequency trading with focus on mathematical rigor, performance optimization, and profitable strategy development.

## Overview

The Quant Analyst agent is designed to develop sophisticated quantitative trading strategies, financial models, and risk management systems. It combines deep expertise in mathematical finance, statistical methods, and computational optimization to generate alpha in competitive markets.

## Capabilities

### Financial Modeling
- Pricing models (Black-Scholes, binomial trees, Monte Carlo)
- Risk models (VaR, CVaR, stress testing)
- Portfolio optimization (Markowitz, Black-Litterman, risk parity)
- Factor models and volatility modeling
- Correlation and scenario analysis

### Trading Strategies
- Statistical arbitrage and pairs trading
- Market making algorithms
- Momentum and mean reversion strategies
- Options strategies and Greeks hedging
- Event-driven and crypto trading algorithms

### Risk Management
- Value at Risk (VaR) calculation
- Conditional VaR and tail risk analysis
- Stress testing and scenario analysis
- Position sizing and drawdown control
- Portfolio hedging and correlation analysis

### High-Frequency Trading
- Market microstructure analysis
- Order book dynamics modeling
- Latency optimization (sub-millisecond)
- Execution algorithms and market impact models
- Tick data analysis and hardware optimization

### Backtesting & Validation
- Historical simulation and walk-forward analysis
- Out-of-sample testing
- Transaction costs and slippage modeling
- Performance metrics (Sharpe ratio, win rate, drawdown)
- Overfitting detection and robustness testing

## MCP Servers

The agent uses the following MCP servers:

- **filesystem**: Access to local file system for reading/writing models and data
- **github**: Version control for trading strategies and research code
- **memory**: Persistent storage for trading insights and strategy parameters
- **postgres**: Database access for market data, backtests, and performance tracking

## Slash Commands

### /quant-model
Develop quantitative financial models for pricing, risk analysis, or factor modeling.

```bash
/quant-model <model_type> <asset_class> [parameters]
```

**Examples:**
```bash
/quant-model black-scholes options --volatility=0.25 --risk-free-rate=0.05
/quant-model var equity-portfolio --confidence=0.99 --horizon=10d
/quant-model factor-model equities --factors=fama-french-5
```

### /backtest
Execute comprehensive backtesting of trading strategies with detailed performance metrics.

```bash
/backtest <strategy_path> <start_date> <end_date> [options]
```

**Examples:**
```bash
/backtest ./strategies/stat_arb.py 2015-01-01 2024-12-31 --initial-capital=1000000
/backtest ./strategies/pairs_trading.py 2020-01-01 2024-12-31 --transaction-cost=0.001
/backtest ./strategies/momentum.py 2018-01-01 2024-12-31 --slippage=0.0005
```

### /risk-calc
Calculate comprehensive risk metrics including VaR, CVaR, stress tests, and options Greeks.

```bash
/risk-calc <portfolio_path> <risk_type> [confidence_level]
```

**Examples:**
```bash
/risk-calc ./portfolios/equity_portfolio.json var --confidence=0.99
/risk-calc ./portfolios/options_book.json greeks --underlying=SPY
/risk-calc ./portfolios/multi_asset.json stress-test --scenario=2008-crisis
```

### /portfolio-optimize
Optimize portfolio allocation using quantitative methods (Markowitz, Black-Litterman, risk parity).

```bash
/portfolio-optimize <assets> <method> [constraints]
```

**Examples:**
```bash
/portfolio-optimize ./data/sp500.csv markowitz --target-return=0.12
/portfolio-optimize ./data/multi_asset.csv black-litterman --risk-aversion=2.5
/portfolio-optimize ./data/commodities.csv risk-parity --max-weight=0.2
```

## Usage Guide

### Getting Started

1. **Set up environment variables:**
   ```bash
   export GITHUB_TOKEN="your_github_token"
   export POSTGRES_URL="postgresql://user:pass@localhost:5432/trading_db"
   ```

2. **Initialize the agent:**
   The agent will automatically query the context manager for:
   - Asset classes and market focus
   - Trading frequency and time horizon
   - Risk tolerance and capital allocation
   - Regulatory constraints
   - Performance targets

### Typical Workflow

#### 1. Strategy Research
```bash
# Analyze market data for opportunities
"Analyze SPY and QQQ for statistical arbitrage opportunities in 2024"

# Test hypothesis
/quant-model cointegration equities --symbols=SPY,QQQ --period=2020-2024
```

#### 2. Model Development
```bash
# Develop pricing model
/quant-model black-scholes options --symbol=AAPL --expiry=2025-03-21

# Build risk model
/risk-calc ./portfolios/options_portfolio.json var --confidence=0.95
```

#### 3. Backtesting
```bash
# Run comprehensive backtest
/backtest ./strategies/mean_reversion.py 2020-01-01 2024-12-31 \
  --initial-capital=1000000 \
  --transaction-cost=0.001 \
  --slippage=0.0005

# Analyze results
"Generate performance attribution report for the backtest"
```

#### 4. Portfolio Optimization
```bash
# Optimize allocation
/portfolio-optimize ./data/etf_universe.csv markowitz \
  --target-return=0.15 \
  --max-weight=0.25 \
  --min-weight=0.05

# Risk parity allocation
/portfolio-optimize ./data/asset_classes.csv risk-parity
```

#### 5. Risk Management
```bash
# Calculate VaR
/risk-calc ./portfolios/current_positions.json var --confidence=0.99

# Stress testing
/risk-calc ./portfolios/current_positions.json stress-test \
  --scenario=market-crash \
  --severity=3-sigma

# Greeks analysis
/risk-calc ./portfolios/options_book.json greeks --underlying=SPX
```

### Advanced Features

#### Machine Learning Integration
```bash
# Price prediction with ML
"Develop LSTM model for SPY price prediction using 10 years of data"

# Feature engineering
"Extract technical indicators and market microstructure features for ML model"

# Ensemble methods
"Build ensemble model combining XGBoost, Random Forest, and Neural Network"
```

#### High-Frequency Trading
```bash
# Analyze order book
"Analyze order book dynamics for AAPL to identify liquidity patterns"

# Optimize execution
"Develop TWAP execution algorithm with market impact minimization"

# Latency optimization
"Profile strategy execution time and optimize to sub-millisecond latency"
```

#### Alternative Data
```bash
# Sentiment analysis
"Incorporate Twitter sentiment data into trading strategy"

# News processing
"Build NLP pipeline to extract trading signals from financial news"
```

## Integration with Other Agents

The Quant Analyst works seamlessly with:

- **risk-manager**: Collaborate on risk modeling and stress testing
- **fintech-engineer**: Support trading system implementation
- **data-engineer**: Work on market data pipelines and storage
- **ml-engineer**: Guide machine learning model development
- **backend-developer**: Help with system architecture
- **database-optimizer**: Optimize tick data storage and queries
- **cloud-architect**: Design scalable infrastructure
- **compliance-officer**: Ensure regulatory compliance

## Best Practices

### Model Development
- Always validate models with out-of-sample data
- Use conservative assumptions for transaction costs and slippage
- Implement robust error handling and edge case testing
- Document all modeling assumptions and limitations

### Backtesting
- Avoid look-ahead bias and survivorship bias
- Include realistic transaction costs and market impact
- Test across multiple market regimes
- Use walk-forward optimization to prevent overfitting

### Risk Management
- Calculate multiple risk metrics (VaR, CVaR, stress tests)
- Monitor tail risk and correlation breakdowns
- Implement position limits and drawdown controls
- Regular stress testing with historical crisis scenarios

### Production Deployment
- Monitor live performance vs. backtest expectations
- Implement circuit breakers and kill switches
- Log all trades and model decisions
- Regular model retraining and validation

## Performance Metrics

The agent tracks comprehensive performance metrics:

- **Returns**: Annualized return, CAGR, excess returns
- **Risk**: Sharpe ratio, Sortino ratio, Calmar ratio
- **Drawdown**: Maximum drawdown, average drawdown, recovery time
- **Win Rate**: Percentage of profitable trades
- **Risk Metrics**: VaR, CVaR, tail risk, beta, correlation
- **Execution**: Fill rate, slippage, transaction costs

## Example Output

```
Quantitative system completed. Developed statistical arbitrage strategy with 2.3 Sharpe ratio
over 10-year backtest. Maximum drawdown 12% with 68% win rate. Implemented with sub-millisecond
execution achieving 23% annualized returns after costs.

Key Metrics:
- Sharpe Ratio: 2.3
- Annualized Return: 23%
- Maximum Drawdown: 12%
- Win Rate: 68%
- Avg Trade Duration: 2.3 hours
- Transaction Costs: 0.8% of returns
- 99% VaR: 3.2%
```

## Environment Requirements

### Python Libraries
```bash
pip install numpy pandas scipy scikit-learn
pip install statsmodels arch pymc3
pip install ta-lib zipline backtrader
pip install cvxpy cvxopt
pip install tensorflow torch
```

### Database Setup
```sql
-- Create tables for market data
CREATE TABLE market_data (
  symbol VARCHAR(10),
  timestamp TIMESTAMP,
  open DECIMAL,
  high DECIMAL,
  low DECIMAL,
  close DECIMAL,
  volume BIGINT,
  PRIMARY KEY (symbol, timestamp)
);

-- Create tables for backtests
CREATE TABLE backtest_results (
  id SERIAL PRIMARY KEY,
  strategy_name VARCHAR(100),
  start_date DATE,
  end_date DATE,
  sharpe_ratio DECIMAL,
  max_drawdown DECIMAL,
  annualized_return DECIMAL,
  created_at TIMESTAMP DEFAULT NOW()
);
```

## License

MIT License - See LICENSE file for details

## Support

For questions or issues:
- Review existing quant strategies in the repository
- Check backtesting best practices documentation
- Consult risk management guidelines
- Contact the quantitative research team

---

**Note**: This agent is designed for quantitative research and strategy development. Always validate models thoroughly, test extensively, and implement proper risk controls before deploying any trading strategy in production.
