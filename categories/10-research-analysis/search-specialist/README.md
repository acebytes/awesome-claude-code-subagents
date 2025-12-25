# Search Specialist Agent

Expert search specialist mastering advanced information retrieval, query optimization, and knowledge discovery. Specializes in finding needle-in-haystack information across diverse sources with focus on precision, comprehensiveness, and efficiency.

## Overview

The Search Specialist agent is a senior-level information retrieval expert that excels at designing search strategies, optimizing queries, and curating high-quality results from diverse sources. Whether you need academic research, competitive intelligence, or specialized domain knowledge, this agent delivers precise, relevant information efficiently.

## Key Capabilities

- **Advanced Query Optimization**: Boolean operators, proximity searches, wildcards, and field-specific queries
- **Multi-Source Search**: Web search engines, academic databases, patent databases, legal repositories, government sources
- **Quality Curation**: Relevance filtering, duplicate removal, quality ranking, and result synthesis
- **Semantic Search**: Natural language queries, citation tracking, cross-reference mining
- **Domain Expertise**: Scientific literature, technical specifications, legal precedents, medical research, financial data

## Slash Commands

### `/deep-search`
Execute comprehensive multi-source deep search with iterative refinement.

```bash
/deep-search <topic> [source_constraints] [quality_criteria]
```

**Examples:**
```bash
/deep-search "quantum computing error correction" academic peer-reviewed
/deep-search "GDPR compliance requirements" legal authoritative
/deep-search "machine learning transformers" technical high-impact
```

### `/source-find`
Identify and evaluate authoritative sources for specific domain.

```bash
/source-find <domain> [source_type] [reputation_level]
```

**Examples:**
```bash
/source-find "medical research" journals high-impact
/source-find "legal precedents" case-law federal
/source-find "market intelligence" industry-reports trusted
```

### `/fact-check`
Verify information accuracy across multiple authoritative sources.

```bash
/fact-check <claim> [verification_depth] [source_count]
```

**Examples:**
```bash
/fact-check "AI model performance benchmarks" comprehensive 10
/fact-check "regulatory changes 2024" thorough authoritative
/fact-check "industry statistics" deep cross-referenced
```

### `/search-strategy`
Design comprehensive search strategy for complex information needs.

```bash
/search-strategy <objectives> [constraints] [timeline]
```

**Examples:**
```bash
/search-strategy "competitive landscape analysis" public-sources 2-weeks
/search-strategy "literature review systematic" academic-only 1-month
/search-strategy "patent landscape mapping" USPTO comprehensive
```

## MCP Servers

The agent uses the following MCP servers:

- **filesystem**: Access local files and directories for document analysis
- **memory**: Store and retrieve search patterns, source preferences, and query history
- **fetch**: Retrieve web content and API data from external sources

## Use Cases

### Academic Research
```bash
/deep-search "CRISPR gene editing recent advances" academic 2023-2024
```
Conducts systematic literature review across academic databases, filters for peer-reviewed sources, and delivers categorized results with citation tracking.

### Competitive Intelligence
```bash
/search-strategy "competitor product analysis" public-sources comprehensive
```
Designs multi-phase search strategy covering company websites, press releases, patents, social media, and industry reports.

### Legal Research
```bash
/source-find "intellectual property case law" federal high-authority
```
Identifies authoritative legal databases, evaluates source credibility, and provides access paths to relevant precedents.

### Technical Documentation
```bash
/fact-check "API deprecation timeline" comprehensive official-sources
```
Verifies technical claims across official documentation, release notes, developer forums, and version control history.

### Market Research
```bash
/deep-search "electric vehicle market trends 2024" industry comprehensive
```
Aggregates market reports, industry analyses, government data, and news sources to provide comprehensive market intelligence.

## Workflow

### 1. Search Planning
- Clarify objectives and requirements
- Identify optimal sources
- Develop comprehensive query strategy
- Set quality criteria and success metrics

### 2. Implementation
- Execute systematic searches
- Refine queries iteratively
- Filter and validate results
- Curate high-quality findings

### 3. Delivery
- Synthesize results
- Remove duplicates
- Rank by relevance
- Generate comprehensive reports

## Performance Metrics

The Search Specialist maintains excellence through:

- **Precision Rate**: > 90% relevance in results
- **Coverage**: Comprehensive source coverage
- **Efficiency**: Optimized search workflows
- **Quality**: Authoritative, verified sources

## Integration

Works seamlessly with other agents:

- **research-analyst**: Comprehensive research projects
- **data-researcher**: Data discovery and validation
- **market-researcher**: Market intelligence gathering
- **competitive-analyst**: Competitor intelligence
- **knowledge-synthesizer**: Information synthesis

## Best Practices

1. **Be Specific**: Provide clear search objectives and quality criteria
2. **Define Scope**: Specify source types, date ranges, and authority levels
3. **Iterate**: Refine searches based on initial results
4. **Verify**: Cross-reference critical information across multiple sources
5. **Document**: Maintain search strategies for reproducibility

## Example Session

```bash
# Start with strategy design
/search-strategy "AI safety research trends" academic-industry 2-weeks

# Execute deep search
/deep-search "AI alignment techniques" peer-reviewed high-impact

# Find authoritative sources
/source-find "AI safety research" academic top-tier

# Verify specific claims
/fact-check "current AI capability benchmarks" comprehensive 15

# Results: 147 queries executed, 43 sources searched, 2.3K results found, 94% precision
```

## Configuration

The agent's behavior can be customized through context queries:

```json
{
  "search_objectives": "comprehensive literature review",
  "quality_requirements": "peer-reviewed, high-impact",
  "source_preferences": ["academic databases", "conference proceedings"],
  "time_constraints": "2 weeks",
  "coverage_expectations": "exhaustive"
}
```

## License

MIT License - See LICENSE file for details

## Author

Claude Code Marketplace

## Version

1.0.0
