# Demographic Risk Assessment & Population Forecasting of India

<p align="center">
  <img src="assets/banner.svg" alt="Project Banner" width="100%">
</p>


<p align="center">
  <img src="assets/banner.png" alt="Demographic Risk Assessment & Population Forecasting of India" width="100%">
  <img src="https://img.shields.io/badge/Data-UN_WPP_2024-green?style=for-the-badge" alt="UN Data">
  <img src="https://img.shields.io/badge/Framework-Jupyter_Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
  <img src ="https://img.shields.io/badge/DRDO-SSPL%20Winter%20Internship-blue?style=for-the-badge">

</p>


## Project Overview

This project was completed during my **Winter Internship at DRDO – Solid State Physics Laboratory (SSPL), New Delhi**.

The study investigates India's demographic transition using the **United Nations World Population Prospects (WPP 2024)** dataset and develops machine learning-based forecasting models to analyze long-term population dynamics, aging trends, workforce sustainability, and demographic risks.

The project combines demographic analysis, feature engineering, risk modeling, and machine learning to understand how India's population structure is expected to evolve from **1950 to 2100**.

---

## Objectives

* Analyze India's historical and projected population trends.
* Study fertility decline, life expectancy growth, and demographic transition.
* Quantify aging-related and workforce-related demographic risks.
* Develop composite demographic risk indices.
* Build machine learning models for long-term population forecasting.
* Evaluate the importance of demographic indicators in future population prediction.
* Generate policy-oriented insights for sustainable demographic planning.

---

## Datasets

### 1. UN WPP 2024 Demographic Indicators

Contains annual demographic indicators including:

* Total Population
* Birth Rate (CBR)
* Death Rate (CDR)
* Fertility Rate (TFR)
* Life Expectancy
* Median Age
* Population Growth Rate
* Migration Statistics

### 2. UN WPP 2024 Population by Age Group

Contains population counts across:

* Young Population (0–14 years)
* Working Age Population (15–64 years)
* Elderly Population (65+ years)

Used for age-structure analysis and dependency ratio computation.

---

## Methodology

### Workflow

1. Data Collection
2. Data Cleaning & Validation
3. Exploratory Data Analysis
4. Demographic Feature Engineering
5. Risk Index Construction
6. Forecast Modeling
7. Model Evaluation
8. Policy Analysis

---

## Exploratory Data Analysis

### Population Growth Analysis

Analyzed India's population trajectory from 1950–2100.

Key observation:

* Population grows from approximately 0.35 billion in 1950
* Peaks near 1.70 billion around 2060
* Gradually declines afterward

---

### Population Growth Rate Analysis

Population growth rate declines continuously:

* Above 2% during the 1960s–1980s
* Around 1% near 2020
* Approaches 0% by 2060
* Becomes negative after 2060

This indicates the completion of India's demographic transition.

---

### Fertility Analysis

Total Fertility Rate (TFR):

* ~6 children per woman in the 1950s
* Falls below replacement level (~2.1)
* Stabilizes near 1.7 by 2100

Key Drivers:

* Female education
* Urbanization
* Family planning access
* Improved healthcare
* Delayed marriages

---

### Life Expectancy Analysis

Life expectancy increases from:

* ~41 years in 1950
* ~71 years in 2024
* ~85 years by 2100

This reflects improvements in:

* Healthcare
* Nutrition
* Sanitation
* Disease control

---

### Median Age Analysis

Median age increases from:

* ~20 years in 1950
* ~28 years in 2024
* ~48 years by 2100

Implication:

India gradually transitions from a young nation to an aging society.

---

## Age Structure Analysis

The second dataset was used to create age-group aggregates.

### Young Population

Age Groups:

* 0–4
* 5–9
* 10–14

### Working Population

Age Groups:

* 15–64

### Elderly Population

Age Groups:

* 65+

---

### Dependency Ratio

Dependency Ratio =

(Young Population + Elderly Population)
/ Working Population

Findings:

* High dependency in the 1950s
* Lowest dependency around 2030–2040
* Increasing dependency after 2050 due to aging

This highlights India's demographic dividend window.

---

## Demographic Risk Assessment

Three custom demographic risk indices were developed.

### Aging Risk Index

Measures aging burden using:

* Median Age
* Elderly Population Share

Represents:

* Pension pressure
* Healthcare burden
* Elderly support requirements

---

### Workforce Risk Index

Measures shrinking labor force risk using:

* Working-age population share

Represents:

* Labor shortages
* Economic productivity concerns

---

### Population Pressure Index

Measures stress on:

* Infrastructure
* Resources
* Urban systems

Uses:

* Population size
* Growth rate

---

### Composite Demographic Risk Score

Combines:

* Aging Risk
* Workforce Risk
* Population Pressure

into a single indicator.

Key finding:

India's demographic risk remains relatively low historically but rises steadily after 2030 due to population aging.

---

## Machine Learning Models

### Model 1: Facebook Prophet

Input:

* Historical population data

Characteristics:

* Time-series forecasting
* Trend extrapolation
* Univariate approach

Observation:

Prophet continued extending historical growth trends and significantly overestimated future population.

---

### Model 2: Random Forest Regressor

Features:

* Birth Rate
* Death Rate
* Fertility Rate
* Life Expectancy
* Median Age
* Population Growth Rate
* Migration

Observation:

Performed better than Prophet but struggled to capture long-term demographic transition.

---

### Model 3: Random Forest + Age Structure

Additional Features:

* Young Population
* Working Population
* Elderly Population
* Dependency Ratio

Observation:

Most realistic model.

Age structure information allowed the model to capture:

* Population momentum
* Workforce dynamics
* Aging transition

---

## Feature Importance Analysis

The most influential predictors were:

1. Death Rate (CDR)
2. Fertility Rate (TFR)
3. Birth Rate (CBR)
4. Life Expectancy
5. Working Population
6. Young Population
7. Elderly Population

Key Insight:

Population dynamics are primarily driven by fertility and mortality, while age structure significantly improves forecasting quality.

---

## Major Findings

### Finding 1

India's population is projected to peak around 2060.

### Finding 2

Population growth becomes negative after approximately 2060.

### Finding 3

Fertility falls below replacement level and stabilizes near 1.7.

### Finding 4

Life expectancy exceeds 85 years by 2100.

### Finding 5

Median age nearly doubles, indicating rapid aging.

### Finding 6

Dependency ratio rises sharply after 2050.

### Finding 7

Workforce growth slows significantly after 2040.

### Finding 8

Demographic dividend peaks around 2030–2040.

### Finding 9

Age structure variables substantially improve forecasting performance.

### Finding 10

Population aging emerges as the dominant long-term demographic challenge.

---

## Policy Recommendations

### Workforce Development

* Expand skill development programs
* Increase labor productivity
* Encourage workforce participation

### Healthy Aging

* Strengthen geriatric healthcare
* Expand elderly care infrastructure
* Improve pension planning

### Human Capital Investment

* Improve education quality
* Promote female workforce participation
* Enhance public healthcare

### Data-Driven Governance

* Build demographic monitoring systems
* Integrate AI-based forecasting into planning

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Prophet
* Jupyter Notebook

---

## Repository Structure

```text
.
├── DRDO.ipynb
├── DRDO_Report.pdf
├── README.md
├── requirements.txt
├── assets/
│   ├── banner.svg
│   └── methodology.svg
├── WPP2024_Demographic_Indicators_Medium.csv.gz
└── WPP2024_PopulationByAge5GroupSex_Medium.csv.gz
```

##

---

## Author

**Karthikeyan Pandita**

B.Tech – Data Science & Business Systems

DRDO–SSPL Winter Intern

---

## Acknowledgement

This project was completed as part of the Winter Internship Programme at **Solid State Physics Laboratory (SSPL), DRDO, New Delhi**, with the objective of applying data science and machine learning techniques to demographic forecasting and strategic risk assessment.
