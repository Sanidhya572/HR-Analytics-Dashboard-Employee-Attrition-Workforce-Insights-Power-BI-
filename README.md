# HR-Analytics-Dashboard-Employee-Attrition-Workforce-Insights-Power-BI-

# 📊 HR Analytics Dashboard  
### Employee Attrition & Workforce Insights | Power BI Project

---

## 🚀 Project Overview

Employee attrition directly impacts productivity, hiring costs, and team stability.  

This project analyzes HR data to uncover the key drivers behind employee turnover and provides interactive workforce insights using Power BI.

The dashboard helps leadership:

✔ Identify high-attrition departments  
✔ Analyze salary & satisfaction impact  
✔ Understand tenure patterns  
✔ Support data-driven retention strategies  

---

## 🧠 Business Problem

The organization is experiencing increasing employee turnover but lacks clarity on the root causes.

Key questions addressed:

- What is the current attrition rate?
- Which departments are most affected?
- Does salary influence employee retention?
- Are early-tenure employees more likely to leave?
- How does job satisfaction correlate with attrition?

This dashboard transforms raw HR data into actionable workforce intelligence.

---

## 📂 Dataset Description

The dataset consists of employee-level HR records including:

- Employee ID  
- Age  
- Gender  
- Department  
- Job Role  
- Education Level  
- Salary  
- Years at Company  
- Job Satisfaction  
- Attrition Status (Yes/No)

The data enables demographic, financial, and tenure-based workforce analysis.

---

## 🛠 Tools & Technologies

- **Power BI** – Dashboard development & visualization  
- **Power Query** – Data cleaning & transformation  
- **DAX (Data Analysis Expressions)** – KPI calculations  
- **GitHub** – Version control & documentation  

---

## 📈 Key KPIs & DAX Measures

### 1️⃣ Total Employees
```DAX
Total Employees = COUNT(Employee[EmployeeID])

###
Total Attrition = 
CALCULATE(COUNT(Employee[EmployeeID]), Employee[Attrition] = "Yes")

Attrition Rate = 
DIVIDE([Total Attrition], [Total Employees], 0)

Average Salary = AVERAGE(Employee[Salary])

Avg Satisfaction = AVERAGE(Employee[JobSatisfaction])

Avg Years = AVERAGE(Employee[YearsAtCompany])
