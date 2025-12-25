# NLP Engineer Agent

Expert NLP engineer specializing in natural language processing, understanding, and generation. Masters transformer models, text processing pipelines, and production NLP systems with focus on multilingual support and real-time performance.

## Overview

The NLP Engineer agent is your comprehensive partner for natural language processing tasks. From text preprocessing to deploying production-ready multilingual NLP systems, this agent handles transformer models (BERT, GPT, T5), builds robust text processing pipelines, implements named entity recognition, sentiment analysis, machine translation, and more.

## Key Capabilities

### Text Preprocessing Pipelines
- Tokenization strategies (WordPiece, BPE, SentencePiece)
- Text normalization and cleaning
- Language detection and encoding handling
- Noise removal and sentence segmentation
- Entity masking and data augmentation
- Multilingual text processing

### Named Entity Recognition (NER)
- Custom entity type definitions
- Model selection and training
- Active learning for data efficiency
- Multilingual NER systems
- Domain adaptation techniques
- Confidence scoring and post-processing
- Production-ready NER APIs

### Text Classification
- Multi-class and multi-label classification
- Hierarchical classification
- Zero-shot and few-shot learning
- Domain transfer and adaptation
- Class imbalance handling
- Sentiment and intent classification
- Topic categorization

### Language Modeling
- Pre-training and fine-tuning strategies
- Adapter methods for efficiency
- Prompt engineering
- Perplexity optimization
- Generation control and decoding
- Context window management
- Language model APIs

### Machine Translation
- Neural machine translation (NMT)
- Parallel data processing
- Back-translation for data augmentation
- Quality estimation
- Low-resource language support
- Real-time translation systems
- Post-editing and quality control

### Question Answering
- Extractive and generative QA
- Multi-hop reasoning
- Document retrieval and ranking
- Answer validation and confidence scoring
- Context windowing strategies
- Multilingual QA systems
- Domain-specific QA

### Advanced NLP Tasks
- Sentiment and emotion analysis
- Information extraction and relation extraction
- Conversational AI and dialogue systems
- Text generation and summarization
- Knowledge graph construction
- Coreference resolution

## MCP Integration

This agent leverages four powerful MCP servers:

### filesystem
- Read/write NLP model code (transformers, spaCy, NLTK)
- Manage text preprocessing scripts
- Access training datasets and corpora
- Save/load model checkpoints and embeddings
- Handle tokenizer configurations
- Organize language resources

### github
- Version control for NLP model code
- Collaborate on text processing pipelines
- Access pre-trained model repositories
- Track model improvements via issues
- Share trained models and tokenizers
- Manage model version releases

### context7
- Semantic search for NLP implementations
- Find existing transformer model code
- Locate text preprocessing patterns
- Discover tokenization strategies
- Find evaluation metric implementations
- Search for multilingual examples

### fetch
- Call NLP model serving APIs
- Access translation services (DeepL, Google Translate)
- Query language detection APIs
- Fetch pre-trained models from Hugging Face
- Access NLP platform APIs (AWS Comprehend, Azure)
- Integrate with text annotation tools

## Slash Commands

### /nlp-pipeline - Create NLP Pipeline

Create complete NLP processing pipeline including text preprocessing, model inference, and post-processing.

```bash
/nlp-pipeline [task] [languages] [requirements]
```

**Example:**
```bash
/nlp-pipeline sentiment-analysis "en,es,fr" "real-time, aspect-based, >0.90 F1"
```

**What it does:**
1. Analyzes task requirements and target languages
2. Designs text preprocessing pipeline
3. Selects appropriate NLP models
4. Configures tokenization and normalization
5. Implements model inference
6. Adds post-processing rules
7. Sets up monitoring and evaluation
8. Documents pipeline components

### /nlp-model - Train NLP Model

Train or fine-tune NLP model for specific task with custom data and evaluation metrics.

```bash
/nlp-model [model-type] [task] [data-path]
```

**Example:**
```bash
/nlp-model bert-base named-entity-recognition ./data/ner_corpus
```

**What it does:**
1. Prepares training data and splits
2. Configures model architecture
3. Sets up tokenization strategy
4. Implements training loop
5. Adds validation metrics
6. Fine-tunes hyperparameters
7. Evaluates on test set
8. Exports optimized model

### /nlp-evaluate - Evaluate Model

Comprehensive model evaluation with multiple metrics, error analysis, and bias detection.

```bash
/nlp-evaluate [model-path] [test-data] [metrics]
```

**Example:**
```bash
/nlp-evaluate ./models/ner-v2 ./data/test.jsonl "f1,precision,recall,bias"
```

**What it does:**
1. Loads model and test data
2. Runs inference on test set
3. Calculates performance metrics
4. Performs error analysis
5. Checks for bias across demographics
6. Generates confusion matrices
7. Creates evaluation report
8. Provides improvement recommendations

## Supported Transformer Models

- **BERT**: Bidirectional encoding for classification, NER, QA
- **GPT**: Autoregressive generation for text completion
- **T5/BART**: Seq2seq for translation, summarization, generation
- **RoBERTa**: Robustly optimized BERT for better performance
- **XLM-RoBERTa**: Cross-lingual understanding for multilingual tasks
- **DistilBERT**: Faster, lighter BERT for production
- **ELECTRA**: Efficient pre-training for resource-constrained scenarios
- **DeBERTa**: Improved attention for state-of-art results

## NLP Frameworks

- **Hugging Face Transformers**: Pre-trained models and pipelines
- **spaCy**: Production-ready NLP with entity recognition
- **NLTK**: Classic NLP toolkit for research and education
- **Gensim**: Topic modeling and document similarity
- **Stanford CoreNLP**: Comprehensive linguistic analysis
- **AllenNLP**: Research library built on PyTorch
- **Flair**: State-of-art NER and text classification
- **FastText**: Efficient text classification and embeddings

## Typical Workflows

### 1. Build Sentiment Analysis Pipeline

```bash
# Create multilingual sentiment analysis pipeline
/nlp-pipeline sentiment-analysis "en,es,fr,de" "real-time, aspect-based, >0.90 F1"

# Agent will:
# - Design preprocessing for multiple languages
# - Select appropriate multilingual model (XLM-RoBERTa)
# - Configure aspect extraction
# - Implement sentiment classification
# - Add confidence scoring
# - Set up real-time API
# - Configure monitoring
# - Create documentation
```

### 2. Train Custom NER Model

```bash
# Train domain-specific NER model
/nlp-model bert-base named-entity-recognition ./data/medical_ner

# Agent will:
# - Load and validate training data
# - Configure BERT tokenizer
# - Set up NER architecture
# - Implement training with validation
# - Tune hyperparameters
# - Evaluate on test set
# - Export optimized model
# - Document entity types and performance
```

### 3. Comprehensive Model Evaluation

```bash
# Evaluate NER model performance
/nlp-evaluate ./models/medical-ner-v2 ./data/test_medical.jsonl "f1,precision,recall,bias"

# Agent will:
# - Load model and test data
# - Run inference and calculate metrics
# - Analyze errors by entity type
# - Check bias across text sources
# - Generate confusion matrix
# - Create detailed evaluation report
# - Suggest improvements
```

### 4. Deploy Translation System

The agent can build complete machine translation systems:
- Parallel corpus processing
- Neural MT model training
- Quality estimation
- Real-time translation API
- Performance monitoring
- Continuous improvement

## Performance Standards

The NLP Engineer agent ensures:

- **F1 Score**: >0.85 for classification and NER tasks
- **Inference Latency**: <100ms per request
- **Model Size**: <1GB for production models
- **Multilingual Support**: 10+ languages
- **Throughput**: Optimized for target load
- **Accuracy**: Consistently meets domain requirements

## Monitoring and Metrics

The agent implements comprehensive monitoring:

- F1 score, precision, and recall
- Inference latency and throughput
- Model size and memory usage
- Per-language performance
- Bias metrics across demographics
- Error rates by category
- Data drift detection
- API response times
- Cache hit rates

## Best Practices

### Text Preprocessing
1. Preserve important information during cleaning
2. Handle multiple languages and scripts
3. Normalize consistently across pipeline
4. Validate encoding before processing
5. Remove noise while preserving signal
6. Test preprocessing on edge cases
7. Document preprocessing decisions
8. Version preprocessing code

### Model Training
1. Start with pre-trained models when possible
2. Use appropriate tokenization for model type
3. Balance training data across classes
4. Validate on diverse test sets
5. Monitor for overfitting
6. Track all hyperparameters
7. Save checkpoints regularly
8. Document training process

### Multilingual NLP
1. Use multilingual pre-trained models (XLM-RoBERTa, mBERT)
2. Test on all supported languages
3. Handle code-switching appropriately
4. Consider script differences (Latin, Arabic, CJK)
5. Validate cultural appropriateness
6. Monitor per-language performance
7. Support right-to-left languages
8. Document language coverage and limitations

### Production Deployment
1. Optimize model size for latency requirements
2. Implement efficient batching strategies
3. Cache frequent predictions
4. Monitor inference performance continuously
5. Handle edge cases gracefully
6. Set up fallback mechanisms
7. Version models properly
8. Document API specifications thoroughly

## Setup

### Prerequisites
- Python 3.8+ for NLP frameworks
- Node.js 18+ for MCP servers
- Git for version control
- GPU recommended for model training

### Installation

1. Clone the agent directory:
```bash
cd claude-code-agent-marketplace/categories/05-data-ai/nlp-engineer
```

2. Install NLP dependencies:
```bash
pip install transformers spacy nltk torch
python -m spacy download en_core_web_sm
```

3. Configure MCP servers (see mcp-config.json)

4. Set up optional environment variables:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=your_token_here
export HUGGINGFACE_TOKEN=your_hf_token_here
```

### Configuration

The agent uses `mcp-config.json` for MCP server configuration. Customize based on your needs:

- **filesystem**: Configure allowed directories for NLP code
- **github**: Set GitHub token for repository access
- **context7**: Configure for your codebase
- **fetch**: Add API endpoints for NLP services

## Integration with Other Agents

The NLP Engineer agent collaborates with:

- **ai-engineer**: Model architecture and optimization
- **data-scientist**: Text analysis and experimentation
- **ml-engineer**: Model deployment infrastructure
- **prompt-engineer**: Language model integration
- **data-engineer**: Data pipelines and ETL
- **backend-developer**: API implementation
- **frontend-developer**: UI for NLP features
- **product-manager**: Feature requirements

## Example Use Cases

### Text Classification
- Sentiment analysis (positive, negative, neutral)
- Intent detection for chatbots
- Topic categorization
- Spam detection
- Content moderation
- Document classification

### Named Entity Recognition
- Person, organization, location extraction
- Medical entity recognition
- Product name extraction
- Custom domain entities
- Multilingual NER
- Entity linking

### Machine Translation
- Document translation
- Real-time chat translation
- Subtitle translation
- Low-resource language pairs
- Domain-specific translation
- Quality estimation

### Question Answering
- Customer support automation
- Document search and retrieval
- FAQ systems
- Knowledge base QA
- Multi-hop reasoning
- Conversational QA

### Text Generation
- Summarization (extractive and abstractive)
- Paraphrasing and rewriting
- Data-to-text generation
- Creative writing assistance
- Report generation
- Content creation

### Conversational AI
- Chatbot development
- Dialogue management
- Slot filling for task completion
- Context tracking
- Multi-turn conversations
- Intent and entity recognition

## Quality Checklist

Before deployment, the agent ensures:

- [ ] F1 score > 0.85 achieved
- [ ] Inference latency < 100ms
- [ ] Multilingual support enabled
- [ ] Model size optimized < 1GB
- [ ] Error handling comprehensive
- [ ] Monitoring implemented
- [ ] Pipeline documented
- [ ] Evaluation automated
- [ ] Bias metrics tracked
- [ ] APIs tested and stable

## Support and Resources

### Documentation
- See CLAUDE.md for detailed agent instructions
- Review agent-manifest.json for complete capabilities
- Check mcp-config.json for MCP server setup

### NLP Platforms
- Hugging Face Hub for pre-trained models
- spaCy Universe for NLP components
- Google Cloud NLP for cloud services
- AWS Comprehend for managed NLP
- Azure Cognitive Services for enterprise

### MLOps Tools
- MLflow for experiment tracking
- Weights & Biases for model monitoring
- TensorBoard for visualization
- DVC for data versioning
- Neptune.ai for model management

## Contributing

To enhance the NLP Engineer agent:

1. Add new transformer architectures
2. Implement additional NLP tasks
3. Add support for new languages
4. Enhance preprocessing techniques
5. Improve evaluation metrics
6. Add new deployment patterns
7. Document best practices
8. Share successful implementations

## License

Part of the Claude Code Agent Marketplace. See repository root for license information.

---

**Remember**: Always prioritize accuracy, performance, and multilingual support while building robust NLP systems that handle real-world text effectively.
