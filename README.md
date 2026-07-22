# Student Performance Data Analysis

An end-to-end exploratory data analysis project on the Student Performance dataset (UCI / Kaggle), built with Python, Pandas, NumPy, and Matplotlib in a dedicated virtual environment, using Jupyter Notebook.

## Dataset

- Source: UCI Student Performance Dataset (via Kaggle)
- 395 students across two schools (GP: 349, MS: 46)
- 33 columns covering demographics, family background, lifestyle, and grades (G1, G2, G3)

## Tech Stack

Python, Pandas, NumPy, Matplotlib (OOP interface), Jupyter Notebook, venv

## Project Phases

1. **Load & Inspect** — reviewed structure, types, and summary stats
2. **Data Cleaning** — checked nulls, duplicates, inconsistent labels, and validated ranges; flagged absence outliers and treated G3=0 as "Incomplete" rather than "Fail"
3. **Feature Engineering** — created Total, Average, Performance, Pass/Fail, ParentEdu, TotalAlc
4. **EDA** — used groupby, value_counts, and correlation checks to find early patterns
5. **GroupBy Analysis** — combined variables (e.g., sex x studytime) to test if patterns held up
6. **Pivot Tables** — reshaped comparisons into grids for clearer pattern reading
7. **Insights & Conclusions** — synthesized findings, flagging correlation-vs-causation traps
8. **Visualization** — built histograms, bar charts, and a grouped bar chart in Matplotlib

## Key Findings

- Past failures is the strongest predictor of final grades (avg G3 drops from 11.25 to 5.69 across failure counts)
- Study time and parental education both show positive trends with grades
- A persistent sex-based performance gap exists that isn't explained by studytime, goout, or failures
- The sex gap is concentrated at GP school and nearly disappears at MS school
- Romantic relationships associate with lower grades for both sexes, more so for females
- School support correlates with lower grades due to selection bias, not causation
- Alcohol consumption showed no reliable relationship with final grades

## Setup

```bash
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install pandas numpy matplotlib jupyter
jupyter notebook student_analysis.ipynb
```

## What This Project Taught Me

Beyond Pandas and Matplotlib syntax, this project pushed me to think like an analyst: checking sample sizes before trusting an average, separating correlation from causation, and reporting honest results even when they didn't match my assumptions.

## About Me

Built on a foundation in C++ and Object-Oriented Programming, now applied to Python and data analysis. Currently expanding into SQL and statistical testing.
