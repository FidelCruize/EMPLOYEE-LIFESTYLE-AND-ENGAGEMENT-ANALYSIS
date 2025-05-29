# EMPLOYEE-LIFESTYLE-AND-ENGAGEMENT-ANALYSIS
An interactive HR analytics dashboard built with Power BI and Excel. This project visualizes key HR metrics including employee demographics, engagement, exits, grievances, and benefits to support strategic decision-making. Includes DAX formulas, stakeholder insights, and custom visuals.

HR Analytics Dashboard in Power BI

This project presents an interactive HR analytics dashboard built using *Power BI* and *Excel*. It provides insights into employee demographics, engagement, attrition trends, grievances, and HR performance across departments. The report is designed to answer critical business questions from stakeholders and support strategic workforce planning.

Project Objectives

- Track employee distribution and trends over time
- Analyze satisfaction and engagement across departments
- Monitor onboarding and attrition metrics
- Assess grievance management and resolution status
- Visualize tenure, age groups, and benefits utilization

---

 Dataset, Dashboard & Report Links

*Dashboard (Power BI Online)*: [View Dashboard](https://your-dashboard-link.com)
*Full Report (PDF)*: [Download Report](https://your-report-link.com)
*Dataset (Excel)*: [Download Dataset](https://1drv.ms/x/c/b7bce82d5399b462/EUJ-TEFDbY9EsFYFOb-MSDAB66l4vvOIzsDxWylCDoZOOA)


Stakeholder Questions & Dashboard Answers

1. *What is our current workforce distribution by department, gender, and role?*
✅ The "Employee Overview" page shows this using bar, pie, and donut charts, helping HR identify department size, gender diversity, and role spread.

### 2. *How many employees are active, on leave, or have exited the organization?*
✅ KPI cards on the overview page give real-time numbers of Active, On Leave, and Exited employees.

### 3. *What is the average tenure of exited employees?*
✅ Displayed as a KPI on the “Onboarding & Exit Trends” page, calculated in years for easy interpretation.

### 4. *How satisfied and engaged are employees across departments?*
✅ The “Engagement & Satisfaction” page includes a matrix and bar chart that compare average engagement scores and satisfaction by department.

### 5. *What are the trends in hiring and exits over time?*
✅ A line chart on the “Onboarding & Exit Trends” page shows monthly trends in new joins and exits.

### 6. *Which departments have the highest leave utilization or excessive leave days?*
✅ The “Leave & Welfare Analysis” page visualizes leave data by department and flags employees with leave days above 20.

### 7. *Are employee grievances being resolved promptly?*
✅ Pie and bar charts on the “Grievance & Records” page show the distribution of grievance status across departments.

### 8. *Which departments have the highest number of unresolved grievances?*
✅ Grievances by department bar chart highlights areas needing HR attention.

### 9. *What percentage of employees are confirmed vs not confirmed?*
✅ A clustered column chart shows confirmation status by department.

---
Key DAX Formulas Used

Employee Status & Metrics
```dax
Active Employee = 
CALCULATE(COUNT('EMPLOYEE DATSET'[EmployeeID]), 'EMPLOYEE DATSET'[Status] = "Active")

Exited Employee = 
CALCULATE(COUNT('EMPLOYEE DATSET'[EmployeeID]), 'EMPLOYEE DATSET'[Status] = "Exited")

On Leave Employee = 
CALCULATE(COUNT('EMPLOYEE DATSET'[EmployeeID]), 'EMPLOYEE DATSET'[Status] = "On Leave")

LeaveThreshold = 
CALCULATE(COUNTROWS('EMPLOYEE DATSET'), 'EMPLOYEE DATSET'[LeaveDaysTaken] > 20)
