# 📚 SQL Data Analysis Project: Chicago Public Schools

This repository contains a Jupyter Notebook (`ChicagoSchool.ipynb`) showcasing beginner-friendly SQL and data analysis techniques using the **Chicago Public Schools** dataset. It serves as a portfolio project for aspiring data analysts.

## 🎯 Project Objective

The goal is to:
- Practice SQL queries in Python using `sqlite3` and `%sql` magic commands
- Load and explore real-world data from the City of Chicago
- Perform meaningful data analysis and gain insights
- Visualize relationships using Seaborn

---

## 🗂 Dataset Information

- **Source**: IBM Developer Skills Network (Coursera Lab)
- **Data**: [Chicago Public Schools Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/FinalModule_Coursera_V5/data/ChicagoPublicSchools.csv)
- **Table Name**: `CHICAGO_PUBLIC_SCHOOLS_DATA`

---

## 🔧 Tools and Technologies

| Tool           | Purpose                          |
|----------------|----------------------------------|
| Python         | Main programming language        |
| Pandas         | Data loading and manipulation    |
| SQLite3        | Local SQL database               |
| ipython-sql    | Magic command for SQL in notebooks |
| PrettyTable    | Neatly display SQL results       |
| Seaborn        | Data visualization               |
| Jupyter Notebook | Interactive coding environment |

---

## 📊 Key SQL Tasks Performed

- ✅ Load CSV into SQLite using `pandas.to_sql()`
- ✅ Retrieve table names using `sqlite_master`
- ✅ Explore table schema with `PRAGMA table_info`
- ✅ Count total number of rows
- ✅ Filter schools by:
  - Hardship Index > 50
  - Maximum Safety Score
  - Maximum Attendance
- ✅ Top 10 schools by attendance
- ✅ Use of `REPLACE()` for cleaning percentage strings
- ✅ Data visualization using scatter plot

---

## 📈 Sample Query

```sql
SELECT NAME_OF_SCHOOL, AVERAGE_STUDENT_ATTENDANCE
FROM CHICAGO_PUBLIC_SCHOOLS_DATA
ORDER BY CAST(REPLACE(AVERAGE_STUDENT_ATTENDANCE, '%', '') AS FLOAT) DESC
LIMIT 10;
