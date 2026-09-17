# Employee Attrition Prediction & Analysis

End-to-end Data Science project: exploratory data analysis, machine learning, and an interactive Tableau dashboard to identify employees at risk of leaving the company.


![Dashboard](Screenshot%202026-09-17%20162938.png)
---

## 📌 Business Problem

Employee attrition is costly. Every employee departure means lost knowledge, recruitment costs, and additional training time.

HR teams often react after employees resign instead of identifying risks early.

**Goal:** Understand why employees leave and build a machine learning model that identifies employees at higher risk of leaving.

### Key Questions

- What factors are most associated with employee attrition?
- Do overtime and business travel increase resignation risk?
- Can machine learning predict employees who are likely to leave?

---

## 📊 Dataset

**Source:** IBM HR Analytics Employee Attrition Dataset (Kaggle)

- 1,470 employees
- 35 features
- Target variable: `Attrition` (Yes/No)

Class distribution:

- Yes: 16.1%
- No: 83.9%

---

# 🛠️ Methodology

## 1. Data Cleaning

Removed unnecessary columns with no analytical value:

- EmployeeCount
- Over18
- StandardHours
- EmployeeNumber

Checked for:

- Missing values
- Duplicate rows
- Data types

---

## 2. Exploratory Data Analysis (EDA)

Performed:

### Univariate Analysis

Analyzed:

- Age distribution
- Income
- Departments
- Attrition balance

### Bivariate Analysis

Studied relationships between attrition and:

- Overtime
- BusinessTravel
- JobRole
- JobSatisfaction

### Multivariate Analysis

Included:

- Correlation analysis
- Interaction effects

Example:

Employees with low job satisfaction and overtime showed a significantly higher attrition rate.

---

# ⚙️ Feature Engineering

Applied:

- Binary Encoding:
  - Gender
  - OverTime

- Ordinal Encoding:
  - BusinessTravel

- One-Hot Encoding:
  - Department
  - EducationField
  - JobRole
  - MaritalStatus

Dataset split:

- Training: 80%
- Testing: 20%

Used:

- Stratified train/test split
- StandardScaler
- Prevented data leakage

---

# 🤖 Machine Learning Models

Compared different classification models:

| Model | Precision | Recall | F1 Score |
|---|---|---|---|
| Logistic Regression | 0.36 | 0.66 | 0.46 |
| Random Forest | 0.50 | 0.06 | 0.11 |
| HistGradientBoosting | 0.59 | 0.36 | 0.45 |

Because the dataset is imbalanced, accuracy alone was not considered a reliable metric.

---

# 🚀 Model Improvement

Applied:

- GridSearchCV
- Class weighting
- Threshold tuning

## Final Model

**Tuned Logistic Regression**

The business objective prioritizes Recall to identify as many potential employees at risk as possible.

### Final Performance

- Recall: 70%
- Precision: 38%
- ROC-AUC: ~0.80

---

# 🔑 Key Findings

## Factors Increasing Attrition Risk 🔴

- Overtime employees:
  - Attrition increased from 10.4% to 30.5%

- Frequent business travel:
  - Attrition increased from 8% to 25%

- More previous companies worked for

- Longer time since last promotion

- Lower job satisfaction

---

## Factors Reducing Attrition Risk 🟢

- Higher job satisfaction

- Stock option participation

- Longer experience and tenure

---

# 💡 Recommendations for HR

1. Monitor overtime workload.
2. Review promotion opportunities.
3. Improve employee incentives.
4. Support frequent travelers.
5. Use predictive models as an early-warning system.

---

# ⚠️ Limitations

- Dataset represents a single snapshot in time.
- Correlation does not prove causation.
- Model predictions should support HR decisions, not replace human judgment.

---

# 📈 Tableau Dashboard

Interactive dashboard built using Tableau Public.

Includes:

- Attrition KPIs
- Attrition analysis by department and job role
- Overtime impact
- High-risk employee identification

Dashboard Link:

[View Interactive Tableau Dashboard](https://public.tableau.com/app/profile/.66268614/viz/dashboard_attrition/Dashboard?publish=yes)

---

# 🧰 Tech Stack

## Programming

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Visualization

- Tableau Public

## Environment

- Google Colab
- Jupyter Notebook

---

# 📁 Repository Structure

```text
HR-Employee-Attrition-Prediction

├── README.md
├── HR_Attrition_Analysis.ipynb
├── HR_Employee_Attrition.csv
├── HR_Attrition_Dashboard_Export.csv
├── Tableau_Dashboard.twbx
└── images
    └── dashboard.png
```

---

# 👤 Author

**Mohammed Hamed Alzahrani**

🎓 Data Science Student at Umm Al-Qura University

🔗 GitHub:
https://github.com/mohmedawifi
