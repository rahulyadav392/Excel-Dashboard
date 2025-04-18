# Excel Dashboard
 ![Dashboard Recording](https://github.com/user-attachments/assets/8c96d603-d487-488b-8054-d0327a73e8f0)

## Introduction
I build this Jobs Salary dashboard to showcase my following skills:

- Data Validation
- Formulas and Function
- Charts
  
The dataset used in this project is real life 'Data Science' jobs posted on various job portals in 2023. This dataset contains 

- Job Location
- Skills
- Salary
- Job Title


## Dashboard File
Final Dashboard file can be accessed through: [JOB_Dashboard](https://github.com/rahulyadav392/Excel-Dashboard/blob/main/Salary%20Dashboard.xlsx)

## Dashboard Build

Following are the different dashboards that I build in this project:

### Bar Chart- Median Salary of Data Roles

![avg salary Dashboard](https://github.com/user-attachments/assets/e73394f8-c180-4b47-9909-51be7e6ebc7d)

- **Excel Features Used:** Shortlisted bar chart and optimised layout for clarification.
- **Data Classification:** Sorted Mean Salary of Data Role in Descending Order to gain meaningful insights from data.
- **Insights Gained:**     We can conclude Senior Roles and Enginnering Roles are paid more than analyst roles.

  ### Map Chart- Median Salary Comparison By Country
  
  ![Map Recording](https://github.com/user-attachments/assets/b40d222d-f4b0-4b93-bb71-006534830406)

- **Excel Features Used:** Here we used Excel's Map Chart Feature to plot Medain Salary across the globe.
- **Data Classification:** Colour Coded Median Salary for each country whose data was available.
- **Insights Gained:** Enables us to read salary trends geographically at a quick glance.

## Formulas and Functions
### Median Salary by Job Title
 ```
=MEDIAN(
IF(
(A2=jobs[job_title_short])*
(Country=jobs[job_country])*
(ISNUMBER(SEARCH(Type,jobs[job_schedule_type])))*
(jobs[salary_year_avg]<>0),
jobs[salary_year_avg]
)
)
```
- **Multiple Filters:** Value shown is passed through multiple filters- Job Title, Job Country, Job Type and filters out Blank Value
- **Array Formula:** Utizlized Median() Function with Nested IF() to analyze data..
- **Formula Purpose:** The formula retrieves and displays the median salary based on the selected job role, location, and employment category in the table below.
