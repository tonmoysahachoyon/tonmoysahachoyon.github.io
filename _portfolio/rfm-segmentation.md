---
title: "Customer Segmentation via RFM Modelling & K-Means"
excerpt: "Log-scaled Recency, Frequency, and Monetary features and K-Means clustering to find behavioural customer groups, including 1,000+ inactive accounts and a high-value segment."
collection: portfolio
permalink: /portfolio/rfm-segmentation/
---

{% include project-styles.html %}

<div class="tags">
  <span class="tag">Python</span>
  <span class="tag">pandas</span>
  <span class="tag">scikit-learn</span>
  <span class="tag">K-Means</span>
  <span class="tag">Feature engineering</span>
</div>

<div class="stat-grid">
  <div class="stat"><span class="num">4</span><span class="label">behavioural segments</span></div>
  <div class="stat"><span class="num">1,000+</span><span class="label">inactive accounts identified</span></div>
  <div class="stat"><span class="num">3</span><span class="label">engineered RFM features</span></div>
</div>

<a href="https://github.com/tonmoysahachoyon/rfm-customer-segmentation" class="btn btn--primary" target="_blank"><i class="fab fa-github"></i> View Code on GitHub</a>

{% assign fig = site.static_files | where: "path", "/images/rfm-clusters.png" | first %}
{% if fig %}
![Customer segmentation clusters](/images/rfm-clusters.png)
{% endif %}

## Overview

Starting from raw transactional data, I derived Recency, Frequency, and Monetary (RFM) features for each customer and used unsupervised learning to segment the customer base.

## Pipeline

<div class="flow">
  <span class="step">Raw transactions</span><span class="arrow">&rarr;</span>
  <span class="step">RFM feature engineering</span><span class="arrow">&rarr;</span>
  <span class="step">Log scaling</span><span class="arrow">&rarr;</span>
  <span class="step">K-Means clustering</span><span class="arrow">&rarr;</span>
  <span class="step">Segment profiles</span>
</div>

## Key Highlights

* **Feature engineering:** Derived RFM metrics from raw transactions and applied logarithmic scaling to correct right skew before clustering.
* **Segmentation:** Grouped customers into four behavioural segments using K-Means.
* **Findings:** Identified over 1,000 inactive accounts and a distinct high-value segment.

<details class="project-details">
<summary>Why log scaling before clustering?</summary>
<p>Frequency and Monetary values are usually heavily right-skewed: a few customers buy far more than everyone else. K-Means relies on Euclidean distance, so without transformation those extreme customers dominate the clustering. Log scaling compresses the long tail, so clusters reflect genuine behavioural differences rather than a handful of outliers.</p>
</details>
