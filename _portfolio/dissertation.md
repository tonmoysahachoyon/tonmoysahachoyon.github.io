---
title: "Synthetic Fraud Pattern Modelling & Anomaly Detection"
excerpt: "Master's dissertation in partnership with XYNQ, building a 100,000-record synthetic data pipeline using CTGANs and LLMs with rigorous statistical validation."
collection: portfolio
---

## Overview
Conducted as my MSc dissertation in Data Science at the University of Aberdeen in collaboration with XYNQ, this research addressed a scenario where no real training data existed. I engineered an end-to-end synthetic data generation pipeline to model fraud patterns and anomalies in digital music uploads.

## Methodology & Implementation
* **Generative Modeling:** Utilized Conditional Tabular GANs (CTGAN) to model complex tabular distributions seeded from prompt-engineered LLM outputs.
* **Ablation Studies:** Tested scaling capabilities by training CTGAN on a 5,000-row subset and generating a validated 100,000-row dataset.
* **Rigorous Statistical Validation:** Evaluated marginal distribution drift and structural fidelity against baseline data using:
  * Kolmogorov-Smirnov (KS) Distance
  * Total Variation Distance (TVD)
  * Spearman Correlation
  * Cramér's V

## Results
A Random Forest classifier trained entirely on the validated synthetic data achieved an overall F1 score of **0.85** and ROC-AUC scores of **0.96, 0.93, and 0.89** across fraud categories, proving that generative models can safely produce privacy-compliant data for robust anomaly detection systems.
