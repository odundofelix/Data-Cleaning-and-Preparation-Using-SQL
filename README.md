# 🧹 SQL Data Cleaning Project: Layoffs Dataset

## 📌 Overview

This project showcases a comprehensive data cleaning and preparation process using SQL on a layoffs dataset. The goal was to transform raw, inconsistent data into a clean and analysis-ready format by applying structured SQL techniques. Key tasks included removing duplicates using window functions, standardizing text and date formats, handling null and blank values, and optimizing the dataset structure.

The project demonstrates core data wrangling skills essential for accurate reporting and modeling, and highlights best practices in using SQL for real-world data preparation in analytics and business intelligence contexts.

---

## 🎯 Objectives

- Remove duplicate records using `ROW_NUMBER()`
- Standardize textual and date fields (e.g., trimming whitespace, fixing formats)
- Identify and handle null or blank values
- Drop unnecessary columns for streamlined analysis

---

🛠️ Tools & Technologies:
- Database: MySQL
- Language: SQL
- Key Concepts: CTEs, Window Functions, Data Standardization, NULL Handling, String Functions, Date Formatting

---

🔍 Key Tasks Performed:
1. Removed Duplicates
- Used a ROW_NUMBER() window function to detect duplicate rows based on all relevant fields.
- Created a staging table (layoffs_staging2) and deleted records where row_num > 1.
2. Standardized Text Data
- Trimmed whitespace using TRIM().
- Unified similar values in the industry column (e.g., "Crypto", "crypto", "cryptocurrency" → crypto).
- Removed trailing characters from country names (e.g., "United States." → "United States").
3. Formatted Dates
- Converted date values from text format (MM/DD/YYYY) to SQL DATE type using STR_TO_DATE() and ALTER TABLE.
4. Handled NULL and Blank Values
- Identified and updated blank strings to NULL.
- Imputed missing values in the industry column using JOIN logic based on the same company with non-null values.
- Deleted rows with missing critical values (total_laid_off AND percentage_laid_off).
5. Dropped Unnecessary Columns
- Removed helper column row_num after de-duplication.
  
---

📈 Outcome / Business Value:
- Produced a clean and consistent dataset ready for further analysis (e.g., trend analysis, layoff metrics).
- Improved data reliability and reduced noise, which is critical for accurate business reporting and decision-making.

---

📁 Project Files
- layoffs.csv: Original dataset

- data_cleaning_project_portfolio_script.sql: Full SQL script with all cleaning steps

- layoffs_staging2.csv: Final cleaned dataset
---
📌 Key Takeaway
- This project highlights practical SQL data cleaning workflows that are crucial before performing data analysis or feeding data into visualization tools like Power BI or Tableau.
