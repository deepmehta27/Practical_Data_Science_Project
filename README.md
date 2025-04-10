# Optimizing Hospital Readmission Reduction Using Patient Clustering

This repository contains the code, documentation, and materials for the data science project **"Optimizing Hospital Readmission Reduction Using Patient Clustering."** Developed as part of the Practical Data Science course at Pace University, this project leverages advanced clustering and predictive modeling techniques to identify high-risk patient subgroups, ultimately guiding targeted interventions to reduce hospital readmissions and improve patient outcomes.

---

## Project Overview

Hospital readmissions significantly drive up costs while also impacting patient satisfaction and overall quality of care. Traditional methods often detect the likelihood of readmission without addressing the root causes. This project applies a data-driven approach:
- **Data Collection & Cleaning:** Utilizes the Diabetes 130-US Hospitals dataset (1999–2008) from the UCI Machine Learning Repository, comprising approximately 100,000 records of patient admissions.
- **Patient Clustering:** Uses unsupervised clustering techniques to segment patients into subgroups based on their healthcare utilization, clinical severity, demographics, and medication data.
- **Predictive Modeling:** Converts the identified clusters into binary targets (one-vs-rest) and applies Random Forest classifiers to understand the specific drivers of readmission within each subgroup.
- **Explainability:** Implements SHAP for model interpretability, identifying the top factors contributing to subgroup membership.
- **Strategic Insights:** Provides actionable business and technical recommendations aimed at reducing readmission rates by targeting high-risk populations.

---

## Project Objectives

- **Reduce Hospital Readmissions:** Identify patient subgroups with high risk and propose targeted interventions.
- **Understand Underlying Factors:** Move beyond prediction to explain the underlying clinical and behavioral drivers contributing to readmission.
- **Enhance Patient Outcomes:** Deliver data-driven insights to support improved care coordination and resource allocation.
- **Support Decision Making:** Provide healthcare providers with actionable strategies based on comprehensive exploratory and predictive analytics.

---

## Data Description

**Data Source:**  
- Diabetes 130-US Hospitals (1999–2008) dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008).

**Dataset Highlights:**
- **Size:** ~100,000 records (each representing a hospital admission)
- **Attributes:** Patient demographics (age, gender), admission details (length of stay, diagnoses), medication counts and changes, and readmission status.
- **Cleaning & Preprocessing:**  
  - Removed duplicates and entries with excessive missing values.
  - Replaced “?” with NaN and dropped columns with >40% missing data (e.g., weight, payer code).
  - Engineered a binary target variable indicating 30-day readmission status.

Detailed steps can be found in the [Appendix](#appendix) section.

---

## Exploratory Data Analysis (EDA)

The EDA phase investigated key trends and patterns in the data:
- **Readmission Distribution:** Approximately 47.7% of diabetic admissions were readmitted within 30 days.
- **Age-Group Risk:** Patients aged 50-70 exhibited the highest readmission rates.
- **Utilization Patterns:** Frequent prior hospital visits and high medication counts were observed in early readmissions.
- **Racial Disparities:** Notable differences exist between racial groups, with African American patients showing a higher rate of readmission compared to Caucasian patients.

Visualizations and detailed breakdowns are included in the notebooks and supporting slides.

---

## Modeling Methods

The modeling strategy integrates unsupervised clustering with a supervised prediction approach:
- **Clustering:**  
  - Patients were segmented using unsupervised techniques (e.g., HDBSCAN) based on clinical and utilization features.
- **Predictive Modeling:**  
  - The unsupervised clusters were transformed into binary targets.
  - A Random Forest classifier (using one-vs-rest scheme) was trained to predict subgroup membership.
- **Model Explainability:**  
  - SHAP analysis was applied to elucidate the role of key features such as total visits, medication count, and clinical severity in driving readmission risk.

This dual approach not only highlights the critical characteristics of high-risk groups but also provides actionable insights into the drivers behind readmissions.

---

## Findings & Business Recommendations

### Key Findings:
- **Distinct Subgroups:** The clustering exercise identified three distinct patient profiles:
  - **Low Engagement:** Minimal outpatient visits and medication changes.
  - **Moderate Utilization:** Balanced healthcare use with potential for escalation.
  - **High Risk:** Frequent outpatient visits, high clinical severity scores, and intensive healthcare utilization.
- **Driver Insights:** SHAP analysis pinpointed key factors (e.g., follow-up compliance, severity score) that differentiate these groups.

### Business Recommendations:
- **High Risk Group:**  
  - Intensify care coordination and regular medication review.
  - Deploy case management teams.
- **Low Engagement Group:**  
  - Implement proactive patient outreach and follow-up protocols.
- **Moderate Utilization Group:**  
  - Monitor consistently with digital engagement tools (telehealth, mobile reminders).

### Technical Next Steps:
- **Algorithm Refinement:** Further optimize clustering parameters and explore alternate dimensionality reduction techniques.
- **Pilot Programs:** Implement targeted pilot interventions and continuously monitor performance.
- **Data Enrichment:** Integrate additional data sources (e.g., social determinants of health) to enhance model accuracy.

---

## Installation & Usage

### Prerequisites

- **Python 3.7+**  
- **Recommended Packages:** (See [requirements.txt](./requirements.txt) for a detailed list)
  - numpy
  - pandas
  - scikit-learn
  - hdbscan
  - matplotlib
  - SHAP
  - jupyter

### Installation Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/deepmehta27/Practical_Data_Science_Project.git
   cd Practical_Data_Science_Project
   ```

2. **Install Dependencies:**

   Create a virtual environment (optional but recommended) and install the packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebooks:**

   Launch Jupyter Notebook or JupyterLab:

   ```bash
   jupyter notebook
   ```

   Open and run the notebooks in the `notebooks/` directory to explore the data analysis, modeling, and findings.

---

## Contributing

Contributions are welcome! Feel free to fork the repository and open pull requests. Please ensure that any additions or modifications are covered by appropriate tests and documentation.

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## Contact

For any inquiries, suggestions, or contributions, please contact:

**Deep Manish Mehta**  
Email: [dm29655n@pace.edu](mailto:dm29655n@pace.edu)

---

This project was developed as part of the Practical Data Science curriculum at Pace University, aiming to provide actionable insights for reducing hospital readmissions through advanced data science techniques.

