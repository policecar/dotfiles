---
name: ml-systems-design
description: Design ML systems and architectures with production and research considerations. Use for system architecture, ML pipeline design, and infrastructure planning.
---

# ML Systems Design

You are helping design an ML system or architecture. Apply systems thinking with ML-specific considerations.

## Design Dimensions

### 1. Requirements Clarification
- **Scale**: Data volume, request rate, latency requirements
- **Accuracy**: What level of performance is acceptable? What's the cost of errors?
- **Users**: Who uses this? What's their technical level?
- **Constraints**: Budget, compute, time-to-deploy, maintenance capacity

### 2. Data Pipeline
- **Data sources**: Where does data come from? Format, volume, velocity
- **Data quality**: How clean is it? What validation is needed?
- **Storage**: Scale, access patterns, retention policies
- **Versioning**: How to track data versions and lineage?
- **Privacy/Security**: PII handling, access controls, compliance

### 3. Model Design
- **Problem formulation**: Classification, regression, ranking, generation?
- **Architecture selection**: Tradeoffs between model families
- **Computational requirements**: Training and inference costs
- **Model versioning**: How to track experiments and production models
- **Fallback strategies**: What happens when the model fails?

### 4. Training Pipeline
- **Compute infrastructure**: GPUs, distributed training, cost optimization
- **Experiment tracking**: Wandb, MLflow, custom solutions
- **Hyperparameter search**: Grid, random, Bayesian optimization
- **Validation strategy**: Train/val/test splits, cross-validation, time-based splits
- **Reproducibility**: Seeds, versioning, containerization

### 5. Serving Infrastructure
- **Latency requirements**: Real-time, batch, streaming?
- **Scaling strategy**: Vertical vs horizontal, auto-scaling triggers
- **Model optimization**: Quantization, pruning, compilation (ONNX, TensorRT)
- **A/B testing**: How to safely deploy and compare models
- **Monitoring**: Metrics, dashboards, alerting

### 6. Monitoring & Observability
- **Model metrics**: Accuracy, latency, throughput
- **Data drift**: Distribution shifts, feature drift detection
- **Prediction monitoring**: Edge cases, anomalies, error analysis
- **System health**: Resource usage, error rates, SLAs
- **Debugging**: Logging, tracing, profiling

### 7. Iteration & Improvement
- **Feedback loops**: How to collect labels and user feedback
- **Retraining strategy**: Frequency, triggers, automation
- **Model updates**: Blue-green deployment, canary releases
- **Continuous evaluation**: Ongoing validation, regression testing

## Technical Considerations

### Performance
- **Batch vs online**: Tradeoffs in latency, throughput, resource usage
- **Caching**: Where and what to cache?
- **Parallelization**: Data parallelism, model parallelism, pipeline parallelism

### Reliability
- **Failure modes**: What can go wrong? How to detect and recover?
- **Rate limiting**: Protect against overload
- **Circuit breakers**: Graceful degradation
- **Backup strategies**: Model fallbacks, cached predictions

### Maintainability
- **Code organization**: Modular, testable, documented
- **Testing**: Unit tests, integration tests, regression tests
- **Documentation**: Architecture decisions, runbooks, APIs
- **Onboarding**: Can new team members understand and contribute?

## Decision Framework

For each design decision, consider:

1. **Requirements**: What are we optimizing for?
2. **Options**: What are the concrete alternatives?
3. **Tradeoffs**: Performance vs complexity, cost vs accuracy, speed vs reliability
4. **Precedent**: What do similar systems do? Why?
5. **Risks**: What could go wrong? How to mitigate?

## Output Format

Provide:
- **Architecture diagram** (in text/ASCII if needed)
- **Component breakdown** with responsibilities
- **Data flow** through the system
- **Key decisions** with rationale
- **Open questions** that need resolution
- **Risks & mitigations**
- **Rough estimates** (scale, cost, timeline)

## When to Use This Skill

- Designing new ML systems from scratch
- Refactoring existing ML pipelines
- Evaluating architectural options
- Planning infrastructure for ML projects
- Reviewing system designs for correctness and scalability
