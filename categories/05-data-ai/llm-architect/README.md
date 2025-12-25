# LLM Architect Agent

Expert LLM architect specializing in large language model architecture, deployment, and optimization. Masters LLM system design, fine-tuning strategies, and production serving with focus on building scalable, efficient, and safe LLM applications.

## Overview

The LLM Architect agent is a specialized expert in designing, implementing, and optimizing large language model systems for production use. It brings deep expertise in model selection, fine-tuning strategies, RAG implementation, inference optimization, and safety mechanisms to help you build scalable and cost-effective LLM applications.

## Key Capabilities

### LLM System Architecture
- Design complete LLM system architectures
- Select appropriate models (open-source vs API)
- Design serving infrastructure
- Plan scaling strategies
- Calculate cost projections

### Fine-tuning Strategies
- Implement LoRA/QLoRA fine-tuning
- Prepare and validate datasets
- Configure training infrastructure
- Optimize hyperparameters
- Merge and deploy fine-tuned models

### RAG Implementation
- Build document processing pipelines
- Select and configure vector stores
- Optimize retrieval strategies
- Implement hybrid search and reranking
- Design context management systems

### Inference Optimization
- Apply quantization (4-bit, 8-bit)
- Optimize KV cache usage
- Configure continuous batching
- Implement prompt caching
- Enable speculative decoding

### Safety & Compliance
- Implement content filters
- Detect prompt injections
- Monitor for hallucinations
- Ensure bias mitigation
- Maintain audit logs

### Cost Optimization
- Optimize token usage
- Implement caching strategies
- Right-size model selection
- Monitor and control spending
- Batch processing optimization

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read, write, and navigate the file system for LLM code and configurations
- **github**: Access repositories, issues, PRs for collaboration on LLM projects
- **context7**: Semantic code search across LLM implementations
- **fetch**: Call external APIs for LLM serving, monitoring, and AI services

## Slash Commands

### /llm-design
Design complete LLM system architecture including model selection, serving infrastructure, fine-tuning strategy, and deployment plan.

**Usage:**
```
/llm-design [use-case] [requirements]
```

**Example:**
```
/llm-design customer-support "multi-language, <500ms response, 1000 qps, safety critical"
```

**Output:**
- Model selection recommendation
- Serving infrastructure design
- Fine-tuning or RAG approach
- Safety mechanisms plan
- Cost projections
- Scaling strategy

### /llm-optimize
Optimize LLM inference for production including quantization, caching, batching, and cost reduction.

**Usage:**
```
/llm-optimize [model-path] [targets]
```

**Example:**
```
/llm-optimize ./models/llama-7b "latency<200ms, cost-50%, throughput+100%"
```

**Output:**
- Performance benchmarks
- Quantization recommendations
- Caching configuration
- Batching setup
- Cost reduction analysis
- Optimized deployment config

### /llm-finetune
Plan and implement LLM fine-tuning using LoRA/QLoRA for task-specific optimization.

**Usage:**
```
/llm-finetune [base-model] [task] [dataset-path]
```

**Example:**
```
/llm-finetune llama-2-7b "legal-document-analysis" ./data/legal-corpus
```

**Output:**
- Dataset preparation pipeline
- LoRA/QLoRA configuration
- Training infrastructure setup
- Hyperparameter recommendations
- Evaluation metrics
- Deployment plan

## Technical Expertise

### Frameworks & Tools
- **Serving**: vLLM, TGI, Triton Inference Server
- **Training**: Transformers, PEFT (LoRA/QLoRA), Axolotl, DeepSpeed
- **RAG**: LangChain, LlamaIndex
- **Vector Stores**: Pinecone, Weaviate, Qdrant, ChromaDB

### Optimization Techniques
- Quantization (4-bit, 8-bit)
- LoRA/QLoRA fine-tuning
- Flash Attention
- Tensor & pipeline parallelism
- KV cache optimization
- Speculative decoding
- Continuous batching

### Performance Targets
- Inference latency: <200ms P95
- Throughput: >100 tokens/s
- Cost per token: <$0.0001
- Safety score: >95%
- Cache hit rate: >60%

## Workflows

### 1. LLM Architecture Design
1. Analyze requirements and use cases
2. Select appropriate model (open-source vs API)
3. Design serving infrastructure
4. Determine fine-tuning vs RAG approach
5. Plan safety mechanisms
6. Set up monitoring and logging
7. Calculate cost projections
8. Define scaling strategies

### 2. Fine-tuning Implementation
1. Prepare and validate dataset
2. Configure LoRA/QLoRA parameters
3. Set up training infrastructure
4. Execute hyperparameter tuning
5. Train and validate model
6. Merge adapter weights
7. Deploy fine-tuned model
8. Benchmark against base model

### 3. RAG System Development
1. Build document processing pipeline
2. Select embedding model
3. Configure vector store
4. Optimize retrieval strategy
5. Implement reranking
6. Design context management
7. Add caching layer
8. Validate end-to-end performance

### 4. Inference Optimization
1. Benchmark current performance
2. Apply quantization
3. Optimize KV cache
4. Configure continuous batching
5. Implement prompt caching
6. Enable speculative decoding
7. Optimize token usage
8. Validate and deploy

## Best Practices

### Architecture
- Start with smallest viable model
- Benchmark thoroughly before scaling
- Implement proper caching
- Use batching effectively
- Monitor costs continuously
- Plan for failures
- Test safety thoroughly

### Fine-tuning
- Curate high-quality datasets
- Use LoRA for efficiency
- Validate rigorously
- Prevent overfitting
- Track experiment metrics
- Compare against baselines

### RAG Systems
- Optimize embedding models
- Choose appropriate vector stores
- Implement hybrid search
- Add reranking
- Cache frequently accessed docs
- Monitor retrieval quality

### Safety
- Implement content filters
- Detect prompt injections
- Validate outputs
- Monitor for hallucinations
- Test bias thoroughly
- Protect user privacy
- Maintain audit logs

## Integration with Other Agents

The LLM Architect agent collaborates with:

- **ai-engineer**: Model integration and deployment
- **prompt-engineer**: Prompt optimization and engineering
- **ml-engineer**: Training and deployment infrastructure
- **data-engineer**: Data pipelines for fine-tuning
- **nlp-engineer**: Language-specific optimizations
- **backend-developer**: API design and integration
- **cloud-architect**: Infrastructure and scaling
- **security-auditor**: Safety and compliance validation

## Quality Standards

Every LLM system delivered includes:

- Inference latency < 200ms P95
- Throughput > 100 tokens/s
- Efficient context window utilization
- Safety filters enabled
- Cost per token optimized
- Comprehensive accuracy benchmarks
- Full monitoring configuration
- Scaling validation
- Complete documentation
- Team training materials

## Example Use Cases

### Customer Support Chatbot
Design and deploy a multi-language customer support LLM with <500ms response time, safety filters, and cost optimization.

### Document Analysis System
Build a RAG-based document analysis system with fine-tuned retrieval, reranking, and domain-specific LLM.

### Code Generation Assistant
Implement a code generation system with fine-tuned models, context optimization, and multi-language support.

### Content Moderation
Deploy a safety-critical content moderation system with low latency, high accuracy, and comprehensive audit logging.

## Getting Started

1. **Install the agent** following the marketplace installation guide
2. **Configure MCP servers** in your environment
3. **Set up GITHUB_PERSONAL_ACCESS_TOKEN** (optional) for GitHub integration
4. **Invoke the agent** with your LLM requirements
5. **Use slash commands** for specific tasks

## Learn More

For detailed documentation on LLM architecture patterns, fine-tuning strategies, RAG implementation, and production deployment, see the [CLAUDE.md](./CLAUDE.md) file.

## Support

For issues, questions, or contributions, please visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).
