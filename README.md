# Optimizing Hospital Readmission Reduction Using Patient Clustering

**Author:** Deep Manish Mehta  
**Date:** April 29, 2025  
**Course:** Practical Data Science – MS in Data Science, Pace University

---

## Project Overview

Hospital readmissions pose significant challenges by driving up healthcare costs and reducing patient satisfaction. Traditional predictive models often lack explainability regarding the underlying causes of readmissions. This project introduces an innovative unsupervised learning framework that not only identifies hidden, high-risk patient subgroups but also explains the key factors driving these outcomes. The ultimate goal is to inform targeted interventions that can reduce readmission rates.

---

## Project Goal

- **Develop an unsupervised learning framework** to cluster patients based on healthcare utilization and clinical severity.
- **Transform clustering results** into actionable insights using explainable AI techniques.
- **Support strategic decision-making** for reducing hospital readmissions through targeted interventions.

---

## Methodology

1. **Data Cleaning & Preprocessing**
   - Replace missing values and remove duplicates.
   - Drop irrelevant or redundant columns.
   - Encode categorical variables and engineer additional features such as total visits, outpatient ratio, and severity score.

2. **Exploratory Data Analysis (EDA)**
   - Visualize data distributions and relationships (e.g., readmission status, age groups, race, gender).
   - Create correlation matrices to understand feature interactions.

3. **Clustering with HDBSCAN**
   - Scale features and perform PCA for dimensionality reduction.
   - Apply HDBSCAN to identify patient subgroups, handling noise points appropriately.

4. **Interpretation with SHAP**
   - Convert unsupervised clusters into binary targets.
   - Train Random Forest classifiers in a one-vs-rest framework.
   - Use SHAP analysis to determine key features driving each patient subgroup.

5. **Model Evaluation**
   - Validate clusters with cross-validation scores, train/test accuracies, and silhouette scores.
   - Generate detailed profiles for each cluster (Low Engagement, Moderate Utilization, High Risk).

---

## Notebook Structure

- **Section 1:** Data Exploration and Cleaning  
  _Includes data loading, cleaning steps, and initial EDA visualizations._
  
- **Section 2:** Feature Engineering  
  _Transforms raw data into features suitable for clustering and subsequent modeling._

- **Section 3:** Clustering and Dimensionality Reduction  
  _Applies HDBSCAN on scaled data and visualizes the clusters using PCA._

- **Section 4:** Cluster Evaluation and SHAP Analysis  
  _Evaluates the performance of clustering models and provides detailed subgroup profiles using SHAP._

- **Section 5:** Business Insights and Recommendations  
  _Summarizes findings in non-technical language and outlines actionable business strategies._

- **Appendix:**  
  _Contains detailed technical evidence, performance metrics, additional visualizations (e.g., heatmaps), and code snippets for further reference._

---

## Quick Start

To begin, ensure all required libraries are installed:

```python
!pip install pandas numpy matplotlib seaborn scikit-learn hdbscan shap
```

Then, load and preprocess the data as described in Section 1. For full details, refer to the subsequent cells in this notebook.

---

This markdown provides a clear entry point to the notebook, setting the stage for a detailed exploration of the data science project and its implications for reducing hospital readmissions.
