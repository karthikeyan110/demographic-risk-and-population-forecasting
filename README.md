# Demographic Risk Assessment & Population Forecasting of India

<p align="center">
  <img src="assets/banner.svg" alt="Project Banner" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/DRDO-SSPL_Delhi-blue?style=for-the-badge&logo=defense&logoColor=white" alt="DRDO SSPL">
  <img src="https://img.shields.io/badge/Python-3.13-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Data-UN_WPP_2024-green?style=for-the-badge" alt="UN Data">
  <img src="https://img.shields.io/badge/Framework-Jupyter_Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

---

## 🌟 Interactive Documentation Companion
We have built a premium, interactive HTML documentation companion dashboard:
👉 **[Open Interactive Readme Dashboard (HTML)](./interactive_readme.html)**

This dashboard features:
- 🎛️ **Live Demographic Risk Simulator**: Adjust parameters (Aging, Workforce, Pressure weights) in real-time to watch the Composite Risk Index update live.
- 📊 **Animated Forecast Models Comparison**: Interactively compare the curves for UN projections, Prophet, and Random Forest models.
- ⚙️ **Modular Execution Guide**: Interactive workspace setup commands.

---

## 📖 Introduction & Objectives

This repository contains the source code, preprocessed datasets, compilation pipelines, and generated technical report for the project **"Demographic Risk Assessment and Population Forecasting of India Using Machine Learning and United Nations Population Data"**, conducted under the **Winter Internship Programme** at **Solid State Physics Laboratory (SSPL), Defence Research and Development Organisation (DRDO), New Delhi**.

The objective of this research is two-fold:
1. **Develop Composite Demographic Risk Indices** to evaluate India's long-term workforce viability, population aging pressure, and environmental sustainability from 1950 to 2100.
2. **Implement and Optimize Machine Learning Models** (Prophet, Random Forest, and a specialized Random Forest with Age Structure features) to forecast future demographic transitions and evaluate the role of population momentum.

---

## 🛠️ Methodological Workflow

The project extracts data from the **United Nations World Population Prospects (WPP 2024)** medium variant dataset. It performs structural feature extraction to track demographic changes across time.

<p align="center">
  <img src="assets/methodology.svg" alt="Methodology Flowchart" width="100%">
</p>

---

## 🧮 Composite Demographic Risk Indices

To analyze the strategic security and economic risk profile of India, we define four composite indexes:

1. **Aging Risk Index (ARI)**:
   $$ARI = \frac{MedianAgePop}{50} \times 0.6 + \frac{ElderlyPct}{30} \times 0.4$$
   *Measures the burden of geriatric healthcare and social security systems.*

2. **Workforce Risk Index (WRI)**:
   $$WRI = 1.0 - WorkingPct$$
   *Quantifies the contraction of the primary productive economic cohort.*

3. **Population Pressure Index (PPI)**:
   $$PPI = \frac{TPopulation1July}{1,700,000} \times 0.7 + \frac{PopGrowthRate + 3}{6} \times 0.3$$
   *Examines resources, environment, and logistical pressure limits.*

4. **Composite Risk Score (CRS)**:
   $$CRS = ARI \times 0.3 + WRI \times 0.4 + PPI \times 0.3$$
   *An aggregate score of the demographic risk profile.*

---

## 🧠 Machine Learning Models & Metrics

We evaluate three distinct machine learning methodologies against the United Nations cohort-component benchmark:

| Model | Core Principle | MAE (Millions) | RMSE (Millions) | Key Characteristics |
| :--- | :--- | :---: | :---: | :--- |
| **Facebook Prophet** | Univariate Trend Extrapolation | *High* | *High* | Extrapolates historical growth without upper bounds, overestimating size. |
| **Random Forest (Basic)** | Decision Tree Regressor on Vital Rates | 185.3 | 243.1 | Bounded by training set maximum; flatlines past historical peaks. |
| **RF + Age Structure** | Regressor augmented with Age Cohorts | **18.7** | **24.5** | **Excellent fit**; captures demographic inertia and population momentum. |

---

## 📂 Repository Organization & Cell Compilation

The notebook is divided into 25 technical sections, built dynamically from modular components to keep scripts cleaner and maintainable.

<details>
<summary>📂 Click to expand the 25 Technical Sections</summary>

1. **Cover Page**: Project titles, author profile, and institutional affiliation.
2. **Certificate**: Document verification by SSPL guides.
3. **Acknowledgement**: Appreciation to DRDO, SSPL, and UN DESA.
4. **Abstract**: High-level study brief and key metrics.
5. **Table of Contents**: Structured roadmap of report cells.
6. **Introduction**: Conceptual overview of Demographic Transition Theory.
7. **Problem Statement**: Merging ML with traditional forecasting.
8. **Objectives**: Detailed research goals.
9. **Literature Review**: Prior work summary (Lee-Carter, Prophet, etc.).
10. **Dataset Description**: UN WPP columns (TFR, CBR, CDR, NetMigrations).
11. **Methodology**: Block diagram and pipeline execution flow.
12. **Data Preprocessing**: Scaling, clean-up, and dataset alignment.
13. **Exploratory Data Analysis (EDA)**: Historical indicators trend charts.
14. **Age Structure Analysis**: Historical and future five-year cohort breakdown.
15. **Demographic Risk Assessment**: Modeling ARI, WRI, PPI, and CRS.
16. **Population Forecasting**: Trend baseline calculations.
17. **Machine Learning Models**: Implementation details for Prophet and Random Forest.
18. **Model Comparison**: Metric comparison charts and prediction error.
19. **Feature Importance**: Gini index scoring of vital rates and age brackets.
20. **Results and Findings**: 10 primary insights of India's population trends.
21. **Discussion**: Analysis of structural momentum and generational lags.
22. **Limitations**: Domain boundary conditions and spatial limitations.
23. **Future Scope**: Extensions (Bayesian forecasting, Deep learning).
24. **Conclusion**: Strategic recommendations and summary.
25. **References**: Academic bibliography.
</details>

---

## 🚀 How to Compile and Run

1. **Clone the repository** and navigate to the project directory:
   ```powershell
   # Open your terminal in the workspace directory
   cd "d:/DRDO 01"
   ```

2. **Initialize python environment** and install requirements:
   ```powershell
   pip install -r requirements.txt
   ```

3. **Compile the Notebook**:
   Execute the master compilation script to assemble the modular code blocks:
   ```powershell
   python build_notebook.py
   ```
   This compiles `DRDO.ipynb` automatically.

4. **Run or View Output**:
   Open the notebook in Jupyter Lab/Notebook:
   ```powershell
   jupyter notebook DRDO.ipynb
   ```
   Or simply open **`DRDO_Report.html`** or **`DRDO_Report.pdf`** to read the pre-rendered full technical report!

---

**© Defence Research and Development Organisation (DRDO) — Solid State Physics Laboratory (SSPL), New Delhi**
*Submitted in partial fulfillment of the requirements for the DRDO-SSPL Winter Internship.*
