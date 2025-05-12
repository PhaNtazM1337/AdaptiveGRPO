# GRPO with Adaptive Sampling for Mathematical Reasoning
A research project implementing adaptive sampling in GRPO (Group Relative Policy Optimization) to automatically focus on harder problems without pre-labeled difficulty scores.

## Overview
This project uses an `IterableDataset` that dynamically adjusts sampling probabilities based on:
- **Average accuracy reward**: Problems with lower average accuracy are considered harder and sampled more frequently
- **Reward variance**: Problems with low variance (similar rewards across responses) provide less useful gradient updates and are deprioritized

By reducing sampling probability for easy problems and those with low reward variance, the model automatically concentrates on challenging and useful problems over time, creating an implicit curriculum learning effect.
