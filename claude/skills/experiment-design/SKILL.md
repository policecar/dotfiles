---
name: experiment-design
description: Design rigorous ML/AI experiments with proper controls and statistical validity. Use when planning experiments, ablation studies, or empirical evaluations.
---

# Experiment Design

You are helping design an ML/AI experiment. Apply rigorous experimental methodology and statistical thinking.

## Experiment Planning Framework

### 1. Research Question
- **Hypothesis**: What specific claim are you testing?
- **Motivation**: Why does this matter? What decision depends on this?
- **Scope**: What's in scope vs out of scope for this experiment?

### 2. Variables & Factors
- **Independent variables**: What are you manipulating? (model architecture, hyperparameters, data)
- **Dependent variables**: What are you measuring? (accuracy, latency, loss)
- **Control variables**: What must be held constant? (seeds, hardware, data splits)
- **Confounding factors**: What else might affect results? How to control for them?

### 3. Metrics & Success Criteria
- **Primary metrics**: What's the main measure of success?
- **Secondary metrics**: What else matters? (efficiency, robustness, interpretability)
- **Practical significance**: What size of effect matters? Not just statistical significance.
- **Tradeoffs**: How to handle multi-objective scenarios?

### 4. Baseline Comparisons
- **Baselines**: What are you comparing against?
  - Trivial baseline (random, majority class)
  - Simple baseline (linear model, k-NN)
  - Strong baseline (SOTA, established method)
  - Ablated versions of your approach
- **Fair comparison**: Same data, same compute budget, same evaluation

### 5. Data Considerations
- **Dataset selection**: Representative of the problem? Known biases?
- **Data splits**: Train/val/test or cross-validation? Stratified? Time-based?
- **Sample size**: Statistical power analysis - how many samples needed?
- **Data leakage**: Any information from test set leaking into training?

### 6. Experimental Design
- **Design type**:
  - Between-subjects (different datasets/seeds)
  - Within-subjects (same datasets, different methods)
  - Factorial (multiple factors varied systematically)
- **Replication**: How many random seeds/runs per condition?
- **Order effects**: Randomize order of experiments to avoid bias

### 7. Statistical Analysis
- **Significance testing**: Appropriate tests (t-test, ANOVA, non-parametric)
- **Multiple comparisons**: Bonferroni or other corrections when needed
- **Effect size**: Cohen's d, confidence intervals, not just p-values
- **Variance analysis**: Understanding sources of variation

### 8. Ablation Studies
For understanding what matters in your approach:
- **Component ablations**: Remove each component individually
- **Cumulative ablations**: Add components incrementally
- **Hyperparameter sensitivity**: How robust is it to changes?
- **Data ablations**: Performance vs training data size

### 9. Robustness & Generalization
- **Stress tests**: Edge cases, out-of-distribution data
- **Perturbation analysis**: Noise, adversarial examples
- **Cross-dataset**: Does it work on other datasets?
- **Domain shift**: Performance under distribution shift

### 10. Reproducibility
- **Fixed seeds**: Random seeds for data splits, initialization, dropout
- **Versioning**: Code version, library versions, data version
- **Documentation**: Hyperparameters, hardware, runtime
- **Artifacts**: Save models, predictions, logs for analysis

## Common Pitfalls to Avoid

- **P-hacking**: Trying many things and only reporting what works
- **Data leakage**: Test set information influencing training
- **Unfair baselines**: Comparing tuned method to untuned baseline
- **Cherry-picking**: Selecting best run rather than reporting distributions
- **Insufficient replication**: Single run, no error bars
- **Confounded comparisons**: Changing multiple things at once
- **Overinterpreting noise**: Seeing patterns in random variation

## Computational Budget

- **Time constraints**: How long can experiments run?
- **Resource constraints**: GPU hours, memory limits
- **Parallel vs sequential**: What can run in parallel?
- **Priority ordering**: Which experiments are most informative?
- **Early stopping**: When can you conclude without full runs?

## Analysis & Interpretation

### During Experiments
- **Training curves**: Convergence, overfitting, instability
- **Intermediate checkpoints**: Performance trajectory over time
- **Resource monitoring**: GPU util, memory usage, bottlenecks

### Post-Experiment
- **Statistical summaries**: Mean, std, median, min/max across runs
- **Visualization**: Plots with error bars, distributions, not just tables
- **Error analysis**: What examples does it fail on? Patterns?
- **Unexpected results**: Investigate anomalies, don't ignore them

## Documentation & Reporting

Report:
1. **Research question** and hypothesis
2. **Experimental setup**: Data, models, hyperparameters, hardware
3. **Baselines** and comparisons
4. **Results**: Tables, plots, statistical tests
5. **Ablations**: What components matter?
6. **Analysis**: Why these results? What do they mean?
7. **Limitations**: What wasn't tested? Where might this fail?
8. **Reproducibility**: Everything needed to replicate

## When to Use This Skill

- Planning experiments before implementation
- Reviewing experimental protocols for soundness
- Designing ablation studies
- Setting up benchmarking comparisons
- Ensuring statistical validity of results
- Planning computational resource allocation
