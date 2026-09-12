
# HR Analytics Dashboard

An interactive Power BI dashboard designed to analyze employee turnover, workforce demographics, and organizational performance metrics to drive data-informed HR strategies.

## Overview
This project visualizes key workforce metrics for an organization of **1,417 employees**, tracking an active headcount of **1,186** and analyzing **231 departures** (**16.3% attrition rate**). 

## Key Insights
* **Department Insights:** Operations (36%) and Sales (23%) experience the highest volume of attrition.
* **Tenure Vulnerability:** Departures peak sharply during early career stages (1–5 years of experience).
* **Role & Satisfaction:** Laboratory Technicians account for the highest individual role turnover (59 employees), with strong correlation to lower job satisfaction ratings.
* **Demographics:** The workforce predominantly sits in the 26–35 age bracket (588 employees), with an average organizational age of 36.94 years.

## Tools Used
* **Power BI Desktop:** Data modeling, DAX measures, and visual report design.
* **Power Query:** Data transformation, cleaning, and ETL processing.

# KPI Questions
What is the total number of employees in the organization?,
How many employees are currently active?,
How many employees have left the organization?,
What is the overall employee attrition rate?,
What is the average age of employees?,
What is the average work experience of employees?,
Which department has the highest number of employees?,
Which department has the highest number of attrition cases?,
Which salary slab has the highest attrition?,
Which age group has the highest number of employees?,
Which gender has the higher number of attrition cases?,
Which job roles have the highest attrition?,
Which job satisfaction level has the highest number of attrition cases?,
How does employee experience relate to attrition?,
Which departments should HR prioritize for employee retention?


# Project Process — HR Analytics Dashboard (Power BI)

## 1. Problem Understanding & Requirement Gathering
- Identified the business need: track employee attrition, workforce composition, and satisfaction levels for HR decision-making.
- Defined key stakeholders (HR managers, department heads) and their reporting requirements.
- Listed required KPIs: Total Employees, Active Employees, Attrition Count, Attrition Rate %, Average Age, Average Experience.

## 2. Data Collection
- Gathered raw HR dataset containing employee details: EmployeeID, Department, JobRole, Age, Gender, Salary, Experience, Attrition Status, Job Satisfaction Score, etc.
- Data sourced typically from HRMS exports, Excel/CSV files, or SQL databases.

## 3. Data Cleaning & Preparation (Power Query)
- Imported data into Power BI using **Get Data**.
- Removed duplicates, handled null/missing values (e.g., missing satisfaction scores or experience).
- Standardized column names and data types (e.g., converting Age/Experience to numeric, Attrition to Yes/No).
- Created calculated columns where needed (e.g., Age Group buckets: 18-25, 26-35, etc.).

## 4. Data Modeling
- Built relationships between tables (if multiple tables existed — e.g., Employee Master, Department, Job Role tables).
- Ensured a proper star schema (fact table: Employee records; dimension tables: Department, JobRole, AgeGroup).

## 5. DAX Measures Creation
- Created calculated measures:
  - `Total Employees = COUNT(EmployeeID)`
  - `Attrition Count = CALCULATE(COUNT(EmployeeID), Attrition="Yes")`
  - `Attrition Rate % = DIVIDE([Attrition Count], [Total Employees])`
  - `Average Age = AVERAGE(Age)`
  - `Average Experience = AVERAGE(TotalExperience)`

## 6. Dashboard Design & Layout Planning
- Sketched dashboard wireframe: header (title + slicers), KPI card row, chart section, department navigation panel.
- Chose a consistent color theme (blue/white corporate style) for visual clarity.

## 7. Visualization Development
- Built KPI cards for headline metrics.
- Created donut chart for Attrition by Department.
- Built bar chart for Attrition by Salary Slab.
- Designed matrix table for Job Role vs Job Satisfaction.
- Added bar chart for Age Group Distribution.
- Created pie chart for Attrition by Gender.
- Built area/line chart for Attrition by Experience.
- Added horizontal bar chart for Department-wise Employee Count.

## 8. Interactivity & Filtering
- Added slicers for Age Group (top panel).
- Created button-based navigation for Department filtering using bookmarks/selections.
- Enabled cross-filtering so selecting one visual updates all others.

## 9. Testing & Validation
- Cross-checked KPI values against raw data totals.
- Verified filter/slicer interactions work correctly across all visuals.
- Checked for calculation accuracy (attrition rate, averages).

## 10. Formatting & Polishing
- Applied consistent fonts, colors, and card styling.
- Added titles, icons, and tooltips for better readability.
- Arranged visuals in a logical, easy-to-scan layout.

## 11. Review & Insights Generation
- Analyzed dashboard to draw insights (e.g., Operations has highest attrition, early-career employees attrit more).
- Prepared summary findings for stakeholders.

## 12. Deployment & Sharing
- Published the report to Power BI Service.
- Shared with stakeholders via workspace access or embedded links.
- Set up scheduled data refresh if connected to a live source.

## 13. Documentation
- Documented data sources, DAX formulas, and dashboard usage instructions.
- Created a README/repository description for future reference or portfolio use.

Want me to turn this into a **flowchart/diagram**, a **step-card visual**, or a **Word document** for your portfolio/resume?
