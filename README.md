# BIS_Assignment - Diabetes Readmission Analysis: Predicting 30-Day Hospital Returns

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Kavithma-Dharmathilake/BIS_Assignment_Data_Analytics_Process_and_Interpretation/blob/main/Notebook_file.ipynb)

---

## 📌 Project Overview

This project analyzes a dataset containing 10 years (1999–2008) of clinical records from 130 US hospitals to identify factors influencing **early patient readmission (within 30 days)**. Reducing readmissions is critical in healthcare as they drive up hospital costs, negatively impact quality ratings, and affect financial incentives linked to insurance reimbursements.

The primary goal of this analysis is to answer: *Which patient, clinical, and hospital factors influence 30-day readmission among diabetic patients, and can we identify those at highest risk?*.

## ⚙️ The Analytical Process

I followed a structured data science workflow to ensure the reliability and depth of the insights:

### 1. Data Preprocessing

Before analysis, the raw dataset (100,000+ encounters and 50 columns) underwent rigorous cleaning:

**Missing Values**: Dropped columns with >90% missing data and imputed others using the mode or custom labels.

**Feature Engineering**: Mapped complex ICD-9 diagnosis codes into broad, clinical disease groups.
 
**Encoding**: Numerically encoded categorical data and grouped them into meaningful buckets for better visualization and correlation.

**Deduplication**: Removed redundant rows and columns with near-zero variation (99% identical values).


### 2. Descriptive Analysis

The data was explored through multiple lenses to find hidden patterns:

**Univariate Analysis**: Examined individual variables across demographics, stay details, clinical measures, and medication.

**Multivariate Analysis**: Explored correlations between numerical features (e.g., stay duration vs. medication count) and categorical relationships (e.g., insulin dosage changes vs. readmission rate).

**Target-Focused Analysis**: Specifically analyzed the relationship between all features and the three readmission classes: **<30 days (1)**, **>30 days (0)**, and **Never (-1)**.



## 📊 Key Insights & Findings


**The "Stay Duration" Myth**: The median hospital stay is **4 days** across all readmission categories, meaning length of stay alone does not predict an early return.

**Clinical Risk Factors**: Early readmission is significantly higher for patients with **fluctuating insulin levels** (dosage increases or decreases) and those with a primary diagnosis in **Group 18**.

**Predictive History**: A strong positive relationship exists between **previous emergency visits** and future inpatient admissions.

**Information Gaps**: Over **83% of A1C tests** and **94% of glucose tests** were missing, identifying a critical area for operational improvement in patient risk assessment.



## 🚀 Recommendations

Based on the analysis, the hospital should:

1. **Target High-Risk Profiles**: Implement enhanced discharge counseling and 48-hour follow-up calls for patients with **insulin adjustments**.


2. **Mandate Testing**: Standardize A1C and glucose testing for all diabetic admissions to provide the objective data needed for future predictive modeling.


3. **Outpatient Intervention**: Invest in outpatient diabetic clinics for "heavy users" to manage their conditions before they require emergency services.



## 🛠️ Tools Used

* **Language**: Python
* **Libraries**: Pandas, NumPy, Seaborn, Matplotlib
* 
**Environment**: Google Colab / Jupyter Notebook 



---

**Conclusion**: This study demonstrates that reducing readmissions requires moving beyond "standard care" for the 60–80 age bracket and focusing on targeted monitoring for patients with clinical instability and complex medical histories.

## 👤 Author
K.A.D.K.D. Dharmathilake Student ID: 21020191 | 2021/IS/019 GitHub Profile
