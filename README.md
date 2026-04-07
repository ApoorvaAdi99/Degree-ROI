# Degree ROI Analysis

> **Is a bachelor's degree worth it financially?** This project explores that question using survey data from 173 college majors, analyzing salary distributions, employment rates, gender representation, and the relevance of a degree across different fields.

---

## Overview

This project was completed as part of **ISE-201** and uses data from the **American Community Survey (ACS) 2010–2012**, sourced from the [FiveThirtyEight GitHub repository](https://github.com/fivethirtyeight/data/tree/master/college-majors).

The analysis is conducted entirely in **R** using an R Markdown document that produces a reproducible PDF report.

---

## Research Questions

1. Do degrees offer a return on investment?
2. Which fields are the most economically rewarding?
3. Are high-paying jobs truly dependent on having a college degree?
4. What is the gender distribution across majors and top-earning fields?
5. How do high-paying roles compare to lower-paying ones within the same industry?

---

## Key Findings

- **Engineering** has the highest median salary (~$57K mean), while **Psychology & Social Work** is the lowest (~$30K).
- **Engineering and Computers & Mathematics** have more college-degree-required jobs than non-college jobs — unlike Arts, Business, and Humanities.
- Employment rates are high across all fields (>90%), but differ significantly by major (ANOVA: p = 0.000591).
- A PCA + linear regression model explains **84% of salary variance** (R² = 0.844), with major category, total graduates, part-time prevalence, and unemployment rate being key factors.
- Fields with higher female representation (Health, Psychology) tend to have lower median salaries.

---

## Methods

| Technique | Purpose |
|---|---|
| Data cleaning & imputation | Handled missing values using category-group means |
| Exploratory data analysis | Bar charts, violin plots, boxplots via ggplot2 |
| One-way ANOVA | Tested whether employment rate differs by major category |
| PCA | Reduced dimensionality; identified top variance-driving factors |
| Linear regression on PCs | Identified principal components that predict median salary |

---

## Repository Structure

```
college-majors-financial-analysis/
├── projectFinalSubmission.Rmd   # Main R Markdown source file
├── projectFinalSubmission.pdf   # Rendered report
├── recent-grads.csv             # Dataset (from FiveThirtyEight)
└── README.md
```

---

## How to Run

1. Clone this repository
2. Open `projectFinalSubmission.Rmd` in RStudio
3. Make sure the following packages are installed:

```r
install.packages(c("tidyverse", "corrplot", "knitr"))
```

4. Place `recent-grads.csv` in the same directory as the `.Rmd` file
5. Click **Knit** to render the PDF report

---

## Dataset

**Source:** FiveThirtyEight — [College Majors](https://github.com/fivethirtyeight/data/tree/master/college-majors)  
**Survey:** American Community Survey 2010–2012 Public Use Microdata Series  
**Observations:** 173 majors across 16 categories  
**Key variables:** Median salary, unemployment rate, share of women, college vs. non-college jobs

---

## Author

**Apoorva Adimulam** 

