# SELF: A Robust Singular Value and Eigenvalue Approach for LLM Fingerprinting


This repository contains the implementation for the paper "**SELF**: A Robust **S**ingular Value and **E**igenvalue Approach for **L**LM **F**ingerprinting". 

## Introduction
Conducting effective Intellectual Property (IP) forensics to safeguard Large Language Models (LLMs) represents a critical challenge. Existing fingerprinting methods are often susceptible to false claim attacks, weight manipulations, or suffer from high false positive rates. 

To address these limitations, we propose **SELF**, a novel intrinsic weight-based fingerprinting scheme. By applying Singular Value Decomposition (SVD) and Eigenvalue Decomposition (EVD) on a specially constructed matrix derived from LLM attention weights, SELF extracts a unique, scalable, and transformation-invariant fingerprint.

### Key Features
* **Input-Independent:** Completely eliminates dependency on input data, inherently resisting false claim attacks.
* **Highly Robust:** Maintains strong resilience against various downstream modifications, including fine-tuning, pruning, and quantization.
* **Transformation-Invariant:** Effectively defends against permutation and linear-mapping attacks.
* **Scalable & Compact:** Produces a lightweight fingerprint (approximately 10³ elements) regardless of the target model's total parameter size.

---

## Getting Started

To quickly set up the required dependencies, run the following commands:

### 1. Environment Setup

```bash
# Create and activate the conda environment
conda env create -f self.yml
conda activate self
```

### 2. Quick Evaluation
We provide Jupyter Notebooks to demonstrate the core functionality and performance of SELF.

- **Effectiveness & Robustness Evaluation**:
Run `self.ipynb` to evaluate the fingerprinting effectiveness on target models including Qwen2.5-7B and Llama2-7B. This notebook demonstrates SELF's ability to distinguish between related and unrelated models.

- **Large-scale Benchmark Testing**:
Run `leafbench_eval.ipynb` to reproduce the performance of SELF on the large-scale LeafBench dataset.