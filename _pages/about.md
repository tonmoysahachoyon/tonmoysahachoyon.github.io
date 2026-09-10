---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
.focus-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 1em; margin: 1em 0 1.5em; }
.focus-card { border: 1px solid #e0e0e0; border-left: 4px solid #52adc8; border-radius: 6px; padding: 0.9em 1em; font-size: 0.85em; transition: box-shadow 0.2s, transform 0.2s; }
.focus-card:hover { box-shadow: 0 4px 14px rgba(0,0,0,0.08); transform: translateY(-2px); }
.focus-card h4 { margin: 0 0 0.4em; font-size: 1em; }
.focus-card p { margin: 0; }
.updates { list-style: none; padding-left: 0; font-size: 0.9em; }
.updates li { padding: 0.35em 0; border-bottom: 1px dashed #e5e5e5; }
.updates .date { display: inline-block; min-width: 6.5em; font-weight: bold; color: #52adc8; }
details { border: 1px solid #e0e0e0; border-radius: 6px; padding: 0.6em 1em; margin: 1em 0; font-size: 0.9em; }
details summary { cursor: pointer; font-weight: bold; }
</style>

**Open to PhD opportunities.** I am seeking a PhD position in machine learning, particularly on trustworthy generative models and the evaluation of synthetic data. [View my CV](/cv/) or [get in touch](mailto:choyontonmoysaha@gmail.com).
{: .notice--info}

I am a data scientist working on generative AI and the validation problem underneath it: **how far can we trust a model's output when little or no real ground truth exists to check it against?** I recently completed an MSc in Data Science at the University of Aberdeen with Commendation. My dissertation, in partnership with the UK company XYNQ, built and statistically validated a synthetic data pipeline for fraud detection in a setting where no real training data was available.

## Research Focus

<div class="focus-grid">
  <div class="focus-card">
    <h4>Synthetic Data Generation</h4>
    <p>Combining LLMs and CTGAN to build realistic tabular datasets when real data is unavailable, scarce, or sensitive.</p>
  </div>
  <div class="focus-card">
    <h4>Statistical Validation</h4>
    <p>Measuring fidelity with complementary tests (KS distance, TVD, Spearman, Cramér's V), each targeting a different failure mode.</p>
  </div>
  <div class="focus-card">
    <h4>Trustworthy Evaluation</h4>
    <p>Understanding what validation against a synthetic or assumption-based baseline can and cannot tell us about real-world performance.</p>
  </div>
</div>

## Questions I Want to Work On

* How can synthetic data be validated when the reference distribution is itself uncertain or partly assumed?
* How reliably can small seed datasets be expanded, and where does the expansion break down?
* What evaluation protocols let models trained on synthetic data be trusted in real deployment?

<details>
<summary>MSc dissertation at a glance</summary>

<ul>
  <li><strong>Problem:</strong> Fraud detection in music streaming with no real labelled training data.</li>
  <li><strong>Approach:</strong> A baseline dataset from prompt-engineered LLM outputs grounded in limited market data and domain assumptions, expanded with CTGAN from a 5,000-row seed to 100,000 rows.</li>
  <li><strong>Validation:</strong> Fidelity to the baseline measured with four statistical tests, plus a feature ablation study.</li>
  <li><strong>Result:</strong> A Random Forest trained on the synthetic data reached F1 = 0.85 and ROC-AUC of 0.96 / 0.93 / 0.89 across three fraud categories.</li>
  <li><strong>Open question:</strong> All evaluation is relative to an assumption-grounded baseline. Validating against real data is the natural next step, and the one I want to pursue in a PhD.</li>
</ul>
</details>

## Selected Projects

* [**Synthetic Data Generation & Model Validation**](/portfolio/synthetic-data-dissertation/): MSc dissertation with XYNQ
* [**Lead Scoring & Sales Intelligence Pipeline**](/portfolio/lead-scoring/): Random Forest, K-Means, and SHAP explanations
* [**Customer Segmentation via RFM & K-Means**](/portfolio/rfm-segmentation/): behavioural clustering of transactional data
* [**Job Market Trend Analysis**](/portfolio/job-market-pipeline/): Adzuna API, BigQuery, dbt, and Power BI

## Updates

<ul class="updates">
  <li><span class="date">Sep 2026</span> Applying for PhD positions in machine learning and data science.</li>
  <li><span class="date">Jun 2026</span> Completed MSc Data Science (Commendation), University of Aberdeen.</li>
  <li><span class="date">2025–26</span> MSc dissertation on synthetic data generation and validation with XYNQ (UK).</li>
  <li><span class="date">May 2023</span> BSc Computer Science and Engineering, Summa Cum Laude (CGPA 3.99/4.00), AIUB.</li>
</ul>
