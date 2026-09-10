---
title: "Lead Scoring & Sales Intelligence Pipeline"
excerpt: "A reproducible two-stage ML pipeline combining a Random Forest classifier, K-Means segmentation, and SHAP explanations to produce ranked, explainable lead scores."
collection: portfolio
permalink: /portfolio/lead-scoring/
---

{% include project-styles.html %}

<div class="tags">
  <span class="tag">Python</span>
  <span class="tag">scikit-learn</span>
  <span class="tag">Random Forest</span>
  <span class="tag">K-Means</span>
  <span class="tag">SHAP</span>
</div>

<div class="stat-grid">
  <div class="stat"><span class="num">0.95</span><span class="label">precision</span></div>
  <div class="stat"><span class="num">0.88</span><span class="label">recall</span></div>
  <div class="stat"><span class="num">5</span><span class="label">behavioural segments</span></div>
</div>

<a href="https://github.com/tonmoysahachoyon/leads-score-sales-intelligence" class="btn btn--primary" target="_blank"><i class="fab fa-github"></i> View Code on GitHub</a>

{% assign fig = site.static_files | where: "path", "/images/lead-scoring-visual.png" | first %}
{% if fig %}
![Lead scoring visual](/images/lead-scoring-visual.png)
{% endif %}

## Overview

The project began as an exploratory notebook. I restructured it into a reproducible two-stage pipeline, `train.py` and `score.py`, with shared preprocessing. This resolved a feature misalignment between the training and scoring passes, a common source of silent errors when models move from notebooks into use.

## Pipeline

<div class="flow">
  <span class="step">Shared preprocessing</span><span class="arrow">&rarr;</span>
  <span class="step">train.py: Random Forest</span><span class="arrow">&rarr;</span>
  <span class="step">score.py: scoring</span><span class="arrow">&rarr;</span>
  <span class="step">SHAP attribution</span><span class="arrow">&rarr;</span>
  <span class="step">Ranked lead list</span>
</div>

## Key Highlights

* **Predictive performance:** Tuned a Random Forest classifier to 0.95 precision and 0.88 recall.
* **Behavioural segmentation:** Applied K-Means clustering to split converted leads into five behavioural segments, isolating a low-intent group that would otherwise have diluted the scoring signal.
* **Explainability:** Used SHAP values to attribute each prediction to its dominant feature, turning the model output into a ranked, explainable list rather than an opaque score.

<details class="project-details">
<summary>Why the two-stage structure matters</summary>
<p>When training and scoring code are written separately, they can apply slightly different preprocessing, such as different column orders or encodings. The model then receives inputs that don't match what it was trained on, often without raising an error. Sharing one preprocessing module between both stages removes this failure mode and makes the results reproducible.</p>
</details>
