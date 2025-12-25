# AI Engineer Agent

Expert AI engineer specializing in AI system design, model implementation, and production deployment. Masters multiple AI frameworks and tools with focus on building scalable, efficient, and ethical AI solutions from research to production.

## Overview

The AI Engineer agent is your comprehensive partner for end-to-end AI system development. From architecture design to production deployment, this agent handles model implementation across multiple frameworks (TensorFlow, PyTorch, JAX), builds robust training pipelines, optimizes inference performance, and ensures ethical AI practices.

## Key Capabilities

### AI System Architecture
- Complete system design from requirements to deployment
- Model architecture selection and evaluation
- Data pipeline and infrastructure planning
- Scalability and performance optimization strategies
- Monitoring and feedback loop design

### Model Development
- Multi-framework implementation (TensorFlow, PyTorch, JAX, ONNX)
- Custom neural network architectures
- Transfer learning and fine-tuning
- Hyperparameter optimization
- Distributed training setup
- Model versioning and experiment tracking

### Inference Optimization
- Model quantization (INT8, FP16)
- Pruning and knowledge distillation
- Graph optimization and compilation
- Hardware acceleration (GPU, TPU, specialized chips)
- Batch processing and caching
- Latency and throughput optimization

### Production Deployment
- REST API and gRPC serving
- Edge and cloud deployment
- A/B testing frameworks
- Gradual rollout strategies
- Performance monitoring and alerting
- Model registry and versioning

### Ethical AI
- Bias detection and mitigation
- Fairness metrics and validation
- Model explainability and interpretability
- Privacy-preserving techniques
- Robustness testing
- Compliance validation

## MCP Integration

This agent leverages four powerful MCP servers:

### filesystem
- Read/write model code (TensorFlow, PyTorch, JAX)
- Manage training scripts and pipelines
- Access datasets and data preprocessing code
- Save/load model checkpoints and weights
- Handle model artifacts and metadata

### github
- Version control for model code and experiments
- Collaborate on AI projects
- Access model repositories and benchmarks
- Track model improvements via issues
- Manage model version releases

### context7
- Semantic search for similar model implementations
- Find existing neural network architectures
- Locate data preprocessing patterns
- Discover training pipeline examples
- Find optimization techniques in codebase

### fetch
- Call model serving APIs for inference
- Access MLOps platforms (MLflow, Weights & Biases)
- Query experiment tracking services
- Integrate with cloud ML services (SageMaker, Vertex AI)
- Access monitoring dashboards

## Slash Commands

### /ai-design - Design AI System Architecture

Design complete AI system architecture including model selection, data pipelines, training infrastructure, and deployment strategy.

```bash
/ai-design [use-case] [requirements]
```

**Example:**
```bash
/ai-design recommendation-system "real-time personalization, <50ms latency, 100M users"
```

**What it does:**
1. Analyzes use case and requirements
2. Evaluates data characteristics
3. Selects appropriate model architectures
4. Designs data preprocessing pipelines
5. Plans training infrastructure
6. Designs inference architecture
7. Defines monitoring and feedback loops
8. Documents scaling strategies

### /ai-model - Implement Model

Implement AI model from scratch or adapt existing architectures, including training pipeline, optimization, and evaluation.

```bash
/ai-model [architecture] [task] [framework]
```

**Example:**
```bash
/ai-model transformer text-classification pytorch
```

**What it does:**
1. Sets up model architecture
2. Implements data loading and preprocessing
3. Configures training loop
4. Adds validation and metrics
5. Implements hyperparameter tuning
6. Adds model compression
7. Creates evaluation suite
8. Documents model specifications

### /ai-deploy - Deploy to Production

Deploy AI model to production with monitoring, A/B testing, and rollback capabilities.

```bash
/ai-deploy [model-path] [environment] [deployment-type]
```

**Example:**
```bash
/ai-deploy ./models/classifier-v2 production rest-api
```

**What it does:**
1. Optimizes model for inference
2. Creates deployment container/package
3. Sets up serving infrastructure
4. Configures monitoring and alerts
5. Implements A/B testing framework
6. Adds rollback mechanisms
7. Creates deployment documentation
8. Validates production metrics

## Supported Frameworks

- **TensorFlow/Keras**: End-to-end ML platform
- **PyTorch**: Research and production deep learning
- **JAX**: High-performance numerical computing
- **ONNX**: Cross-framework model deployment
- **TensorRT**: NVIDIA GPU optimization
- **Core ML**: iOS/macOS deployment
- **TensorFlow Lite**: Mobile and embedded devices
- **OpenVINO**: Intel hardware optimization

## Typical Workflows

### 1. New AI Project Setup

```bash
# Design the architecture
/ai-design image-classification "multi-class, 1000 categories, mobile deployment"

# Agent will:
# - Analyze requirements and constraints
# - Select appropriate model architecture (e.g., EfficientNet)
# - Design data preprocessing pipeline
# - Plan training infrastructure
# - Create deployment strategy for mobile
# - Document the complete architecture
```

### 2. Model Implementation

```bash
# Implement the model
/ai-model efficientnet image-classification tensorflow

# Agent will:
# - Create model architecture code
# - Set up data loading pipeline
# - Implement training loop with validation
# - Add metrics and logging
# - Configure hyperparameter tuning
# - Implement model compression
# - Create evaluation scripts
```

### 3. Model Optimization

The agent automatically optimizes models through:
- Quantization (INT8, FP16)
- Pruning (structured and unstructured)
- Knowledge distillation
- Graph optimization
- Hardware-specific optimizations

### 4. Production Deployment

```bash
# Deploy to production
/ai-deploy ./models/efficientnet-v2 production rest-api

# Agent will:
# - Optimize model for inference (quantization, pruning)
# - Create Docker container with serving infrastructure
# - Set up REST API endpoints
# - Configure monitoring and alerting
# - Implement A/B testing
# - Create rollback procedures
# - Validate production performance
```

## Performance Standards

The AI Engineer agent ensures:

- **Model Accuracy**: >90% on validation data
- **Inference Latency**: <100ms per request
- **Model Size**: >50% reduction through compression
- **Bias Score**: <0.05 on fairness metrics
- **Throughput**: Optimized for target load
- **Resource Utilization**: Efficient use of compute resources

## Monitoring and Metrics

The agent implements comprehensive monitoring:

- Model accuracy and performance metrics
- Inference latency and throughput
- Resource utilization (CPU, GPU, memory)
- Bias and fairness metrics
- Error rates and failure modes
- Cache hit rates
- A/B test results
- Data drift detection

## Best Practices

### Model Development
1. Start with simple baselines to establish performance floor
2. Always validate on held-out test data
3. Track all experiments with proper versioning
4. Version control both datasets and models
5. Document hyperparameters and configurations
6. Monitor training metrics continuously
7. Test on diverse data distributions
8. Measure and mitigate bias

### Optimization
1. Profile code before optimizing
2. Use appropriate quantization techniques
3. Enable hardware acceleration where available
4. Implement efficient batching strategies
5. Cache frequent predictions
6. Optimize data loading pipelines
7. Use efficient model architectures
8. Monitor resource usage

### Deployment
1. Validate model performance before deployment
2. Implement gradual rollout (canary, blue-green)
3. Monitor inference metrics in real-time
4. Set up comprehensive alerts
5. Enable A/B testing for validation
6. Plan and test rollback strategies
7. Document all dependencies
8. Maintain comprehensive model registry

### Ethical AI
1. Measure bias across demographic groups
2. Test on diverse populations
3. Document model limitations clearly
4. Enable model explainability
5. Preserve user privacy
6. Validate model robustness
7. Maintain complete audit trails
8. Review models regularly

## Setup

### Prerequisites
- Node.js 18+ for MCP servers
- Python 3.8+ for AI frameworks
- Git for version control
- Access to compute resources (GPU recommended)

### Installation

1. Clone the agent directory:
```bash
cd claude-code-agent-marketplace/categories/05-data-ai/ai-engineer
```

2. Configure MCP servers (see mcp-config.json)

3. Set up optional environment variables:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=your_token_here
```

### Configuration

The agent uses `mcp-config.json` for MCP server configuration. Customize based on your needs:

- **filesystem**: Configure allowed directories for model code
- **github**: Set GitHub token for repository access
- **context7**: Configure for your codebase
- **fetch**: Add API endpoints for MLOps tools

## Integration with Other Agents

The AI Engineer agent collaborates with:

- **data-engineer**: Data pipelines and ETL
- **ml-engineer**: Model deployment infrastructure
- **llm-architect**: Large language model systems
- **data-scientist**: Research and experimentation
- **mlops-engineer**: Infrastructure and automation
- **prompt-engineer**: LLM integration
- **performance-engineer**: System optimization
- **security-auditor**: Model security and privacy

## Example Use Cases

### Computer Vision
- Image classification and object detection
- Semantic segmentation
- Face recognition and verification
- Image generation and enhancement
- Video analysis and tracking

### Natural Language Processing
- Text classification and sentiment analysis
- Named entity recognition
- Machine translation
- Question answering
- Text generation and summarization

### Recommender Systems
- Collaborative filtering
- Content-based recommendations
- Hybrid recommendation systems
- Real-time personalization
- Session-based recommendations

### Time Series
- Forecasting and prediction
- Anomaly detection
- Pattern recognition
- Predictive maintenance
- Financial modeling

### Multi-modal AI
- Vision-language models
- Audio-visual processing
- Cross-modal retrieval
- Multi-modal generation
- Sensor fusion

## Quality Checklist

Before deployment, the agent ensures:

- [ ] Model accuracy targets met
- [ ] Inference latency < 100ms
- [ ] Model size optimized
- [ ] Bias metrics tracked and acceptable
- [ ] Explainability features implemented
- [ ] A/B testing enabled
- [ ] Comprehensive monitoring configured
- [ ] Complete documentation
- [ ] Compliance requirements verified
- [ ] Rollback procedures tested

## Support and Resources

### Documentation
- See CLAUDE.md for detailed agent instructions
- Review agent-manifest.json for complete capabilities
- Check mcp-config.json for MCP server setup

### MLOps Tools
- MLflow for experiment tracking
- Weights & Biases for model monitoring
- TensorBoard for visualization
- Kubeflow for ML workflows
- Cloud platforms (SageMaker, Vertex AI, Azure ML)

### Monitoring Tools
- Prometheus for metrics collection
- Grafana for visualization
- DataDog for comprehensive monitoring
- CloudWatch for AWS deployments

## Contributing

To enhance the AI Engineer agent:

1. Add new model architectures
2. Implement additional optimization techniques
3. Add support for new frameworks
4. Enhance monitoring capabilities
5. Improve bias detection methods
6. Add new deployment patterns
7. Document best practices
8. Share successful implementations

## License

Part of the Claude Code Agent Marketplace. See repository root for license information.

---

**Remember**: Always prioritize accuracy, efficiency, and ethical considerations while building AI systems that deliver real value and maintain trust through transparency and reliability.
