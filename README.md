# HR Analytics Dashboard | Power BI

An interactive HR Analytics Dashboard built using **Microsoft Power BI, DAX, Power Query, and Excel** to analyze employee attrition, workforce demographics, job satisfaction, and employee retention patterns.

## 📌 Project Overview

The objective of this project is to transform raw HR data into meaningful insights that help HR teams understand employee attrition, monitor workforce metrics, and make data-driven decisions to improve employee retention.

## 🎯 Objectives

- Analyze employee attrition across departments, job roles, age groups, and education fields.
- Monitor key HR metrics through interactive KPI cards.
- Explore workforce demographics, salary patterns, and job satisfaction.
- Identify employee groups and business areas that may require further retention analysis.
- Build an interactive dashboard for HR reporting and decision-making.

## 🛠️ Tools & Technologies

- **Microsoft Power BI** — Dashboard development and data visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — Calculated measures and KPI development
- **Microsoft Excel** — Dataset inspection and data preparation

## 📂 Dataset

The dataset contains employee information, including demographics, department, job role, education, salary, job satisfaction, business travel, and attrition status.

## ⚙️ Project Workflow

### 1. Data Collection
- Imported the raw employee dataset into Power BI.
- Inspected columns, data types, and data quality.

### 2. Data Cleaning & Transformation
- Removed unnecessary columns and duplicate records where appropriate.
- Handled missing values and data errors.
- Standardized column names and corrected data types.
- Prepared the dataset for analysis using Power Query.

### 3. Data Modeling & DAX

Created an `AttritionCount` column to identify employees who left the organization.

Example calculated column:

```dax
AttritionCount =
IF(HR_Analytics[Attrition] = "Yes", 1, 0)
```

Example measures:

```dax
Employee Count =
DISTINCTCOUNT(HR_Analytics[EmployeeNumber])
```

```dax
Attrition Count =
SUM(HR_Analytics[AttritionCount])
```

```dax
Active Employees =
[Employee Count] - [Attrition Count]
```

```dax
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Employee Count],
    0
)
```

Format `Attrition Rate` as a percentage in Power BI. Replace table and column names if your dataset uses different names.

### 4. Dashboard Development
- Created KPI cards for total employees, attrition count, active employees, and attrition rate.
- Built bar charts, clustered column charts, donut charts, and matrix tables.
- Added interactive slicers and filters for exploring workforce metrics.
- Designed visualizations to compare attrition across employee categories.

## 📊 Key Performance Indicators

The dashboard focuses on:

- Total Employee Count
- Attrition Count
- Active Employees
- Employee Attrition Rate
- Average Employee Age
- Average Salary
- Department-wise Attrition
- Gender-wise Attrition
- Job Satisfaction Ratings

## 🔍 Key Business Questions

The dashboard helps answer the following questions:

1. What is the total number of employees?
2. How many employees have left the organization?
3. How does attrition differ by gender?
4. Which departments have the highest employee count and attrition?
5. Which job roles experience higher employee turnover?
6. How does attrition vary by age group and education field?
7. What are the average employee age and salary?
8. How are employees distributed across education fields?
9. Which business travel categories have the most employees?
10. How do job satisfaction ratings vary across job roles?

## 💡 Key Insights

Based on the analysis of the dataset:

- **Workforce Size:** The dataset contains 1,470 employees.
- **Employee Attrition:** 237 employees left the organization.
- **Gender Analysis:** Attrition cases include 150 male and 87 female employees.
- **Age Group Analysis:** Employees aged 25–34 account for 112 attrition cases.
- **Department Analysis:** Department-wise comparisons help identify areas for further retention analysis.
- **Job Role Analysis:** Role-based attrition patterns can help HR teams investigate potential retention challenges.
- **Education Analysis:** Comparing attrition across education fields and levels provides additional workforce insights.

*Note: Validate all reported values and rankings against the final dashboard before publication. Attrition counts and attrition rates measure different things.*

## 📈 Skills Demonstrated

- Data Cleaning and Transformation
- Exploratory Data Analysis
- Data Modeling
- DAX Measures and Calculated Columns
- KPI Development
- Interactive Dashboard Design
- Data Visualization
- Business Intelligence Reporting
- Data-Driven Decision-Making

## 🚀 How to Use

1. Download or clone this repository.
2. Download the HR dataset using the link provided above.
3. Open the `.pbix` file in Microsoft Power BI Desktop.
4. If prompted, update the dataset source path.
5. Refresh the data and verify the measures.
6. Use the dashboard slicers and filters to explore the results.


## 👨‍💻 Author

**Ashish Gola**

- GitHub: [ashish-gola](https://github.com/ashish-gola)
- LinkedIn: [Ashish Gola](https://www.linkedin.com/in/ashish-gola-388833278/)

---

If you find this project useful, consider giving the repository a ⭐ on GitHub.
