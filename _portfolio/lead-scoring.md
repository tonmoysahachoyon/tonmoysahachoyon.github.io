---
title: "Lead Scoring & Sales Intelligence Pipeline"
excerpt: "Two-stage machine learning pipeline with Random Forest, K-Means clustering, and SHAP interpretability."
collection: portfolio
---

## Overview
Engineered a reproducible, two-stage machine learning pipeline (`train.py`, `score.py`) designed to eliminate feature misalignment between training and real-time scoring passes.

![Lead Scoring Visual](/images/lead-scoring-visual.png)

## Key Highlights
* **Predictive Performance:** Tuned a Random Forest classifier achieving **0.95 precision** and **0.88 recall**.
* **Behavioral Segmentation:** Applied K-Means clustering to partition converted leads into distinct behavioral segments, isolating low-intent cohorts to preserve signal strength.
* **Explainable AI:** Integrated SHAP (SHapley Additive exPlanations) values to translate model outputs into clear, feature-attributed rankings rather than opaque scores.
* **Code Repository:** [GitHub Project](https://github.com/Tonmoy10/leads-score-sales-intelligence)
