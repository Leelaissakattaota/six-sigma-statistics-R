# Six Sigma: Basic Statistical Analysis in R

![R](https://img.shields.io/badge/Language-R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![RStudio](https://img.shields.io/badge/IDE-RStudio-75AADB?style=for-the-badge&logo=rstudio&logoColor=white)
![Methodology](https://img.shields.io/badge/Methodology-Six%20Sigma%20DMAIC-2E7D32?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Healthcare%20Analytics-0277BD?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## Project Overview

This project applies Six Sigma statistical methodology to real-world healthcare data, specifically analyzing patient **Time to Admit** metrics using the R programming language. It demonstrates a complete end-to-end statistical workflow — from raw data wrangling all the way through distribution fitting — showing how quality engineers and data analysts identify and solve process inefficiency problems in regulated industries.

**Domain:** Healthcare Process Quality  
**Methodology:** Six Sigma DMAIC  
**Language:** R  

---

## Problem Statement

Hospitals struggle with inconsistent patient admission times. This project uses Six Sigma statistical tools to identify patterns and outliers in admission data, measure process spread and central tendency, and validate statistical assumptions required for process capability analysis.

---

## Tech Stack

![Language](https://img.shields.io/badge/Language-R-276DC3?style=flat-square&logo=r&logoColor=white)
![IDE](https://img.shields.io/badge/IDE-RStudio-75AADB?style=flat-square&logo=rstudio&logoColor=white)
![Fitting](https://img.shields.io/badge/Library-fitdistrplus-orange?style=flat-square)
![Testing](https://img.shields.io/badge/Library-nortest-red?style=flat-square)
![Viz](https://img.shields.io/badge/Visualization-Base%20R%20Graphics-blue?style=flat-square)

---

## Project Structure
```
six-sigma-statistics-R/
│
├── Six Sigma Basic Statistics.R      # Main analysis script
├── data.csv                          # Healthcare patient dataset
└── README.md
```

---

## Workflow

**Task 1 — Data Wrangling**  
Imported the dataset and subset the data by injury category such as Minor Injury. Inspected data types, structure, and missing values to ensure data quality before analysis.

**Task 2 — Descriptive Statistics**  
Calculated centering metrics including Mean, Median, and Mode. Calculated spread metrics including Standard Deviation, Variance, IQR, and SPAN to understand process variation.

**Task 3 — Statistical Sampling**  
Applied the Central Limit Theorem by drawing 1,000 random samples from the dataset. Computed 95% Confidence Intervals to estimate true process parameters.

**Task 4 — Data Visualization**  
Created Histograms with Normal Curve overlays, Boxplots segmented by injury category, and Pareto Charts for defect prioritization and root cause identification.

**Task 5 — Probability Distributions**  
Generated and compared four distribution types — Uniform, Normal, Exponential, and Log-Normal — to understand which best describes the patient admission process.

**Task 6 — Distribution Fitting**  
Used Anderson-Darling and Kolmogorov-Smirnov goodness-of-fit tests to identify the best statistical model for patient Time to Admit data.

---

## How to Run

Install the required R packages before running the script:
```r
install.packages("fitdistrplus")
install.packages("nortest")
```

Then open RStudio, set your working directory to the project folder, and run:
```r
setwd("path/to/six-sigma-statistics-R")
source("Six Sigma Basic Statistics.R")
```

---

## Key Learnings

Applied Six Sigma DMAIC framework using statistical computing in R. Understood how distribution shape directly impacts process capability decisions. Practiced hypothesis testing using goodness-of-fit tests on real healthcare data. Built professional-grade visualizations suitable for process analysis reporting in regulated industries.

---

## Certifications

| Certification | Issuer | Platform |
|---|---|---|
| IBM Data Science Professional Certificate | IBM | Coursera |
| IBM Generative AI Professional Certificate | IBM | Coursera |
| IBM Agentic AI with RAG Certificate | IBM | Coursera |
| IBM RAG and Agentic AI Professional Certificate | IBM | Coursera |

---

## Connect with Me

**Leela A.** — AI/ML Engineer | Data Science Enthusiast  
Bengaluru, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Leela%20A-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/leela-a)
[![GitHub](https://img.shields.io/badge/GitHub-Leelaissakattaota-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Leelaissakattaota)
[![Gmail](https://img.shields.io/badge/Gmail-attotaleelaissak@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:attotaleelaissak@gmail.com)
