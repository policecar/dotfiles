---
description: Set up a quick ML experiment with proper tracking and reproducibility
---

# Quick Experiment Setup

Set up a minimal but rigorous experiment for the user. Include:

1. **Experiment tracking setup**
   - Initialize Weights & Biases or MLflow run
   - Log hyperparameters, code version, command

2. **Reproducibility essentials**
   - Set random seeds (Python, NumPy, PyTorch/TensorFlow)
   - Log library versions (torch, transformers, etc.)
   - Save config/hyperparameters to file

3. **Basic structure**
   - Train/val/test split with proper seeding
   - Training loop with checkpointing
   - Validation metrics logging
   - Save best model

4. **Monitoring**
   - Log loss, metrics, learning rate
   - Save training curves
   - Log system metrics (GPU util, memory)

Ask the user what they're experimenting with, then provide runnable code with these essentials built in.

Be concise - this is meant to be quick to set up while still being rigorous.
