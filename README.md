# 🏥 Healthcare Data Quality Checker

A Python-based data validation pipeline that ensures the accuracy, consistency, and completeness of healthcare patient records. This tool identifies duplicate entries, missing patient information, and logical errors such as discharge dates occurring before admission — all essential checks before downstream analytics, reporting, or machine learning.

## 📌 Problem Statement

In many healthcare systems, raw patient data can suffer from:
- Inconsistent or missing information
- Duplicate patient IDs
- Logical date conflicts (e.g., discharge before admission)

These issues can lead to flawed analytics, incorrect billing, or regulatory non-compliance. This project automates the validation and cleaning of such data using **Python**, **Pandas**, and optional **SQLite**.

---

## 🔧 Features

✅ Detects duplicate patient records (based on Patient ID)  
✅ Flags missing fields (e.g., Age, Diagnosis, Admission/Discharge Dates)  
✅ Checks for invalid date sequences (e.g., discharge before admission)  
✅ Exports cleaned dataset to CSV  
✅ Optionally loads cleaned data into a local SQL database

---

## 🧰 Tech Stack

- **Python 3.x**
- **Pandas** for data transformation
- **SQLite (Optional)** for structured storage
- **Jupyter Notebook / Google Colab** for development

---

## 📁 Sample Input Format (CSV)

```csv
Patient_ID, Name, Gender, Age, Admission_Date, Discharge_Date, Diagnosis
1001, John Doe, Male, 45, 2023-10-10, 2023-10-15, Hypertension
1002, Jane Smith, Female, , 2023-10-12, 2023-10-11, Diabetes
1001, John Doe, Male, 45, 2023-10-10, 2023-10-15, Hypertension
