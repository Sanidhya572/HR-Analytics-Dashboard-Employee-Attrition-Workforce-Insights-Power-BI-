# 📊 HR Analytics Dashboard — Employee Attrition & Workforce Insights

<p align="left">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Power_Query-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Excel/CSV-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white" />
</p>

An interactive Power BI dashboard built to analyze employee attrition patterns across an organization of **1,470 employees**. The dashboard helps HR teams and business leaders identify the key drivers of attrition — by salary, age, department, job role, education, and tenure — and make data-driven decisions to improve employee retention.

---

## 📸 Dashboard Preview

![HR Analytics Dashboard](./Dashboard.png)

> **Note:** The dashboard has 4 pages — Main Dashboard, Attrition By Education, Attrition By Age Group, and Attrition By Years At Company — each enabling deep-dive analysis beyond the summary view.

---

## 🔢 Key KPIs at a Glance

| Metric | Value |
|---|---|
| 👥 Total Employees | 1,470 |
| 🚪 Attrition Count | 237 |
| 📉 Attrition Rate | 16.12% |
| 🎂 Average Age | 37 years |
| 💰 Average Salary | ₹6.50K/month |
| 🗓️ Average Tenure | 7.0 years |
| 🚹 Male Attrition | 143 |
| 🚺 Female Attrition | 80 |

---

## 📋 Dashboard Pages

| Page | Description |
|---|---|
| **Main Dashboard** | High-level summary with all KPIs, department filter, and 6 core visuals |
| **Attrition By Education** | Deep-dive into attrition rates across 6 education fields |
| **Attrition By Age Group** | Age-band breakdown of attrition with demographic filters |
| **Attrition By Years At Company** | Tenure-based attrition curve to identify early exit risk |

---

## 📊 Visuals & Charts

**KPI Cards**
Six summary cards at the top of the dashboard display Emp Count, Attrition Count, Attrition Rate, Average Age, Average Salary, and Avg Years — all dynamically filtered by department slicer (Human Resources · Research & Development · Sales).

**Attrition By Education — Donut Chart**
| Education Field | Attrition Share |
|---|---|
| Life Sciences | 37.55% |
| Medical | 26.58% |
| Marketing | 14.77% |
| Technical Degree | 13.50% |
| Other | 4.64% |

**Attrition By Age Group — Bar Chart**
| Age Group | Attrition Count |
|---|---|
| 26–35 | 116 |
| 18–25 | 44 |
| 36–45 | 43 |
| 46–55 | 26 |
| 55+ | 8 |

**Job Satisfaction Matrix — Matrix Visual**
Breaks down attrition by Job Role across satisfaction ratings 1–4, highlighting which roles have the highest dissatisfied leavers. Laboratory Technicians (62), Sales Executives (57), and Research Scientists (47) top the list.

**Attrition By Salary Slab — Bar Chart**
| Salary Range | Attrition Count |
|---|---|
| Upto ₹5K | 163 |
| ₹5K–₹10K | 49 |
| ₹10K–₹15K | 20 |
| ₹15K+ | 5 |

**Attrition By Job Role — Bar Chart**
| Job Role | Attrition Count |
|---|---|
| Laboratory Technician | 62 |
| Sales Executive | 57 |
| Research Scientist | 47 |
| Sales Representative | 33 |

**Attrition By Years At Company — Area Chart**
Attrition curve peaks sharply in Year 1, with secondary spikes around Year 5, then declines steadily — identifying early tenure as the highest-risk window for employee exits.

---

## 💡 Key Insights

**1. Salary is the single biggest attrition driver**
68.8% of all attrition (163 out of 237 employees) comes from the lowest salary bracket (Upto ₹5K/month). Compensation is the most critical lever for retention strategy.

**2. The 26–35 age group is the highest risk segment**
This group accounts for 48.9% of total attrition (116 employees), suggesting mid-career employees are leaving due to limited growth opportunities or pay dissatisfaction.

**3. First-year employees are most likely to leave**
Attrition peaks sharply at Year 1 with a rapid decline thereafter, signalling potential gaps in onboarding, cultural fit, or early role expectations.

**4. Research & Development carries the most attrition volume**
R&D accounts for 133 out of 237 attrition cases — the highest of all three departments — despite being the largest department by headcount.

**5. Laboratory Technicians are the most at-risk job role**
With 62 exits, Lab Technicians represent 26.2% of all attrition. Combined with Sales Executives (57) and Research Scientists (47), these three roles alone account for 69.6% of all leavers.

**6. Life Sciences education field sees the most exits**
37.55% of attrition comes from Life Sciences graduates, making education background a relevant factor in targeted retention programs.

---

## 🗂️ Dataset Overview

**Source:** IBM HR Analytics Employee Attrition Dataset (via Kaggle)
**Records:** 1,470 employees · **Features:** 38 columns

| Category | Columns |
|---|---|
| Employee Info | EmpID, Age, AgeGroup, Gender, MaritalStatus, Over18 |
| Job Details | Department, JobRole, JobLevel, JobInvolvement, BusinessTravel, OverTime |
| Compensation | MonthlyIncome, SalarySlab, DailyRate, HourlyRate, MonthlyRate, PercentSalaryHike, StockOptionLevel |
| Satisfaction | JobSatisfaction, EnvironmentSatisfaction, RelationshipSatisfaction, WorkLifeBalance |
| Education | Education, EducationField |
| Tenure | YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager, TotalWorkingYears |
| Performance | PerformanceRating, TrainingTimesLastYear, NumCompaniesWorked |
| Target | Attrition (Yes / No) |

---

## ⚙️ DAX Measures Used

```dax
-- Attrition Count
Attrition Count = COUNTROWS(FILTER('HR_Analytics', 'HR_Analytics'[Attrition] = "Yes"))

-- Attrition Rate
Attrition Rate = DIVIDE([Attrition Count], COUNT('HR_Analytics'[EmpID]), 0) * 100

-- Active Employees
Active Employees = COUNT('HR_Analytics'[EmpID]) - [Attrition Count]

-- Average Salary
Avg Salary = AVERAGE('HR_Analytics'[MonthlyIncome])

-- Average Age
Avg Age = AVERAGE('HR_Analytics'[Age])

-- Average Tenure
Avg Years = AVERAGE('HR_Analytics'[YearsAtCompany])
```

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Dashboard design, data modeling, visualization |
| **DAX** | Custom KPI measures and calculated columns |
| **Power Query (M)** | Data cleaning, transformation, and column profiling |
| **Excel / CSV** | Source data format |

---

## 📁 File Structure

```
HR-Analytics-Dashboard/
│
├── HR_Analytics_Dashboard.pbix     # Power BI report file
├── HR_Analytics.csv                # Source dataset (38 columns, 1470 rows)
├── Dashboard.png                   # Dashboard screenshot
└── README.md                       # Project documentation
```

---

## 🚀 How to Use

1. Clone or download this repository
2. Open `HR_Analytics_Dashboard.pbix` in **Power BI Desktop**
3. If prompted, reconnect the data source to `HR_Analytics.csv`
4. Use the **department slicer** (Human Resources / Research & Development / Sales) at the top to filter all visuals
5. Navigate across the 4 report pages using the tabs at the bottom

---

## 👤 Author

**Sanidhya Rajguru** — Data Analyst | Power BI Developer | MIS Analyst

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=netlify&logoColor=white)](YOUR_PORTFOLIO_URL_HERE)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL_HERE)
[![GitHub](https://img.shields.io/badge/GitHub-121011?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sanidhya572)
