---
description: Check if ML code follows reproducibility best practices
---

# Reproducibility Check

Analyze the codebase for reproducibility issues. Check for:

## 1. Random Seed Management
- [ ] Seeds set for random, numpy, torch/tf
- [ ] Seeds documented or configurable
- [ ] Seeds set before data loading
- [ ] Seeds set before model initialization

## 2. Dependencies & Versions
- [ ] requirements.txt or environment.yml exists
- [ ] Specific versions pinned (not >=)
- [ ] Python version documented
- [ ] CUDA/GPU dependencies documented

## 3. Data Handling
- [ ] Data splits saved or deterministic
- [ ] Data preprocessing documented
- [ ] Data augmentation uses fixed seeds
- [ ] Dataset versions tracked

## 4. Model & Training
- [ ] Model architecture fully specified
- [ ] Initialization method documented
- [ ] Hyperparameters logged or saved
- [ ] Training procedure documented

## 5. Experiments & Results
- [ ] Experiment configs saved
- [ ] Multiple runs with different seeds
- [ ] Results include error bars/std
- [ ] Models/checkpoints saved

## 6. Code & Environment
- [ ] Code versioned (git)
- [ ] Docker/container definition available
- [ ] Hardware specs documented
- [ ] Runtime/resource requirements noted

## 7. Documentation
- [ ] README with setup instructions
- [ ] Command to reproduce main results
- [ ] Expected outputs documented
- [ ] Known issues/limitations noted

After checking, provide:
1. Issues found with severity (critical, important, minor)
2. Specific recommendations for fixes
3. Example code for implementing fixes
