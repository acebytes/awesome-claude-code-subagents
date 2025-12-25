# Prompt Engineer Agent

Expert prompt engineer specializing in designing, optimizing, and managing prompts for large language models. Masters prompt architecture, evaluation frameworks, and production prompt systems with focus on reliability, efficiency, and measurable outcomes.

## Overview

The Prompt Engineer agent is your comprehensive partner for creating, testing, and optimizing prompts for LLM applications. From initial design through A/B testing to production deployment, this agent ensures your prompts are accurate, efficient, cost-effective, and safe.

## Key Capabilities

### Prompt Design Patterns
- Zero-shot and few-shot prompting
- Chain-of-thought reasoning
- Tree-of-thought exploration
- ReAct (Reasoning + Acting) pattern
- Constitutional AI approaches
- Role-based prompting
- Instruction following optimization
- Template architecture design

### Evaluation Frameworks
- Accuracy metrics and benchmarking
- Consistency testing across variations
- Edge case validation
- A/B test design and analysis
- Statistical significance testing
- Cost-benefit analysis
- User satisfaction metrics
- Business impact measurement

### Token Optimization
- Context compression techniques
- Instruction efficiency improvements
- Output format optimization
- Example selection and ordering
- Dynamic few-shot learning
- Caching strategies
- Batch processing optimization
- Cost tracking and reduction

### Production Systems
- Prompt version management
- Deployment workflows
- Performance monitoring
- Cost allocation and tracking
- Incident response procedures
- Safety and compliance checks
- Team collaboration tools
- Documentation standards

### Safety Mechanisms
- Input validation and filtering
- Output safety checks
- Bias detection and mitigation
- Harmful content prevention
- Privacy protection measures
- Injection attack defense
- Audit logging
- Compliance verification

## MCP Integration

This agent leverages four powerful MCP servers:

### filesystem
- Read/write prompt templates and configurations
- Manage prompt catalogs and libraries
- Store evaluation test sets and results
- Save performance metrics and reports
- Organize prompt versions
- Handle A/B test configurations

### github
- Version control for prompt templates
- Collaborate on prompt development
- Track prompt iterations and changes
- Manage issues for improvements
- Review pull requests for updates
- Share prompt libraries across teams

### context7
- Semantic search for existing prompt patterns
- Find similar prompt implementations
- Locate prompt optimization examples
- Discover evaluation frameworks
- Search for few-shot examples
- Find safety filter implementations

### fetch
- Call LLM APIs for prompt testing
- Execute A/B test comparisons
- Fetch evaluation metrics from services
- Access prompt management platforms
- Query cost tracking APIs
- Integrate with monitoring dashboards

## Slash Commands

### /prompt-design - Design Optimized Prompt Template

Design effective, optimized prompt templates based on use case requirements and constraints.

```bash
/prompt-design [use-case] [requirements]
```

**Example:**
```bash
/prompt-design customer-support "empathetic, accurate, <500 tokens, handles complaints"
```

**What it does:**
1. Analyzes use case and requirements
2. Selects appropriate prompt patterns
3. Designs template structure
4. Selects relevant examples
5. Optimizes context usage
6. Validates safety considerations
7. Tests performance
8. Documents the prompt

### /prompt-evaluate - Evaluate Prompt Quality

Comprehensive evaluation of prompt performance across multiple metrics and test cases.

```bash
/prompt-evaluate [prompt-path] [test-set] [metrics]
```

**Example:**
```bash
/prompt-evaluate ./prompts/classifier.txt ./tests/100-samples.json "accuracy,consistency,latency"
```

**What it does:**
1. Loads prompt and test set
2. Establishes baseline performance
3. Tests accuracy on samples
4. Validates consistency
5. Tests edge cases
6. Performs statistical analysis
7. Generates performance report
8. Provides improvement recommendations

### /prompt-optimize - Optimize Prompt Efficiency

Optimize existing prompts to reduce token usage and costs while maintaining or improving quality.

```bash
/prompt-optimize [prompt-path] [optimization-target]
```

**Example:**
```bash
/prompt-optimize ./prompts/summarizer.txt "reduce-tokens-30%"
```

**What it does:**
1. Analyzes current performance
2. Profiles token usage
3. Applies compression techniques
4. Prunes unnecessary context
5. Refines instructions
6. Tests optimized version
7. Performs cost-benefit analysis
8. Validates quality maintained

## Prompt Patterns

### Zero-shot Prompting
Direct instruction without examples for simple, well-defined tasks.

```
Task: Classify the sentiment of the following text as positive, negative, or neutral.
Text: [input]
Sentiment:
```

### Few-shot Learning
Include examples to guide the model's understanding and output format.

```
Classify product reviews as positive, negative, or neutral.

Review: "Great product, works perfectly!"
Sentiment: positive

Review: "Terrible quality, broke after one use."
Sentiment: negative

Review: "It's okay, nothing special."
Sentiment: neutral

Review: [input]
Sentiment:
```

### Chain-of-thought
Break down complex reasoning into steps.

```
Solve the following problem step by step:

Problem: [complex question]

Let's approach this systematically:
1. First, let's identify...
2. Next, we need to...
3. Then, we calculate...
4. Finally, the answer is...
```

### ReAct Pattern
Combine reasoning with actions for complex workflows.

```
Task: [goal]

Thought: What do I need to do first?
Action: [action to take]
Observation: [result]
Thought: Based on this, what's next?
Action: [next action]
...
Answer: [final result]
```

## Typical Workflows

### 1. Design New Prompt from Scratch

```bash
# Design a prompt for a specific use case
/prompt-design email-classifier "categorize support emails, 5 categories, <300 tokens"

# Agent will:
# - Analyze the requirements
# - Select few-shot pattern (5 categories suggests examples needed)
# - Create template with clear instructions
# - Select diverse examples for each category
# - Optimize token usage
# - Add error handling
# - Test on edge cases
# - Save versioned prompt
```

### 2. Evaluate Existing Prompt

```bash
# Evaluate prompt performance
/prompt-evaluate ./prompts/email-classifier.txt ./tests/email-samples.json "accuracy,consistency,cost"

# Agent will:
# - Load prompt and 100+ test cases
# - Run evaluation against LLM API
# - Measure accuracy (% correct classifications)
# - Test consistency (same inputs = same outputs)
# - Calculate cost (tokens used * pricing)
# - Generate detailed report
# - Identify failure patterns
# - Suggest improvements
```

### 3. Optimize for Efficiency

```bash
# Reduce token usage while maintaining quality
/prompt-optimize ./prompts/email-classifier.txt "reduce-tokens-40%"

# Agent will:
# - Analyze current prompt (650 tokens)
# - Compress instructions (redundancy removal)
# - Optimize examples (most informative ones)
# - Reduce context (essential info only)
# - Test optimized version (390 tokens)
# - Validate accuracy maintained
# - Calculate cost savings ($847/month)
# - Document optimization techniques
```

### 4. A/B Test Variations

The agent automatically conducts A/B tests to compare prompt variations:

```
Variation A (original): 650 tokens, 89% accuracy
Variation B (optimized): 390 tokens, 91% accuracy
Variation C (chain-of-thought): 580 tokens, 94% accuracy

Statistical analysis (n=500):
- Variation C significantly better (p<0.01)
- 40% reduction in tokens vs. A
- 5% improvement in accuracy
- $623/month cost savings

Recommendation: Deploy Variation C
```

## Performance Standards

The Prompt Engineer agent ensures:

- **Accuracy**: >90% on validation sets
- **Token Reduction**: >30% through optimization
- **Latency**: <2s response time
- **Cost Reduction**: >40% through efficiency gains
- **Consistency**: >95% same outputs for same inputs
- **Safety**: Zero harmful outputs in testing

## Evaluation Metrics

### Accuracy Metrics
- Exact match accuracy
- Semantic similarity scores
- Task-specific metrics (F1, precision, recall)
- Human evaluation alignment

### Efficiency Metrics
- Token usage per query
- Average response latency
- Cost per query
- Throughput (queries per second)

### Quality Metrics
- Consistency score
- Edge case handling
- Output format compliance
- Instruction following rate

### Safety Metrics
- Harmful content rate
- Bias scores across demographics
- Privacy violation rate
- Injection attack success rate

## Optimization Techniques

### Token Reduction
1. **Instruction compression**: Remove redundant words
2. **Context pruning**: Keep only essential information
3. **Example optimization**: Select most informative examples
4. **Format efficiency**: Use concise output formats

### Context Compression
1. **Summarization**: Compress long contexts
2. **Entity extraction**: Focus on key information
3. **Deduplication**: Remove repeated information
4. **Hierarchical structure**: Organize efficiently

### Caching Strategies
1. **Prompt caching**: Reuse static prompt parts
2. **Example caching**: Store common examples
3. **Response caching**: Cache frequent queries
4. **Batch processing**: Combine similar requests

## Safety and Compliance

### Input Validation
- Length limits enforcement
- Format verification
- Malicious content detection
- PII detection and masking

### Output Filtering
- Harmful content detection
- Bias identification
- Privacy violation checks
- Quality assurance gates

### Audit and Compliance
- Complete request logging
- Performance tracking
- Safety incident recording
- Compliance reporting

## Best Practices

### Prompt Design
1. Start with clear, specific instructions
2. Use appropriate patterns for the task
3. Provide diverse, high-quality examples
4. Specify exact output format
5. Handle edge cases explicitly
6. Test thoroughly before deployment
7. Version control all prompts
8. Document design decisions

### Optimization
1. Measure current performance first
2. Set clear optimization targets
3. Test one change at a time
4. Validate quality maintained
5. Calculate cost-benefit ratio
6. Monitor production impact
7. Iterate based on data
8. Document optimization techniques

### Evaluation
1. Create diverse test sets (>100 samples)
2. Include edge cases and failures
3. Use multiple metrics
4. Establish statistical significance
5. Track performance over time
6. Compare to baselines
7. Conduct regular A/B tests
8. Document all results

### Production Management
1. Implement gradual rollout
2. Monitor key metrics continuously
3. Set up alerts for anomalies
4. Maintain version history
5. Have rollback procedures
6. Document all changes
7. Review performance regularly
8. Keep prompt library organized

## Setup

### Prerequisites
- Node.js 18+ for MCP servers
- Access to LLM APIs (OpenAI, Anthropic, etc.)
- Git for version control

### Installation

1. Clone the agent directory:
```bash
cd claude-code-agent-marketplace/categories/05-data-ai/prompt-engineer
```

2. Configure MCP servers (see mcp-config.json)

3. Set up optional environment variables:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=your_token_here
```

### Configuration

The agent uses `mcp-config.json` for MCP server configuration. Customize based on your needs:

- **filesystem**: Configure allowed directories for prompts
- **github**: Set GitHub token for repository access
- **context7**: Configure for your codebase
- **fetch**: Add LLM API endpoints and credentials

## Integration with Other Agents

The Prompt Engineer agent collaborates with:

- **llm-architect**: System design and architecture
- **ai-engineer**: LLM integration and deployment
- **data-scientist**: Evaluation methodology
- **nlp-engineer**: Language-specific optimization
- **qa-expert**: Testing and validation
- **product-manager**: Requirements and metrics
- **content-writer**: Tone and style guidance
- **security-auditor**: Safety and compliance

## Example Use Cases

### Customer Support
- Intent classification
- Sentiment analysis
- Response generation
- Escalation routing
- FAQ answering

### Content Generation
- Product descriptions
- Marketing copy
- Email drafting
- Social media posts
- Documentation

### Data Processing
- Text classification
- Entity extraction
- Summarization
- Translation
- Data transformation

### Code Assistance
- Code generation
- Code explanation
- Bug detection
- Documentation generation
- Code review

### Research and Analysis
- Document analysis
- Literature review
- Data synthesis
- Report generation
- Insight extraction

## Quality Checklist

Before production deployment, the agent ensures:

- [ ] Accuracy > 90% on validation set
- [ ] Token usage optimized (>30% reduction)
- [ ] Latency < 2s for typical requests
- [ ] Cost per query tracked and acceptable
- [ ] Safety filters validated
- [ ] Version controlled in repository
- [ ] Monitoring and alerts configured
- [ ] Complete documentation
- [ ] Team training completed
- [ ] Rollback procedure tested

## Cost Optimization

### Token Usage Tracking
- Track tokens per query
- Monitor trends over time
- Identify high-cost queries
- Optimize outliers

### Cost Reduction Strategies
1. Compress instructions (10-20% savings)
2. Optimize examples (15-25% savings)
3. Implement caching (20-40% savings)
4. Batch similar requests (10-15% savings)
5. Use appropriate models (30-50% savings)

### ROI Calculation
```
Monthly queries: 100,000
Before optimization: 650 tokens/query
After optimization: 390 tokens/query
Token reduction: 40%
Cost savings: $1,247/month
Annual savings: $14,964
```

## Monitoring and Analytics

### Real-time Metrics
- Query volume and trends
- Average response time
- Token usage per query
- Error rates
- Cost per query

### Performance Dashboards
- Accuracy trends over time
- Consistency scores
- Token usage patterns
- Cost allocation by use case
- A/B test results

### Alerting
- Accuracy drops below threshold
- Latency exceeds targets
- Cost spikes detected
- Safety violations
- Unusual patterns

## Support and Resources

### Documentation
- See CLAUDE.md for detailed agent instructions
- Review agent-manifest.json for complete capabilities
- Check mcp-config.json for MCP server setup

### Prompt Libraries
- LangChain prompt templates
- OpenAI prompt examples
- Anthropic prompt engineering guide
- Community prompt repositories

### Tools and Platforms
- LangChain for prompt management
- PromptFlow for evaluation
- Weights & Biases for tracking
- Custom evaluation frameworks

## Contributing

To enhance the Prompt Engineer agent:

1. Add new prompt patterns
2. Implement additional evaluation metrics
3. Enhance optimization techniques
4. Add support for new LLM platforms
5. Improve safety mechanisms
6. Document best practices
7. Share successful prompts
8. Contribute evaluation datasets

## License

Part of the Claude Code Agent Marketplace. See repository root for license information.

---

**Remember**: Always prioritize effectiveness, efficiency, and safety while building prompt systems that deliver consistent value through well-designed, thoroughly tested, and continuously optimized prompts.
