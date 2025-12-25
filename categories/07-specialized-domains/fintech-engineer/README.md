# Fintech Engineer Agent

Expert fintech engineer specializing in financial systems, regulatory compliance, and secure transaction processing. Masters banking integrations, payment systems, and building scalable financial technology that meets stringent regulatory requirements.

## Overview

The Fintech Engineer agent is a specialized AI assistant designed to help build secure, compliant financial systems. It provides expertise in payment processing, banking integrations, regulatory compliance, fraud detection, and trading platforms while ensuring 100% transaction accuracy and regulatory adherence.

## Features

- **Banking System Integration**: Core banking APIs, account management, transaction processing, reconciliation
- **Payment Processing**: Gateway integration, authorization flows, settlement, multi-currency support
- **Trading Platforms**: Order management, matching engines, market data feeds, risk management
- **Regulatory Compliance**: KYC/AML implementation, transaction monitoring, audit requirements
- **Fraud Detection**: Real-time monitoring, behavioral analysis, ML-based scoring
- **Blockchain Integration**: Cryptocurrency support, smart contracts, DeFi protocols
- **Open Banking APIs**: Account aggregation, payment initiation, consent management
- **Security Architecture**: Zero trust model, encryption, key management, API authentication

## Prerequisites

### Required Environment Variables

- `POSTGRES_URL`: PostgreSQL connection string for financial database access
  - Example: `postgresql://user:password@localhost:5432/fintech_db`

### Optional Environment Variables

- `GITHUB_TOKEN`: GitHub personal access token for repository access

### System Requirements

- Node.js and npx installed
- PostgreSQL database for financial data
- Access to payment gateway APIs (if applicable)
- Compliance certifications documentation

## Installation

1. Clone or download the agent files to your preferred location
2. Set up the required environment variables in your shell or `.env` file:

```bash
export POSTGRES_URL="postgresql://user:password@localhost:5432/fintech_db"
export GITHUB_TOKEN="your-github-token"  # Optional
```

3. The MCP servers will be automatically installed when the agent starts (via `npx -y`)

## Usage

### Starting the Agent

Load the agent configuration into Claude Code:

```bash
claude-code --agent fintech-engineer
```

### Slash Commands

The agent provides four specialized slash commands for common fintech operations:

#### `/fintech-audit`
Perform a comprehensive audit of your fintech system:
- Compliance verification (PCI DSS, KYC/AML, GDPR)
- Security assessment
- Transaction accuracy validation
- Regulatory requirement review
- Audit trail completeness
- Performance metrics analysis

**Example:**
```
/fintech-audit
```

#### `/pci-check`
Validate PCI DSS compliance across your infrastructure:
- Infrastructure security
- Application security controls
- Data storage encryption
- Network security measures
- Access control policies
- Logging and monitoring
- Incident response procedures

**Example:**
```
/pci-check
```

#### `/ledger-design`
Design or review double-entry ledger systems:
- ACID compliance verification
- Transaction journaling
- Reconciliation processes
- Audit trail implementation
- Balance integrity checks
- Historical data retention
- Error handling and recovery

**Example:**
```
/ledger-design --for payment-processing
```

#### `/transaction-flow`
Analyze and optimize transaction flows:
- Authorization flow analysis
- Settlement process review
- Error handling mechanisms
- Retry logic optimization
- Timeout configuration
- Idempotency checks
- Performance bottlenecks

**Example:**
```
/transaction-flow --optimize
```

## MCP Servers

The agent uses the following MCP servers:

1. **Filesystem** (`@modelcontextprotocol/server-filesystem`)
   - Access to local files and directories
   - Read/write financial system configurations

2. **GitHub** (`@modelcontextprotocol/server-github`)
   - Repository access for code reviews
   - Pull request management
   - Issue tracking for compliance tasks

3. **Context7** (`@upstash/context7-mcp`)
   - Up-to-date documentation access
   - Payment gateway API references
   - Regulatory framework updates

4. **Memory** (`@modelcontextprotocol/server-memory`)
   - Persistent context across sessions
   - Financial system architecture memory
   - Compliance requirement tracking

5. **Postgres** (`@modelcontextprotocol/server-postgres`)
   - Direct database access for financial data
   - Transaction analysis
   - Ledger verification
   - Audit trail queries

## Common Use Cases

### 1. Building a Payment Processing System

```
I need to build a payment processing system that handles credit card transactions
with PCI DSS compliance. Requirements:
- Support for Visa, Mastercard, Amex
- 99.99% uptime
- < 100ms latency
- Multi-currency support
- Fraud detection
```

### 2. Implementing KYC/AML Compliance

```
Help me implement a KYC/AML system for our banking application. We need:
- Identity verification
- Document validation
- Watchlist screening
- Risk scoring
- Ongoing monitoring
- Regulatory reporting for FinCEN
```

### 3. Designing a Trading Platform

```
Design a matching engine for our stock trading platform:
- Support for limit, market, and stop orders
- Real-time market data feeds
- Position tracking
- P&L calculation
- Margin requirements
- Regulatory reporting
```

### 4. Audit Trail Implementation

```
/fintech-audit

Review our current transaction logging and help implement a comprehensive
audit trail that meets SOC 2 requirements.
```

### 5. Database Schema for Ledger

```
/ledger-design

Design a PostgreSQL schema for a double-entry accounting ledger that:
- Handles multi-currency transactions
- Supports transaction reversal
- Maintains historical balance snapshots
- Ensures data integrity with constraints
```

## Performance Targets

The agent helps you achieve:

- **Transaction Accuracy**: 100% verified
- **System Uptime**: > 99.99%
- **Latency**: < 100ms for payment processing
- **Compliance Score**: 98%+ on regulatory audits

## Compliance Frameworks

Expert support for:

- PCI DSS (Payment Card Industry Data Security Standard)
- KYC (Know Your Customer)
- AML (Anti-Money Laundering)
- GDPR (General Data Protection Regulation)
- SOC 2 (Service Organization Control 2)
- ISO 27001 (Information Security Management)

## Security Best Practices

The agent enforces:

- Zero trust security model
- Encryption at rest and in transit (TLS)
- Secure key management
- Token-based authentication
- Rate limiting and DDoS protection
- Immutable audit logs
- Idempotent operations
- Circuit breakers for resilience

## Integration with Other Agents

Works seamlessly with:

- **security-engineer**: Threat modeling and security audits
- **cloud-architect**: Infrastructure design and scaling
- **database-administrator**: Financial data optimization
- **devops-engineer**: CI/CD for fintech applications
- **compliance-auditor**: Regulatory compliance verification

## Troubleshooting

### Database Connection Issues

If you encounter PostgreSQL connection errors:

1. Verify `POSTGRES_URL` is correctly set
2. Ensure the database is running and accessible
3. Check network connectivity and firewall rules
4. Verify database credentials

### PCI Compliance Warnings

If the agent flags PCI compliance issues:

1. Review the specific findings
2. Use `/pci-check` for detailed analysis
3. Implement recommended security controls
4. Re-run validation after fixes

### Transaction Accuracy Problems

If transaction reconciliation fails:

1. Use `/ledger-design` to review schema
2. Check for race conditions in concurrent transactions
3. Verify idempotency implementation
4. Review error handling and retry logic

## Example Workflows

### Complete Payment Gateway Integration

```bash
# 1. Start with requirements gathering
Help me integrate Stripe for payment processing. I need to support
subscriptions, one-time payments, and refunds.

# 2. Review security requirements
/pci-check

# 3. Design the transaction flow
/transaction-flow

# 4. Implement with the agent's guidance
Implement the Stripe integration with proper error handling and webhook
processing.

# 5. Validate compliance
/fintech-audit
```

### Building a Fraud Detection System

```bash
# 1. Define fraud detection requirements
I need to build a real-time fraud detection system for credit card transactions.
Include velocity checks, device fingerprinting, and ML-based scoring.

# 2. Design the data architecture
Design a PostgreSQL schema for storing transaction patterns and fraud signals.

# 3. Implement monitoring
Set up real-time monitoring with alerts for suspicious patterns.

# 4. Validate the system
Test the fraud detection system with various attack scenarios.
```

## Best Practices

1. **Always prioritize security** - Use encryption, secure authentication, and zero trust principles
2. **Ensure compliance first** - Verify regulatory requirements before implementation
3. **Maintain audit trails** - Log all transactions and system events
4. **Test thoroughly** - Validate 100% transaction accuracy
5. **Monitor continuously** - Track performance, security events, and compliance metrics
6. **Document everything** - Maintain comprehensive documentation for audits

## Support and Resources

- Review `CLAUDE.md` for detailed agent instructions
- Check `agent-manifest.json` for capability reference
- Consult `mcp-config.json` for MCP server configuration
- Join the Claude Code community for additional support

## License

Part of the Claude Code Agent Marketplace. See repository license for details.
