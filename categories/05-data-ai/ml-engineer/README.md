# ML Engineer Agent

Expert ML engineer specializing in machine learning model lifecycle, production deployment, and ML system optimization. Masters both traditional ML and deep learning with focus on building scalable, reliable ML systems from training to serving.

## Overview

The ML Engineer agent is your production ML specialist, covering the complete machine learning lifecycle from data validation through model serving. It excels at building robust, scalable ML systems that deliver reliable predictions in production environments.

### Key Capabilities

- **ML Pipeline Development**: End-to-end pipeline orchestration for training and inference
- **Feature Engineering**: Feature extraction, transformation, and feature store integration
- **Model Training**: Algorithm selection, hyperparameter optimization, distributed training
- **Production Deployment**: Blue-green, canary releases, and various serving strategies
- **Model Monitoring**: Drift detection, performance tracking, automated retraining
- **A/B Testing**: Experiment design, statistical testing, and rollout decisions
- **System Optimization**: Scaling, caching, batching, and performance tuning
- **Reliability Engineering**: Health checks, fallback models, disaster recovery

## Slash Commands

### /ml-train - Train Machine Learning Model

Train a model with comprehensive pipeline including data validation, feature engineering, and experiment tracking.

**Usage**:
```
/ml-train [model_type] [data_path] [config_path]
```

**Examples**:
```bash
# Train random forest classifier
/ml-train random_forest ./data/train.csv ./config/rf_config.yaml

# Train XGBoost with custom config
/ml-train xgboost ./data/train.parquet ./config/xgb_config.json

# Train neural network
/ml-train neural_net ./data/embeddings.h5 ./config/nn_config.yaml
```

**Features**:
- Data validation and quality checks
- Automated feature engineering pipeline
- Hyperparameter optimization
- Cross-validation
- Checkpointing and recovery
- Experiment tracking with MLflow
- Model artifact management
- Training metrics visualization

### /ml-evaluate - Evaluate Model Performance

Comprehensive model evaluation with multiple metrics, visualizations, and bias detection.

**Usage**:
```
/ml-evaluate [model_path] [data_path] [metrics]
```

**Examples**:
```bash
# Evaluate classifier
/ml-evaluate ./models/model_v1.pkl ./data/test.csv "accuracy,f1,auc"

# Evaluate regression model
/ml-evaluate ./models/xgb_model.json ./data/validation.parquet "rmse,mae,r2"

# Evaluate deep learning model
/ml-evaluate ./models/classifier.h5 ./data/test.tfrecord "precision,recall,auc"
```

**Features**:
- Multiple metrics calculation
- Confusion matrix and ROC curves
- Prediction distribution analysis
- Bias and fairness detection
- Feature importance analysis
- Comparison with baselines
- Performance report generation
- Statistical significance testing

### /ml-serve - Deploy Model for Inference

Deploy models with production-grade serving infrastructure including monitoring and scaling.

**Usage**:
```
/ml-serve [model_path] [serving_config]
```

**Examples**:
```bash
# Deploy with REST API
/ml-serve ./models/model_v1.pkl ./config/serve_config.yaml

# Deploy ONNX model
/ml-serve ./models/production_model.onnx ./config/rest_api_config.json

# Deploy ensemble on Kubernetes
/ml-serve ./models/ensemble ./config/k8s_serving_config.yaml
```

**Features**:
- REST API and gRPC endpoints
- Request batching and caching
- Health checks and monitoring
- Autoscaling configuration
- Blue-green and canary deployments
- Latency optimization
- Load balancing
- Logging and metrics

## MCP Integration

This agent uses Model Context Protocol servers for enhanced functionality:

### filesystem
Access ML artifacts, training data, configs, and pipelines across your project.

### github
Track model versions, review ML code changes, and manage experiment history.

### context7
Retrieve ML best practices, optimization techniques, and deployment patterns.

### fetch
Access ML framework documentation, model architectures, and API references.

## Workflow

### 1. System Analysis
- Define ML problem and success criteria
- Assess data quality and availability
- Review infrastructure constraints
- Plan deployment strategy
- Design monitoring approach

### 2. Implementation
- Build feature pipelines
- Implement training orchestration
- Optimize model performance
- Deploy with gradual rollout
- Set up monitoring and alerts

### 3. Production Excellence
- Achieve performance targets
- Automate retraining pipelines
- Monitor drift and degradation
- Maintain documentation
- Deliver measurable business value

## Tooling Ecosystem

### Experiment Tracking
- **MLflow**: Experiment management and model registry
- **Weights & Biases**: Visualization and collaboration
- **TensorBoard**: Metrics and architecture visualization
- **Neptune**: Team collaboration and tracking

### Pipeline Orchestration
- **Kubeflow Pipelines**: Kubernetes-native ML workflows
- **Apache Airflow**: General-purpose workflow orchestration
- **Prefect**: Modern workflow engine
- **Metaflow**: Human-friendly ML stack

### Hyperparameter Optimization
- **Optuna**: Bayesian optimization framework
- **Ray Tune**: Distributed hyperparameter tuning
- **Hyperopt**: Python library for optimization
- **Keras Tuner**: Deep learning HPO

### Model Serving
- **BentoML**: Model packaging and serving
- **Seldon Core**: Kubernetes-native serving
- **TorchServe**: PyTorch model serving
- **TensorFlow Serving**: TensorFlow model serving

### Feature Stores
- **Feast**: Open-source feature store
- **Tecton**: Enterprise feature platform
- **Hopsworks**: ML data platform

### Versioning
- **DVC**: Data version control
- **Git**: Code versioning
- **Model Registries**: MLflow, W&B model versioning

## Performance Targets

- **Training Time**: < 4 hours
- **Inference Latency**: < 50ms (p95)
- **Model Accuracy**: > 90% (domain-dependent)
- **Pipeline Reliability**: > 99%
- **Data Validation**: 100% coverage
- **Monitoring**: 100% coverage

## Best Practices

### Pipeline Design
- Modular, reusable components
- Version all artifacts (code, data, models)
- Comprehensive testing (unit, integration, E2E)
- Validate data quality at every stage
- Maintain feature consistency across train/serve
- Implement graceful error handling
- Document all processes

### Deployment Strategies
- Use gradual rollouts (blue-green, canary)
- Maintain fallback models
- Implement health checks
- Set up monitoring and alerting
- Test under realistic load
- Plan rollback procedures
- Monitor business metrics

### Monitoring
- Track prediction and feature drift
- Monitor performance metrics continuously
- Set up automated alerts
- Analyze error patterns
- Track resource utilization
- Measure business impact
- Implement automated retraining triggers

### Optimization
- Batch requests for efficiency
- Cache predictions when appropriate
- Use model compression techniques
- Implement request queuing
- Optimize feature computation
- Profile and remove bottlenecks
- Scale horizontally when needed

## Integration with Other Agents

- **data-scientist**: Model development and experimentation
- **data-engineer**: Feature pipelines and data infrastructure
- **mlops-engineer**: ML infrastructure and automation
- **backend-developer**: ML API integration
- **ai-engineer**: Deep learning and advanced AI
- **devops-engineer**: Deployment and infrastructure
- **performance-engineer**: System optimization
- **qa-expert**: ML testing and validation

## Configuration Example

### Training Config (YAML)
```yaml
model:
  type: random_forest
  n_estimators: 100
  max_depth: 10

data:
  train_path: ./data/train.csv
  validation_split: 0.2
  test_path: ./data/test.csv

features:
  numerical: [age, income, credit_score]
  categorical: [occupation, region]
  target: default

training:
  cross_validation: 5
  hyperparameter_search: bayesian
  early_stopping: true
  checkpoint_interval: 100

tracking:
  experiment_name: credit_default_prediction
  mlflow_uri: http://localhost:5000
```

### Serving Config (YAML)
```yaml
model:
  path: ./models/model_v1.pkl
  format: sklearn

serving:
  type: rest_api
  host: 0.0.0.0
  port: 8080
  workers: 4

inference:
  batch_size: 32
  timeout_ms: 100
  cache_predictions: true
  cache_ttl: 300

monitoring:
  enable_metrics: true
  log_predictions: true
  drift_detection: true

scaling:
  min_replicas: 2
  max_replicas: 10
  target_cpu_utilization: 70
```

## Success Metrics

A successful ML system delivers:
- Model accuracy meeting business requirements
- Training pipeline completing in < 4 hours
- Inference latency < 50ms (p95)
- Automated drift detection active
- Automated retraining pipeline operational
- Comprehensive monitoring dashboard
- Clear rollback procedures documented
- Measurable business impact (revenue, conversion, etc.)

## Getting Started

1. **Setup**: Configure MCP servers and environment variables
2. **Train**: Use `/ml-train` to develop and optimize your model
3. **Evaluate**: Use `/ml-evaluate` to validate performance
4. **Deploy**: Use `/ml-serve` to deploy to production
5. **Monitor**: Set up dashboards and alerts for ongoing monitoring
6. **Iterate**: Use automated retraining and continuous improvement

## Support and Resources

- ML framework documentation (scikit-learn, TensorFlow, PyTorch)
- MLOps platform guides (MLflow, Kubeflow)
- Production ML best practices
- Model serving optimization techniques
- A/B testing methodologies
- Statistical testing frameworks

---

Built with reliability, performance, and maintainability as core principles. Deploy ML systems that deliver consistent value through automated, monitored, and continuously improving machine learning pipelines.
