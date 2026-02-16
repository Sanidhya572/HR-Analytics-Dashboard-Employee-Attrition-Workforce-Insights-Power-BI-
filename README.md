# HR-Analytics-Dashboard-Employee-Attrition-Workforce-Insights-Power-BI-

🧠 1️⃣ Problem Statement

A company is experiencing increasing employee turnover and lacks clarity on the key factors driving attrition. Leadership wants a data-driven dashboard to:

Identify departments with high attrition
Analyze salary and satisfaction impact
Understand demographic trends
Improve retention strategy

The objective of this project is to analyze HR data and uncover actionable insights to help reduce attrition and improve workforce planning.


📊 2️⃣ Dataset Description

The dataset contains employee-level HR records including:

Employee ID
Age
Gender
Department
Job Role
Education
Salary
Years at Company
Job Satisfaction
Attrition (Yes/No)

🛠 3️⃣ Tools Used

Power BI – Data modeling & dashboard creation
DAX – KPI calculations & measures
Power Query – Data cleaning & transformation
GitHub – Version control & documentation

📈 4️⃣ KPIs Defined

1. Total Employees
Total workforce size.
Total Employees = COUNT(Employee[EmployeeID])

2. Total Attrition
Number of employees who left.
Total Attrition = CALCULATE(COUNT(Employee[EmployeeID]), Employee[Attrition] = "Yes")

3. Attrition Rate (%)
Measures employee turnover percentage.
Attrition Rate = 
DIVIDE([Total Attrition], [Total Employees], 0)

Business Value:
Helps measure workforce stability.

4. Average Salary
Average compensation level.
Average Salary = AVERAGE(Employee[Salary])

5. Average Job Satisfaction
Avg Satisfaction = AVERAGE(Employee[JobSatisfaction])

6. Average Years at Company
Avg Years = AVERAGE(Employee[YearsAtCompany])
