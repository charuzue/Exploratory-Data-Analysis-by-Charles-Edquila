# 📉 Layoffs Data Cleaning & Analysis Project

This project focuses on cleaning and analyzing global tech layoff data using MySQL. It covers end-to-end data wrangling and exploratory data analysis (EDA) to uncover trends in layoffs by company, country, industry, and time.

---

## 🧹 Data Cleaning Process

- 📦 Created a backup table to preserve the original dataset before applying transformations.
- 🔍 Removed duplicates using `CTE` with `ROW_NUMBER() OVER (PARTITION BY ...)` to ensure clean and reliable records.
- 🧾 Standardized inconsistent values in text columns (`company`, `industry`, `country`) using `TRIM()`, `LIKE`, and `UPDATE`.
- 🗓️ Converted string-based date values into SQL `DATE` format using `STR_TO_DATE()` for accurate time-based queries.
- 🔗 Imputed missing `industry` values using `self-JOINs` based on company name similarity and removed rows with null layoff metrics.

---

## 📊 Data Analysis Insights

- Aggregated layoffs by `company`, `industry`, `country`, and `funding stage` using `GROUP BY` and `SUM()` to identify top trends.
- Analyzed layoff activity over time using `SUBSTRING()` and `YEAR()` to group by month and year.
- Detected companies that laid off **100% of their workforce** by filtering `percentage_laid_off = 1`.
- Implemented `window functions` (`SUM() OVER`) to calculate **rolling totals** of layoffs across months.
- Ranked the **Top 5 companies per year** by total layoffs using `CTEs` and `DENSE_RANK()` with `PARTITION BY`.

---

## 🛠️ Tools & Technologies

- SQL (MySQL)
- Window Functions
- Common Table Expressions (CTEs)
- Data Cleaning & Transformation
- Exploratory Data Analysis (EDA)

---

## 📁 Dataset Source

- The dataset used in this project is a cleaned and structured version of publicly available layoff records.

---

## 📌 Author

Charles Reyes  
GitHub: [charuzue](https://github.com/charuzue)  
