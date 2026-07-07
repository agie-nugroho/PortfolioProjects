# COVID-19 Data Exploration with SQL

## 📌 Overview

This project demonstrates SQL-based exploratory data analysis (EDA) on global COVID-19 data using Microsoft SQL Server.

The analysis focuses on understanding the spread of COVID-19, mortality rates, infection rates, and vaccination progress across countries and continents. Advanced SQL techniques such as **JOIN**, **Common Table Expressions (CTE)**, **Window Functions**, **Temporary Tables**, and **Views** are used to transform and analyze the data.

This project is intended to showcase practical SQL skills commonly used by Data Analysts.

---

## 📂 Dataset

This project uses two datasets:

* **CovidDeaths.xlsx**

  * Country information
  * Date
  * Total cases
  * New cases
  * Total deaths
  * Population
  * Continent

* **CovidVaccinations.xlsx**

  * Country information
  * Date
  * New vaccinations
  * Vaccination statistics

Both datasets are imported into SQL Server as:

* `CovidDeaths`
* `CovidVaccinations`

---

## 🛠️ Tools & Technologies

* Microsoft SQL Server
* SQL Server Management Studio (SSMS)
* Microsoft Excel

---

## 📊 Analysis Performed

The project includes several analytical queries:

### 1. Data Selection

* Display relevant columns for analysis
* Filter unnecessary records

### 2. Death Percentage Analysis

* Calculate the percentage of deaths among confirmed COVID-19 cases.

Formula:

```
(total_deaths / total_cases) × 100
```

---

### 3. Infection Rate by Population

* Calculate the percentage of each country's population infected with COVID-19.

Formula:

```
(total_cases / population) × 100
```

---

### 4. Countries with Highest Infection Rate

* Identify countries with the highest infection percentage relative to their population.

---

### 5. Countries with Highest Death Count

* Compare total deaths across countries.

---

### 6. Continents with Highest Death Count

* Aggregate death counts by continent.

---

### 7. Global COVID-19 Statistics

Calculate worldwide:

* Total Cases
* Total Deaths
* Global Death Percentage

---

### 8. Vaccination Progress

Join COVID deaths and vaccination datasets to analyze vaccination progress over time.

Techniques used:

* INNER JOIN
* Window Function (`SUM() OVER()`)

Rolling vaccination calculation:

```
SUM(new_vaccinations)
OVER (
    PARTITION BY location
    ORDER BY date
)
```

---

### 9. Common Table Expression (CTE)

Use CTE to simplify rolling vaccination calculations and percentage computations.

---

### 10. Temporary Table

Store intermediate vaccination results inside a temporary table for further analysis.

---

### 11. SQL View

Create a reusable SQL View:

```
PercentPopulationVaccinated
```

This view can later be connected directly to visualization tools such as Tableau or Power BI.

---

## 💡 SQL Concepts Demonstrated

* SELECT
* WHERE
* ORDER BY
* GROUP BY
* Aggregate Functions
* CAST & CONVERT
* INNER JOIN
* Window Functions
* Common Table Expressions (CTE)
* Temporary Tables
* SQL Views

---

## 📁 Repository Structure

```
COVID19-SQL-Data-Exploration/
│
├── CovidDeaths.xlsx
├── CovidVaccinations.xlsx
├── Covid_Data_Exploration.sql
├── README.md
```

---

## 🎯 Learning Outcomes

Through this project, I practiced:

* Writing analytical SQL queries
* Exploring real-world datasets
* Performing data aggregation
* Calculating infection and mortality metrics
* Using window functions for cumulative calculations
* Building reusable SQL objects with Views
* Preparing datasets for visualization

---

## 🚀 Future Improvements

* Create interactive dashboards using Tableau or Power BI.
* Add trend analysis by month and year.
* Compare vaccination progress between countries.
* Perform regional and continental comparisons.
* Optimize queries for larger datasets.

---

## 👤 Author

**Agie Nugroho**

Mathematics Graduate | Aspiring Data Analyst

Feel free to connect and explore more of my data analytics projects.
