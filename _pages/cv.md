---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p><a href="{{ base_path }}/files/CV.pdf" class="btn btn--primary" target="_blank"><i class="fa fa-download"></i> Download Full CV (PDF)</a></p>

## Research Interests
* Generative AI and synthetic data generation
* Trustworthy evaluation of generative models, especially when little or no real ground truth exists
* Statistical model validation and fraud / anomaly detection
* Machine learning and computational statistics

## Education
* **M.Sc. in Data Science (Commendation)**, University of Aberdeen *(Jan 2025 – Jun 2026)*
  * *Dissertation:* Synthetic Data Generation and Model Validation (in partnership with XYNQ)
  * *Supervisor:* Prof. M. Carmen Romano
  * *Relevant modules:* Machine Learning, Advanced Statistics and Special Applications, Image Analysis, Data Visualization
* **B.Sc. in Computer Science and Engineering (Summa Cum Laude, CGPA 3.99/4.00)**, American International University-Bangladesh *(Sep 2019 – May 2023)*
  * *Thesis:* Comparing CNN, SVM, and ensemble classifiers for medical image classification, with a focus on failure modes across approaches

## Honours & Awards
* **Academic Excellence Scholarship** — American International University-Bangladesh
* **Summa Cum Laude** — American International University-Bangladesh (2023)
* **Dean's List** — American International University-Bangladesh (four semesters)

## Key Research & Technical Projects
* **Synthetic Data Generation & Model Validation** *(MSc Dissertation, with XYNQ)*
  * Tackled fraud detection in music streaming where no real labelled training data existed, building a baseline dataset from prompt-engineered LLM outputs grounded in limited market data and explicit domain assumptions.
  * Used CTGAN to expand a 5,000-row seed subset into 100,000 synthetic rows, and ran a feature ablation study to prioritise features in the generation pipeline.
  * Measured fidelity to the baseline distribution with KS distance, Total Variation Distance, Spearman correlation, and Cramér's V.
  * Trained a Random Forest on the synthetic data, reaching F1 = 0.85 and ROC-AUC of 0.96 / 0.93 / 0.89 across three fraud categories on held-out data.
  * Key limitation: fidelity and performance are measured relative to the assumption-grounded baseline rather than real fraud data; validating against real samples or domain-expert review is the natural next step.
* **Lead Scoring & Sales Intelligence Pipeline** — [GitHub](https://github.com/tonmoysahachoyon/leads-score-sales-intelligence)
  * Refactored a notebook into a reproducible two-stage pipeline (`train.py`, `score.py`) with shared preprocessing; Random Forest (0.95 precision, 0.88 recall), K-Means segmentation, and SHAP-based explanations.
* **Customer Segmentation via RFM & K-Means** — [GitHub](https://github.com/tonmoysahachoyon/rfm-customer-segmentation)
  * Engineered log-scaled RFM features from transactional data and identified four behavioural segments, including 1,000+ inactive accounts and a distinct high-value group.
* **Job Market Trend Analysis Pipeline** — [GitHub](https://github.com/tonmoysahachoyon/job-market-pipeline)
  * Automated extraction from the Adzuna API into Google BigQuery, with dbt transformations and tests, and a Power BI dashboard.

## Work Experience
* **Data & Operations Lead**, Family Restaurant Business, Dhaka, Bangladesh *(Jan 2024 – Nov 2024)*
  * Analysed sales and inventory data to guide stocking and scheduling, reducing stock waste by ~30%.
  * Designed and deployed a point-of-sale system, saving roughly two hours of daily admin time.
* **Junior Software Developer Intern**, DeshiIT, Dhaka, Bangladesh *(Jan 2023 – Apr 2023)*
  * Restructured a MongoDB schema across 10,000+ records, reducing query response times by ~40%; built MERN-stack features.

## Technical Skills
* **Generative AI & ML:** CTGAN, synthetic data generation, LLM prompt engineering, scikit-learn, Random Forest, K-Means, SHAP
* **Statistical Validation:** KS distance, Total Variation Distance, Spearman correlation, Cramér's V
* **Programming:** Python, R, SQL, JavaScript, Wolfram Mathematica
* **Data Engineering & Tools:** Google BigQuery, dbt, ETL pipelines, Power BI, Tableau, pandas, NumPy, Git

## English Language
* **IELTS Academic:** Overall Band 8.0

## References
Available on request.
