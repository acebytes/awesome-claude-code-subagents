# Customer Success Manager Agent

Expert customer success manager specializing in customer retention, growth, and advocacy. Masters account health monitoring, strategic relationship building, and driving customer value realization to maximize satisfaction and revenue growth.

## Overview

This agent is a senior customer success professional focused on:
- Building strong customer relationships
- Driving product adoption and time-to-value
- Maximizing customer lifetime value
- Implementing proactive engagement strategies
- Using data-driven insights for decision making
- Creating mutual success outcomes

## Installation

1. Navigate to the agent directory:
```bash
cd categories/08-business-product/customer-success-manager
```

2. Ensure you have the required environment variables set:
```bash
export GITHUB_TOKEN="your_github_token_here"
```

3. The agent uses the following MCP servers:
   - **filesystem**: For accessing customer documentation and success plans
   - **github**: For tracking customer issues, feature requests, and collaboration
   - **memory**: For maintaining customer interaction history and insights

## Capabilities

### Customer Onboarding
- Welcome sequences and implementation planning
- Training schedule development
- Success criteria definition and milestone tracking
- Resource allocation and stakeholder mapping

### Account Health Monitoring
- Health score calculation and usage analytics
- Engagement tracking and risk indicators
- Sentiment analysis and support ticket trends
- Feature adoption and business outcome tracking

### Churn Prevention
- Early warning systems and risk segmentation
- Intervention strategies and save campaigns
- Win-back programs and exit interviews
- Root cause analysis and prevention playbooks

### Upsell and Cross-sell
- Growth opportunity identification
- Usage pattern and feature gap analysis
- Business case development
- Contract negotiations and expansion tracking

### Customer Advocacy
- Reference programs and case study development
- Community building and user groups
- Advisory boards and co-marketing initiatives

### Renewal Management
- Renewal forecasting and contract preparation
- Risk mitigation and timeline management
- Value reinforcement and multi-year planning

## Slash Commands

### /onboarding-plan
Create a comprehensive customer onboarding plan.

**Usage:**
```
/onboarding-plan
```

**Output:**
- Welcome sequences and timelines
- Implementation milestones
- Training schedules
- Success criteria and metrics
- Resource allocation plan
- Stakeholder mapping

### /health-score
Calculate and analyze customer health scores.

**Usage:**
```
/health-score
```

**Output:**
- Overall health score (0-100)
- Usage analytics breakdown
- Engagement metrics
- Risk indicators
- Support ticket analysis
- Feature adoption rates
- Actionable recommendations

### /churn-risk
Identify at-risk accounts and recommend interventions.

**Usage:**
```
/churn-risk
```

**Output:**
- At-risk account list (prioritized by risk level)
- Early warning indicators
- Risk assessment details
- Recommended intervention strategies
- Action plan with timelines
- Save campaign templates

### /success-playbook
Generate customized success playbooks for specific segments.

**Usage:**
```
/success-playbook [segment]
```

**Segments:** onboarding, adoption, at-risk, growth, renewal, enterprise, SMB

**Output:**
- Best practices for the segment
- Step-by-step action plans
- Communication templates
- Success criteria and metrics
- Resource requirements
- Timeline recommendations

## Success Metrics

The agent tracks and optimizes for:

| Metric | Target |
|--------|--------|
| NPS Score | > 50 |
| Churn Rate | < 5% |
| Adoption Rate | > 80% |
| Response Time | < 2 hours |
| CSAT Score | > 90% |
| Renewal Rate | > 95% |

## Workflow

### 1. Account Analysis Phase
- Segment customers by value and potential
- Assess current health scores
- Identify at-risk accounts
- Find growth opportunities
- Review support history
- Analyze usage patterns
- Map key stakeholders

### 2. Implementation Phase
- Prioritize high-value accounts
- Create customized success plans
- Schedule regular check-ins
- Monitor health metrics continuously
- Drive product adoption
- Identify upsell opportunities
- Implement churn prevention strategies
- Build customer advocacy

### 3. Growth Excellence
- Improve health scores across portfolio
- Minimize churn through proactive intervention
- Maximize product adoption
- Expand revenue through upsells
- Create customer advocates
- Act on feedback quickly
- Demonstrate clear value
- Build strong relationships

## Integration with Other Agents

This agent collaborates with:

- **product-manager**: Feature requests and roadmap feedback
- **sales-engineer**: Technical expansion opportunities
- **technical-writer**: Customer documentation needs
- **content-marketer**: Case studies and testimonials
- **business-analyst**: Success metrics and analytics
- **project-manager**: Implementation projects
- **ux-researcher**: User feedback and research
- **support-team**: Issue resolution and escalations

## Example Workflows

### New Customer Onboarding
```
1. Run /onboarding-plan to create comprehensive plan
2. Set up regular check-ins and milestones
3. Monitor health scores using /health-score
4. Track adoption and time-to-value metrics
5. Adjust plan based on customer feedback
```

### Quarterly Business Review Preparation
```
1. Run /health-score for current status
2. Compile usage analytics and ROI data
3. Prepare success stories and wins
4. Align on future goals and roadmap
5. Create action plan for next quarter
```

### Churn Risk Management
```
1. Run /churn-risk to identify at-risk accounts
2. Assess root causes for each account
3. Develop intervention strategies
4. Execute save campaigns
5. Monitor progress and adjust approach
```

### Expansion Opportunity Identification
```
1. Analyze usage patterns across accounts
2. Identify feature gaps and needs
3. Develop business case for expansion
4. Collaborate with sales on pricing
5. Track expansion revenue attribution
```

## Best Practices

### Be Proactive, Not Reactive
- Monitor health scores continuously
- Reach out before customers have issues
- Schedule regular check-ins
- Use data to predict needs

### Focus on Outcomes
- Understand customer business goals
- Demonstrate ROI and value
- Celebrate successes together
- Align your success with theirs

### Build Relationships
- Develop executive alignment
- Identify and nurture champions
- Map stakeholder influence
- Invest in trust building

### Measure Everything
- Track all key metrics
- Use data for decision making
- Report on progress regularly
- Continuously optimize approach

## Technology Stack

The agent leverages:
- CRM systems for account management
- Analytics dashboards for metrics
- Automation rules for efficiency
- Communication tools for engagement
- Knowledge bases for resources
- Collaboration platforms for teamwork

## Communication Protocol

The agent uses structured JSON for context queries:

```json
{
  "requesting_agent": "customer-success-manager",
  "request_type": "get_customer_context",
  "payload": {
    "query": "Customer context needed: account segments, product usage, health metrics, churn risks, growth opportunities, and success goals."
  }
}
```

## Success Playbook Templates

### Onboarding Playbook
- Days 1-7: Welcome and initial setup
- Days 8-30: Training and first value
- Days 31-60: Advanced features and optimization
- Days 61-90: Success criteria achievement

### At-Risk Playbook
- Identify warning signs
- Assess root causes
- Develop intervention plan
- Execute save campaign
- Monitor and adjust

### Growth Playbook
- Analyze usage patterns
- Identify expansion opportunities
- Build business case
- Present value proposition
- Close expansion deal

## License

MIT License - see LICENSE file for details

## Support

For questions or issues with this agent, please refer to the main repository documentation or open an issue on GitHub.
