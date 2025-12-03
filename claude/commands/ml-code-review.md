---
description: Review ML code for correctness, performance, and best practices
---

# ML Code Review

Perform a thorough code review focused on ML-specific concerns.

## Review Checklist

### Correctness
- [ ] **Math/logic correctness**: Are calculations correct? Off-by-one errors?
- [ ] **Shape handling**: Tensor shapes correct? Broadcasting issues?
- [ ] **Loss function**: Appropriate for the task? Correctly implemented?
- [ ] **Metrics**: Calculated correctly? Edge cases handled?
- [ ] **Data leakage**: Test data isolated from training?
- [ ] **Gradient flow**: Any operations that block gradients?

### Performance & Efficiency
- [ ] **Unnecessary operations**: Redundant computations in loops?
- [ ] **Memory efficiency**: Excessive tensor copies? In-place ops possible?
- [ ] **Batch processing**: Operations vectorized appropriately?
- [ ] **Data loading**: Efficient data pipeline? Prefetching?
- [ ] **GPU utilization**: Proper device placement? Transfer minimized?

### Numerical Stability
- [ ] **Overflow/underflow**: Log-space for probabilities?
- [ ] **Division by zero**: Epsilon added where needed?
- [ ] **NaN/Inf handling**: Checked and handled appropriately?
- [ ] **Numerical precision**: Float32 vs float64 considered?

### ML Best Practices
- [ ] **Determinism**: Random seeds set appropriately?
- [ ] **Hyperparameters**: Configurable, not hardcoded?
- [ ] **Validation**: Proper train/val/test separation?
- [ ] **Monitoring**: Key metrics logged?
- [ ] **Checkpointing**: Model saving implemented?
- [ ] **Error handling**: Graceful handling of training failures?

### Code Quality
- [ ] **Type hints**: Function signatures typed?
- [ ] **Documentation**: Complex logic explained?
- [ ] **Testing**: Unit tests for key functions?
- [ ] **Modularity**: Functions focused, reusable?
- [ ] **Magic numbers**: Constants defined as named variables?

### Common ML Bugs
- [ ] **Data preprocessing**: Same preprocessing train/test?
- [ ] **Batch norm**: Handled correctly in train vs eval mode?
- [ ] **Dropout**: Disabled during evaluation?
- [ ] **Learning rate**: Appropriate scale? Scheduler working?
- [ ] **Loss averaging**: Properly accounting for batch sizes?

## Output

For each issue found, provide:
1. **Location**: File and line number
2. **Issue**: What's wrong
3. **Impact**: Severity and consequences
4. **Fix**: Specific recommendation with code example

Focus on issues that could cause incorrect results or significant performance problems. Flag potential bugs even if not certain.
