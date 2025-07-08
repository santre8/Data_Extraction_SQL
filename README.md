# Data_Extraction_SQL

This project replicates the clinical cohort logic from Liu et al. (2022), using SQL to extract relevant features from **MIMIC-IV v3.1** for analyzing weaning outcomes in mechanically ventilated sepsis patients.


---

## 📌 Project Overview

- **Goal:** Extract clinical variables for machine learning based on a published study
- **Database:** MIMIC-IV v3.1 (accessed via BigQuery)
- **Tools:** SQL, BigQuery, Python (XGBoost)
- **Patient group:** Adult ICU patients with Sepsis-3 diagnosis and first invasive ventilation

---

## 📁 Files in this Repository

- `SQL_queries.txt`: full SQL code used to extract data
- `Conceptualization comparison and Reflection.pdf`: explanation of cohort definition and ethical considerations
- `ML-XGBoost.ipynb`: optional notebook to train an XGBoost classifier on the extracted dataset

---

## 📊 Extracted Variables

- **Vitals:** heart rate, respiratory rate, MAP, SpO₂, temperature
- **Labs:** pH, PaO₂, PaCO₂, creatinine, WBC, hemoglobin, etc.
- **Treatments:** vasopressors, antibiotics, CRRT
- **Derived features:** PaO₂/FiO₂ ratio, PEEP, GCS, BMI
- **Comorbidities:** Charlson Index + selected conditions

---

## 🤖 ML Summary

- XGBoost model trained on extracted dataset
- AUROC ≈ 0.71
- Class imbalance affected performance (F1-score for failure = 0.02)
- Model was used to reflect how raw data affects predictive power

---

## 🔐 Ethics & CITI Certification

All queries were conducted in a secure BigQuery environment using de-identified patient data.  
Access was granted through completion of the **CITI course** on human subjects research.  
Data privacy, anonymity, and ethical handling were respected throughout the project.

---

## 📚 Reference

Liu, W. et al. (2022).  
*A Simple Weaning Model Based on Interpretable Machine Learning Algorithm for Patients With Sepsis: A Research of MIMIC-IV and eICU Databases.*  
Frontiers in Medicine. https://doi.org/10.3389/fmed.2021.814566

---

## 👩🏻‍💻 About Me

Carmen Sandate  
Post-Degree Diploma in Data Analytics – Langara College  
💼 [Portfolio](https://sandate.vercel.app) | 🧠 [LinkedIn](https://www.linkedin.com/in/mariacarmensandate/)
