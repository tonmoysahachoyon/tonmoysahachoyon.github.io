---
title: "Job Market Trend Analysis via Cloud Data Warehousing"
excerpt: "An automated ELT pipeline from the Adzuna API into Google BigQuery, with dbt transformations and tests and a Power BI dashboard of hiring and salary trends."
collection: portfolio
permalink: /portfolio/job-market-pipeline/
---

{% include project-styles.html %}

<div class="tags">
  <span class="tag">Python</span>
  <span class="tag">Adzuna API</span>
  <span class="tag">Google BigQuery</span>
  <span class="tag">dbt</span>
  <span class="tag">SQL</span>
  <span class="tag">Power BI</span>
</div>

<a href="https://github.com/tonmoysahachoyon/job-market-pipeline" class="btn btn--primary" target="_blank"><i class="fab fa-github"></i> View Code on GitHub</a>

{% assign fig = site.static_files | where: "path", "/images/job-market-dashboard.jpg" | first %}
{% if fig %}
![Power BI dashboard](/images/job-market-dashboard.jpg)
{% endif %}

## Overview

An automated analytics pipeline that tracks job posting volume, hiring activity by company, and salary trends over time.

## Pipeline

<div class="flow">
  <span class="step">Adzuna API</span><span class="arrow">&rarr;</span>
  <span class="step">Raw JSON in BigQuery</span><span class="arrow">&rarr;</span>
  <span class="step">dbt models + tests</span><span class="arrow">&rarr;</span>
  <span class="step">Power BI dashboard</span>
</div>

## Key Highlights

* **Extraction:** Built an automated pipeline against the Adzuna API, loading raw JSON responses into Google BigQuery.
* **Transformation:** Defined SQL transformations and automated data tests with dbt.
* **Visualisation:** Built a Power BI dashboard tracking posting volume, hiring activity by company, and salary trends over time.

<details class="project-details">
<summary>Why load raw data first and transform later?</summary>
<p>Storing the untouched API responses in the warehouse before transforming them means the transformations can be changed or rerun at any time without calling the API again. With dbt, each transformation is a version-controlled SQL model with automated tests, so data quality problems are caught before they reach the dashboard.</p>
</details>
