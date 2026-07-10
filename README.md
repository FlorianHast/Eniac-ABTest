# Eniac Website Redesign – A/B Testing Analysis

## Project Overview

This project is a **fictional business case study** developed to demonstrate an end-to-end A/B testing workflow for an e-commerce scenario.

The analysis evaluates the impact of different website versions on user engagement and conversion behavior for **Eniac, a fictional e-commerce company**.

The goal is to determine whether different website designs lead to statistically significant differences in customer interaction and to provide a data-driven recommendation based on the test results.

Using Python, exploratory data analysis, and statistical hypothesis testing, four website variants (A, B, C, and D) were compared to identify meaningful differences in user behavior.

---

## Business Context

Eniac is a fictional e-commerce company testing multiple website designs to improve customer engagement and conversion performance.

The company wants to answer:

> **Do different website designs significantly influence user behavior, and which version should be selected for implementation?**

This case study simulates a real-world data analytics workflow where business decisions are supported by controlled experiments and statistical evidence.

---

Dataset

The dataset contains user interaction data from four website variants:

Version	Description
A	Website version A (Control Group: 'SHOP NOW' button in white)
B	Website version B ('SHOP NOW' button in red)
C	Website version C ('SHOP NOW' changed to 'SEE DEALS')
D	Website version D ('SHOP NOW' changed to 'SEE DEALS' and color red)

Each version contains information about:

Number of visitors
Click interactions
User actions on the website
Conversion-related metrics
Project Objectives

The analysis aims to:

Compare user engagement across different website versions
Calculate conversion metrics
Perform statistical hypothesis testing
Determine whether observed differences are statistically significant
Provide a data-driven recommendation for the website redesign
Methodology
1. Data Preparation

The analysis included:

Loading and combining datasets
Extracting relevant metrics from raw interaction data
Cleaning and transforming variables
Preparing contingency tables for statistical testing
2. Exploratory Data Analysis

The following metrics were analyzed:

Number of visitors per version
Number of clicks
Click-through rates (CTR)

The conversion rate was calculated as:

[
Conversion\ Rate = \frac{Conversions}{Visitors}
]

Visual comparisons were used to identify differences between website versions.

Statistical Testing
Chi-Square Test of Independence

To evaluate whether website version and user behavior are independent, a Chi-Square test was applied.

Hypotheses

Null hypothesis (H₀):

There is no significant difference in user behavior between website versions.

Alternative hypothesis (HA):

At least one website version produces significantly different user behavior.

Significance level:

[
\alpha = 0.1
]

Multiple Comparison Correction

Since four website versions create multiple pairwise comparisons, a Bonferroni correction was applied to reduce the risk of false positives.

The adjusted significance level was calculated as:

[
\alpha_{adjusted} = \frac{\alpha}{number\ of\ comparisons}
]

Results

Pairwise Chi-Square tests showed the following results:

Comparison	p-value	Result
Bonferroni alpha: 0.0167

A vs. B -> 2.6731e-15: A and B differ significantly
A vs. C -> 4.6484e-01: A and C show no significant difference
A vs. D -> 3.0809e-33: A and D differ significantly
B vs. C -> 6.9555e-18: B and C differ significantly
B vs. D -> 2.3573e-05: B and D differ significantly
C vs. D -> 6.4505e-37: C and D differ significantly
Key Finding

The analysis indicates that:

Version A and C show no statistically significant difference
All other combinations show statistically significant differences

This suggests that user behavior differs strongly depending on the website version.

Business Recommendation

Based on the statistical analysis:

Versions B and D significantly differ from the other tested variants
Version C does not provide a measurable improvement compared to version A
The final implementation decision should consider both:
statistical significance
practical business impact (conversion rate improvement)

A/B testing results should therefore be combined with conversion performance and business KPIs before selecting the final website design.

Technologies Used
Python
Pandas
NumPy
SciPy
Matplotlib
Seaborn
Google Colab
Repository Structure
Eniac-AB-Test/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── eniac_A.csv
│   ├── eniac_B.csv
│   ├── eniac_C.csv
│   └── eniac_D.csv
│
├── notebooks/
│   └── Eniac_ABTesting.ipynb
│
└── reports/
    └── figures/
How to Run the Project

Clone the repository:

git clone https://github.com/FlorianHast/Eniac-ABTest.git

Install dependencies:

pip install -r requirements.txt

Launch Jupyter Notebook:

jupyter notebook

Open:

notebooks/Eniac_AB_Test.ipynb
Author

Florian Hastreiter
Junior Data Analyst | Analytics Engineer

GitHub:
https://github.com/FlorianHast
