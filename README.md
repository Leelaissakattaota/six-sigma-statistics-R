# 📊 Six Sigma: Basic Statistical Analysis in R

![R](https://img.shields.io/badge/Language-R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![RStudio](https://img.shields.io/badge/IDE-RStudio-75AADB?style=for-the-badge&logo=rstudio&logoColor=white)
![Methodology](https://img.shields.io/badge/Methodology-Six%20Sigma%20DMAIC-2E7D32?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Healthcare%20Analytics-02779B?style=for-the-badge)
![Course](https://img.shields.io/badge/Course-Coursera%20Guided%20Project-0056D2?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

This project applies **Six Sigma statistical methodology** to real-world 
healthcare data — specifically analyzing **patient Time to Admit (TTA)** 
metrics across an Accident & Emergency (A&E) department using R. 

It demonstrates a complete end-to-end statistical workflow — from raw 
data loading and wrangling, through descriptive statistics, sampling, 
visualization, distribution generation, and distribution fitting — 
showing how quality engineers and data analysts identify and solve 
process inefficiency problems in healthcare.

**Domain:** Healthcare Process Quality  
**Methodology:** Six Sigma DMAIC  
**Dataset:** Patient admission records (PatientID, TimeToAdmit, Category, PatientAge)  
**Language:** R  

---

## 📂 Dataset

| Column | Description |
|---|---|
| `PatientID` | Unique patient identifier |
| `TimeToAdmit` | Time taken to admit patient (minutes) |
| `Category` | A&E category — Major A&E, Speciality, Minor Injury |
| `PatientAge` | Age of the patient |

---

## 🛠️ Tech Stack

| Tool / Library | Purpose |
|---|---|
| **R** | Core programming language |
| **RStudio** | Development environment |
| **fitdistrplus** | Distribution fitting (Normal, Exponential, Log-Normal) |
| **nortest** | Anderson-Darling normality test |
| **Base R stats** | Descriptive stats, sampling, confidence intervals |
| **Base R graphics** | Histograms, Boxplots, Normal curve overlay |

---

## 🚀 Project Workflow — 6 Tasks

### ✅ Task 1 — Load & Explore Data
- Loaded patient dataset (`data.csv`) into RStudio
- Explored data structure, types, dimensions
- Subset data by injury category (e.g. `Minor Injury`)
- Inspected head, tail, and row slices of dataset

```r
dt = read.csv("~/data.csv")
dt1 = subset(dt, Category == "Minor Injury")
nrow(dt); head(dt); tail(dt)
```

---

### ✅ Task 2 — Calculate Centering & Spread
- **Centering:** Mean, Median, Mode of `TimeToAdmit`
- **Spread:** Standard Deviation, Variance, IQR, SPAN, RANGE
- Custom `SummaryStats()` function for full statistical summary

```r
mean(x); median(x); Mode(x)
sd(x); IQR; SPAN; RANGE
summary(dt)
```

---

### ✅ Task 3 — Statistical Sampling & Confidence Intervals
- Applied **Central Limit Theorem** — collected 1,000 samples of size 50
- Computed **Standard Error of the Mean (SEM)**
- Calculated **95%, 90%, and 99% Confidence Intervals**

```r
p = SampledMeans(x, 50, 1000)
se = sd(x)/sqrt(50)
mean(x) - 1.96 * se  # 95% CI Lower
mean(x) + 1.96 * se  # 95% CI Upper
```

---

### ✅ Task 4 — Data Visualization
- **Histogram** with Normal Curve overlay
- **Boxplots** — overall and by A&E category (Major A&E, Speciality, Minor Injury)
- **Pareto Chart** for defect/category prioritization

```r
hist(x, col = "gold2", freq = FALSE)
curve(dnorm(x, mean=mean(x), sd=sd(x)), col="red", lwd=2, add=TRUE)
boxplot(TimeToAdmit ~ Category, dt, col = "gold2")
ParetoPlot(dt$Category, "A&E Category")
```

---

### ✅ Task 5 — Generate & Compare Distributions
Generated and compared 4 distribution types to understand process behavior:

| Distribution | Function | Parameters |
|---|---|---|
| Uniform | `runif()` | min=5, max=10 |
| Normal | `rnorm()` | Mean=10, SD=2 |
| Exponential | `rexp()` | Lambda=1/5 |
| Log-Normal | `rlnorm()` | MeanLog, SDLog |

---

### ✅ Task 6 — Distribution Fitting
- Used **Anderson-Darling test** (`nortest`) to test normality
- Used **Kolmogorov-Smirnov test** via `fitdistrplus` to fit distributions
- Fitted Normal, Exponential, and Log-Normal distributions to TTA data

```r
ad.test(x)           # Anderson-Darling normality test
d = fitdist(x, "norm")   # Fit Normal distribution
d = fitdist(x, "exp")    # Fit Exponential distribution
d = fitdist(x, "lnorm")  # Fit Log-Normal distribution
ad.test(log(x))      # Normality after log transform
```

---

## ⚙️ How to Run

**Step 1 — Install required packages:**
```r
install.packages("fitdistrplus")
install.packages("nortest")
```

**Step 2 — Set working directory and run:**
```r
setwd("path/to/six-sigma-statistics-R")
source("Six Sigma Basic Statistics.R")
```

---

## 📈 Key Insights

- Identified that **TimeToAdmit** data follows a **Log-Normal distribution** 
  rather than Normal — confirmed via Anderson-Darling and KS tests
- **Minor Injury** category showed highest variation in admission times
- **95% Confidence Interval** for mean TimeToAdmit computed from 
  1,000 random samples of size 50
- Pareto chart revealed which A&E categories contributed most 
  to admission delays

---

## 🎓 Skills Demonstrated

- Six Sigma DMAIC framework — Measure & Analyze phases
- Descriptive statistics — Mean, Median, Mode, SD, IQR, SPAN
- Statistical sampling & Central Limit Theorem
- Confidence interval calculation (90%, 95%, 99%)
- Distribution fitting & goodness-of-fit testing
- Data visualization — Histogram, Boxplot, Pareto Chart
- Healthcare data analysis in R

---

## 📜 Certifications

| Certification | Issuer | Platform |
|---|---|---|
| IBM Data Science Professional Certificate | IBM | Coursera |
| IBM Generative AI Professional Certificate | IBM | Coursera |
| IBM Agentic AI with RAG Certificate | IBM | Coursera |
| IBM RAG and Agentic AI Professional Certificate | IBM | Coursera |

---

## 🤝 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Leela%20A-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/leela-a)
[![Gmail](https://img.shields.io/badge/Gmail-attotaleelaissak@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:attotaleelaissak@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Leelaissakattaota-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Leelaissakattaota)
