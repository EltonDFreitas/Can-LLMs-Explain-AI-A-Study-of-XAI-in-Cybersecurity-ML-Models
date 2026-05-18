# Can LLMs Explain AI?  
## A Study of Explainable AI in Cybersecurity Machine Learning Models

This repository contains the implementation, experiments, prompts, datasets preprocessing workflows, explainability pipelines, and evaluation artifacts used in the paper:

> **Can LLMs Explain AI? A Study of Explainable AI in Cybersecurity Machine Learning Models**

---

## Overview

Machine Learning (ML) models are increasingly used in cybersecurity applications such as intrusion detection, malware analysis, and anomaly detection. However, many of these systems operate as black boxes, making their decisions difficult to interpret.

This project investigates whether Large Language Models (LLMs) can reliably support Explainable Artificial Intelligence (XAI) in cybersecurity contexts.

The experiments evaluate:

- Traditional explainability techniques:
  - SHAP
  - LIME

- LLM-based explainability approaches:
  - GPT-5
  - GPT-OSS-20B

The study compares:
1. LLMs used as standalone explainability tools
2. LLMs combined with SHAP/LIME outputs
3. Human perception and interpretability of generated explanations

---

## Main Findings

### Standalone LLM explanations are unreliable
When prompted without SHAP or LIME data, LLMs frequently:
- hallucinated feature importance
- introduced semantic bias
- generated explanations inconsistent with the actual ML model behavior

### SHAP/LIME-grounded prompts improve fidelity
When SHAP and LIME outputs were included in prompts:
- explanations became more coherent
- alignment with feature importance improved significantly
- hallucinations were reduced

### Users preferred LLM-enhanced explanations
In a human-centered evaluation with 38 participants:
- GPT-5 explanations achieved the highest preference rate
- GPT-OSS-20B achieved competitive results
- Raw SHAP/LIME outputs were considered harder to understand

---

## Repository Structure
```text
.
├── datasets/
│   ├── dataset1/
│   │   └── Network_logs.csv
│   ├── dataset2/
│   │   └── cybersecurity_intrusion_data.csv
│   └── dataset3/
│       └── KDDTrain+20.txt
│
├── notebooks/
│   ├── dataset1_experiments.ipynb
│   ├── dataset2_experiments.ipynb
│   └── dataset3_experiments.ipynb
├── requirements.txt
└── README.md
