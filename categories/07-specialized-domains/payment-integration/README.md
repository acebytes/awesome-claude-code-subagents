# Payment Integration Agent

Expert payment integration specialist mastering payment gateway integration, PCI compliance, and financial transaction processing. Specializes in secure payment flows, multi-currency support, and fraud prevention with focus on reliability, compliance, and seamless user experience.

## Overview

This agent helps you implement secure, compliant payment systems with expertise spanning:

- **Payment Gateway Integration**: Stripe, Braintree, Adyen, PayPal, and more
- **PCI DSS Compliance**: Security standards, tokenization, and audit preparation
- **Transaction Processing**: Authorization, capture, refunds, and reconciliation
- **Subscription Billing**: Recurring payments, plan management, and dunning
- **Fraud Prevention**: Risk scoring, velocity checks, and 3D Secure
- **Multi-Currency**: International payments, exchange rates, and local pricing
- **Webhook Infrastructure**: Reliable event handling and state synchronization

## Quick Start

### Prerequisites

1. **Environment Variables**:
   - `GITHUB_TOKEN`: GitHub personal access token for repository access
   - `STRIPE_API_KEY` (optional): For Stripe integration examples
   - `STRIPE_WEBHOOK_SECRET` (optional): For webhook signature verification

2. **MCP Servers**:
   - **filesystem**: File system operations
   - **github**: Repository integration and version control
   - **context7**: Access to payment gateway documentation
   - **memory**: Persistent context for compliance requirements

### Installation

1. Copy the `payment-integration` directory to your agents folder
2. Configure your MCP servers in `mcp-config.json`
3. Set required environment variables
4. Load the agent with `CLAUDE.md` as instructions

## Slash Commands

### `/payment-flow`

Analyze and design payment flows for your application.

**Usage**:
```
/payment-flow

I need to design a checkout flow for a SaaS product with:
- Monthly and annual subscriptions
- Trial period of 14 days
- Support for credit cards and PayPal
- Multi-currency (USD, EUR, GBP)
```

**The agent will**:
- Analyze your business requirements
- Design the complete payment flow
- Recommend payment methods and gateways
- Identify compliance requirements
- Create implementation checklist

### `/stripe-setup`

Configure Stripe integration from scratch.

**Usage**:
```
/stripe-setup

Set up Stripe for my e-commerce store with:
- Product catalog integration
- One-time payments
- Customer portal for subscriptions
- Webhook handling for payment events
```

**The agent will**:
- Guide API key configuration
- Set up payment methods (cards, wallets, etc.)
- Configure webhook endpoints
- Implement idempotency and error handling
- Ensure PCI compliance with tokenization

### `/pci-audit`

Conduct PCI DSS compliance audit.

**Usage**:
```
/pci-audit

Audit our payment implementation for PCI compliance:
- We use Stripe for card processing
- Customer data stored in PostgreSQL
- API built with Node.js and Express
- Deployed on AWS
```

**The agent will**:
- Review your architecture for PCI requirements
- Identify compliance gaps
- Assess data handling practices
- Check encryption and tokenization
- Provide remediation roadmap
- Recommend appropriate SAQ (Self-Assessment Questionnaire)

### `/webhook-config`

Set up reliable webhook handling.

**Usage**:
```
/webhook-config

Configure webhooks for Stripe events:
- payment_intent.succeeded
- payment_intent.failed
- customer.subscription.updated
- invoice.payment_failed
```

**The agent will**:
- Design webhook endpoint architecture
- Implement signature verification
- Set up idempotency handling
- Configure retry mechanisms
- Create event queue processing
- Add monitoring and alerting

## Key Capabilities

### Payment Gateway Integration

- **Stripe**: Full API integration, Checkout, Payment Intents, Subscriptions
- **Braintree**: PayPal support, drop-in UI, hosted fields
- **Adyen**: Global processing, smart routing, local payment methods
- **PayPal**: Express Checkout, subscription buttons, REST API
- **Square**: In-person and online payments, inventory integration

### Transaction Types

- **One-time payments**: Standard checkout flow
- **Recurring billing**: Subscriptions, installments
- **Marketplace**: Split payments, platform fees
- **Pre-authorization**: Hotel-style holds
- **Delayed capture**: Fulfill-then-charge
- **Refunds**: Full, partial, automated

### Security & Compliance

- **PCI DSS Levels 1-4**: Compliance assessment and implementation
- **Tokenization**: No raw card data storage
- **Encryption**: TLS 1.3, AES-256 at rest
- **3D Secure**: SCA compliance for European payments
- **Fraud detection**: Machine learning models, rule engines
- **Audit trails**: Comprehensive logging for compliance

### Advanced Features

- **Multi-currency**: Dynamic pricing, local currencies, FX handling
- **Payment routing**: Smart gateway selection, failover
- **Reconciliation**: Automated settlement matching
- **Dispute management**: Chargeback evidence automation
- **Analytics**: Revenue reporting, payment success metrics
- **Testing**: Sandbox environments, test card scenarios

## Integration Patterns

### Direct API Integration

Full control over payment flow with direct API calls.

```javascript
// Example: Stripe Payment Intent
const paymentIntent = await stripe.paymentIntents.create({
  amount: 2000,
  currency: 'usd',
  payment_method_types: ['card'],
  metadata: { order_id: '12345' }
});
```

### Hosted Checkout

PCI-simplified approach with gateway-hosted pages.

```javascript
// Example: Stripe Checkout Session
const session = await stripe.checkout.sessions.create({
  payment_method_types: ['card'],
  line_items: [{ price: 'price_xxx', quantity: 1 }],
  mode: 'payment',
  success_url: 'https://example.com/success',
  cancel_url: 'https://example.com/cancel'
});
```

### Webhook Handling

Reliable event processing with idempotency.

```javascript
// Example: Stripe Webhook Handler
app.post('/webhooks/stripe', express.raw({ type: 'application/json' }), (req, res) => {
  const sig = req.headers['stripe-signature'];
  const event = stripe.webhooks.constructEvent(req.body, sig, webhookSecret);

  // Idempotent handling
  if (await isProcessed(event.id)) {
    return res.json({ received: true });
  }

  // Process event
  await handleEvent(event);
  res.json({ received: true });
});
```

## Compliance Checklist

Before going live, ensure:

- [ ] **PCI Compliance**: SAQ completed, no card data stored
- [ ] **Tokenization**: All card data tokenized via gateway
- [ ] **HTTPS Only**: All endpoints use TLS 1.2+
- [ ] **Webhook Security**: Signature verification implemented
- [ ] **Idempotency**: Duplicate transaction prevention
- [ ] **Error Handling**: User-friendly messages, no data leaks
- [ ] **Logging**: Comprehensive audit trail (no sensitive data)
- [ ] **Monitoring**: Alerts for failures, fraud, anomalies
- [ ] **Testing**: Sandbox tested, load tested
- [ ] **Documentation**: Runbooks, incident response plans

## Common Use Cases

### E-commerce Checkout

Integrate payment processing for online store.

**Key Requirements**:
- Shopping cart integration
- Multiple payment methods
- Guest checkout support
- Order confirmation emails
- Inventory synchronization

### Subscription Service

Implement recurring billing for SaaS.

**Key Requirements**:
- Plan management (free, starter, pro, enterprise)
- Trial periods (7, 14, 30 days)
- Proration on upgrades/downgrades
- Dunning for failed payments
- Customer portal for self-service

### Marketplace Platform

Handle multi-party payments.

**Key Requirements**:
- Split payments (platform fee + vendor)
- Escrow or delayed payout
- Vendor onboarding (KYC)
- Commission management
- Multi-currency support

### Mobile App Payments

Native payment experience.

**Key Requirements**:
- Apple Pay / Google Pay
- Mobile SDK integration
- Biometric authentication
- Offline payment queuing
- Receipt generation

## Best Practices

### Security First

- Never log or store raw card data
- Use tokenization for all card references
- Implement proper access controls (RBAC)
- Enable MFA for admin access
- Regular security audits and penetration testing

### Reliability

- Implement idempotency keys
- Use exponential backoff for retries
- Handle network timeouts gracefully
- Maintain fallback payment methods
- Monitor success rates continuously

### User Experience

- Minimize checkout steps (one-page ideal)
- Provide clear error messages
- Support multiple payment methods
- Auto-save cart state
- Mobile-responsive design

### Monitoring

- Track payment success rate (target: >99%)
- Monitor processing latency (target: <3s)
- Alert on fraud patterns
- Dashboard for real-time metrics
- Weekly reconciliation reports

## Collaboration

This agent works seamlessly with:

- **security-auditor**: Compliance verification, penetration testing
- **backend-developer**: API integration, webhook implementation
- **frontend-developer**: Checkout UI, payment forms
- **fintech-engineer**: Financial flows, reconciliation
- **devops-engineer**: Infrastructure, monitoring, scaling
- **qa-expert**: Test scenarios, regression testing

## Support & Resources

### Documentation

- [Stripe API Docs](https://stripe.com/docs/api)
- [PCI DSS Requirements](https://www.pcisecuritystandards.org/)
- [Payment Card Industry Data Security Standard](https://listings.pcisecuritystandards.org/)

### Community

- [Stripe Developer Forums](https://support.stripe.com/)
- [Payment Gateway Comparison](https://www.merchantmaverick.com/)

### Tools

- Stripe CLI for webhook testing
- Postman collections for API testing
- ngrok for local webhook development

## License

This agent is part of the Claude Code Agent Marketplace and follows the repository's license terms.

## Contributing

Contributions welcome! Please submit issues and pull requests to improve payment integration capabilities.
