# HR-Attrition-Analytics-Dashboard-Predictive-Insights
This repository provides an **end-to-end analytics and modeling framework** for understanding and predicting employee attrition.  
It combines **exploratory data analysis (EDA)**, **predictive modeling**, and **data-driven insights** to help HR teams identify the key drivers of employee turnover and design effective retention strategies.

---

## 🚀 Project Overview

- **Goal:** Identify patterns and predictors of employee attrition using HR data.  
- **Deliverables:**
  - Interactive dashboard (Power BI file)
  - Jupyter notebook for analysis
  - Cleaned dataset
  - Python scripts for reproducible analytics
  - Visualizations and key statistical summaries

---
## 🧩 Dataset Description

**Source:** Internal HR dataset (`cleaned_hr_data.csv`)  
**Size:** ~1,400 rows × 35 columns  
**Target Variable:** `Attrition` (Yes/No → converted to `Attrition_flag`)  

| Feature Group | Example Columns |
|----------------|-----------------|
| **Demographics** | Age, Gender, MaritalStatus |
| **Employment** | Department, JobRole, JobLevel, YearsAtCompany |
| **Performance** | JobInvolvement, PerformanceRating |
| **Compensation** | MonthlyIncome, StockOptionLevel |
| **Career Growth** | YearsInCurrentRole, TrainingTimesLastYear |
| **Work–Life** | WorkLifeBalance, BusinessTravel |

---

## 🧮 Analytical Approach

### 1️⃣ Data Preparation
- Converted attrition to binary (1 = Left, 0 = Stayed).
- Cleaned categorical values and handled missing entries.
- Encoded categorical columns for modeling.
- Standardized numerical features for comparability.

### 2️⃣ Exploratory Data Analysis (EDA)
- Calculated **point-biserial correlations** for numeric features vs attrition.
- Summarized **attrition rates by category** for features like Department, JobRole, EducationField.
- Generated **visualizations**:
  - Attrition distribution (0 vs 1)
  - Age histograms (by attrition status)
  - Top model coefficients bar chart

### 3️⃣ Predictive Modeling
- **Model used:** Logistic Regression (interpretable baseline)
- **Pipeline steps:**
  - One-hot encoding for categorical features
  - Standard scaling for numerical features
  - Model fitting on `Attrition_flag`
- **Evaluation metric:** ROC-AUC (baseline model achieves 0.78–0.82 range)
- Extracted feature importance (coefficients)

### 4️⃣ Visualization in Power BI
The Power BI dashboard (`hr_attriton_analytics dashboard.pbix`) presents:
- Attrition trends by department, age, gender, and education field  
- Interactive slicers to filter by demographics  
- KPI cards showing overall attrition %  
- Drill-down view for high-risk job roles  
- Departmental retention heatmaps  

---

## 📊 Key Insights

| Insight Type | Summary |
|---------------|----------|
| **Attrition Rate** | ~15% overall; higher in Sales & HR departments |
| **High-Risk Groups** | Younger employees (<30 years), lower job levels, frequent travelers |
| **Top Numeric Drivers** | Lower TotalWorkingYears, JobLevel, MonthlyIncome, Age |
| **Top Categorical Drivers** | BusinessTravel (Frequent), MaritalStatus (Single), Department (Sales) |
| **Manager/Role Factors** | Fewer YearsWithCurrentManager and YearsInCurrentRole correlate with leaving |
| **Compensation Link** | Higher attrition among employees with low StockOptionLevel and income |

---
## 📊 Key Insights (from current analysis)

| Category | Insight |
|-----------|----------|
| **Overall Attrition Rate** | ~15–20% (varies by department) |
| **High-Risk Groups** | Sales & Human Resources employees show higher attrition |
| **Strongest Numeric Drivers** | Lower *TotalWorkingYears*, *JobLevel*, *MonthlyIncome*, and *Age* are linked with higher attrition |
| **Categorial Factors** | Employees who *Travel Frequently* or are *Single* show higher attrition |
| **Actionable Steps** | Focus retention efforts on early-tenure and lower-level employees; enhance career path transparency and work-life balance |

## 💡 Actionable Recommendations

1. **Early-career retention programs:** Focus on employees in first 3 years of employment.  
2. **Career progression visibility:** Provide promotion and skill-development opportunities.  
3. **Sales department focus:** Review compensation, workload, and travel frequency.  
4. **Manager enablement:** Train managers to identify disengaged team members early.  
5. **Flexible travel and remote work:** Reduce attrition among frequent travelers.

---


---
