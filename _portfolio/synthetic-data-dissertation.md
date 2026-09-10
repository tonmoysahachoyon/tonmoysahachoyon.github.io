---
title: "Synthetic Data Generation & Model Validation"
excerpt: "MSc dissertation with XYNQ (UK): an LLM + CTGAN pipeline that generated 100,000 synthetic records for music-streaming fraud detection where no real training data existed, validated with four statistical tests."
collection: portfolio
permalink: /portfolio/synthetic-data-dissertation/
---

{% include project-styles.html %}

<div class="tags">
  <span class="tag">MSc Dissertation</span>
  <span class="tag">University of Aberdeen</span>
  <span class="tag">In partnership with XYNQ (UK)</span>
  <span class="tag">Supervisor: Prof. M. Carmen Romano</span>
</div>

<div class="stat-grid">
  <div class="stat"><span class="num">100,000</span><span class="label">synthetic rows generated</span></div>
  <div class="stat"><span class="num">5,000</span><span class="label">row seed subset</span></div>
  <div class="stat"><span class="num">0.85</span><span class="label">overall F1 score</span></div>
  <div class="stat"><span class="num">4</span><span class="label">statistical fidelity tests</span></div>
</div>

## The Problem

Fraud detection in music streaming needs labelled examples of fraud, but in this project **no real training data was available at all**. The question was whether a realistic, useful dataset could be built from scratch, and how its quality could be checked without real data to compare against.

## Approach

<div class="flow">
  <span class="step">Market data + domain assumptions</span><span class="arrow">&rarr;</span>
  <span class="step">Prompt-engineered LLM baseline</span><span class="arrow">&rarr;</span>
  <span class="step">CTGAN expansion</span><span class="arrow">&rarr;</span>
  <span class="step">Statistical validation</span><span class="arrow">&rarr;</span>
  <span class="step">Random Forest evaluation</span>
</div>

* **Baseline construction:** Built a baseline dataset from prompt-engineered LLM outputs, grounded in the limited market data available and in explicit domain assumptions.
* **Generative expansion:** Used CTGAN (Conditional Tabular GAN) to expand the baseline into a full synthetic dataset.
* **Scalability test:** Trained CTGAN on a 5,000-row subset and generated 100,000 rows, to test whether a small seed dataset could be reliably expanded.
* **Feature ablation study:** Measured which input features most influenced model performance, and used the result to prioritise features in the generation pipeline.

## Statistical Validation

Each test targets a different way synthetic data can go wrong:

| Test | What it checks |
|---|---|
| Kolmogorov–Smirnov distance | Shift in each feature's marginal distribution |
| Total Variation Distance | Overall difference between distributions |
| Spearman correlation | Whether dependencies between features are preserved |
| Cramér's V | Association structure between categorical features |

## Results

A Random Forest classifier trained on the synthetic data and evaluated on held-out data reached:

<div class="stat-grid">
  <div class="stat"><span class="num">0.85</span><span class="label">overall F1</span></div>
  <div class="stat"><span class="num">0.96</span><span class="label">ROC-AUC, category 1</span></div>
  <div class="stat"><span class="num">0.93</span><span class="label">ROC-AUC, category 2</span></div>
  <div class="stat"><span class="num">0.89</span><span class="label">ROC-AUC, category 3</span></div>
</div>

<details class="project-details">
<summary>Limitations and what comes next</summary>
<p>All fidelity scores and classifier results are measured relative to the assumption-grounded baseline, not against real fraud data. They show that CTGAN reproduced the baseline faithfully and that the resulting data supports a learnable classification task. They do not yet show how closely either matches real-world fraud behaviour.</p>
<p>The natural next steps are validation against a small sample of real data, review by domain experts, and methods for quantifying uncertainty in the baseline itself. This question, how to validate synthetic data when the reference distribution is partly assumed, is the one I want to pursue in a PhD.</p>
</details>
