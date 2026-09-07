---
title: "Lead Scoring & Sales Intelligence Pipeline"
excerpt: "Two-stage machine learning pipeline with Random Forest, K-Means clustering, and SHAP interpretability."
collection: portfolio
---

## Overview
Engineered a reproducible, two-stage machine learning pipeline (`train.py`, `score.py`) designed to eliminate feature misalignment between training and real-time scoring passes.

## Key Highlights
* **Predictive Performance:** Tuned a Random Forest classifier achieving **0.95 precision** and **0.88 recall**.
* **Behavioral Segmentation:** Applied K-Means clustering to partition converted leads into distinct behavioral segments, isolating low-intent cohorts to preserve signal strength.
* **Explainable AI:** Integrated SHAP (SHapley Additive exPlanations) values to translate model outputs into clear, feature-attributed rankings rather than opaque scores.
* **Code Repository:** [GitHub Project](https://github.com/tonmoysahachoyon/leads-score-sales-intelligence)
```

*   **Job Market Trend Analysis Pipeline**
    *   Create file: `_portfolio/job-market-pipeline.md`
    *   Content:
```markdown
---
title: "Job Market Trend Analysis via Cloud Data Warehousing"
excerpt: "Automated extraction pipeline using the Adzuna API, Google BigQuery, dbt, and Power BI."
collection: portfolio
---

## Overview
Built an automated analytics and data warehousing pipeline to track hiring patterns, posting volume, and salary trends across technical job sectors.

## Key Highlights
* **ETL Architecture:** Automated data ingestion from the Adzuna API, staging raw JSON responses directly into **Google BigQuery**.
* **Data Transformation:** Defined modular SQL models, testing suites, and transformation workflows using **dbt**.
* **Visualization:** Designed an interactive Power BI dashboard tracking market dynamics and compensation benchmarks across companies.
* **Code Repository:** [GitHub Project](https://github.com/Tonmoy10/job-market-pipeline)
```

Commit each file, wait for the GitHub build to turn green, and check your live portfolio page.
