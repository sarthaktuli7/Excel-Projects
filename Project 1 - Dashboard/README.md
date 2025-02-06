**Excel Salary Dashboard**

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/ed30a14e-33b6-4c9f-8c51-c08af0353fc1)

**Introduction**

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

It contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

**Dashboard File**

My final dashboard is in Project 1 - Dashboard [1_Salary_Dashboard.xlsx](https://github.com/sarthaktuli7/Excel-Projects/blob/main/Project%201%20-%20Dashboard/1_Salary_Dashboard.xlsx)

**Excel Skills Used**
The following Excel skills were utilized for analysis:

📉 Charts
🧮 Formulas and Functions
❎ Data Validation

Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023.It includes detailed information on:

👨‍💼 Job titles
💰 Salaries
📍 Locations
🛠️ Skills

**Dashboard Build**

📉 Charts
📊 Data Science Job Salaries - Bar Chart

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/77a6f78f-8fd8-463f-9262-a052bc51e87c)


🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
📉 Data Organization: Sorted job titles by descending salary for improved readability.
💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

**🗺️ Country Median Salaries - Map Chart**

![1_Salary_Dashboard_Chart2](https://github.com/user-attachments/assets/09644e0d-3b12-4164-817b-850aedef3757)

🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
📊 Data Representation: Plotted median salary for each country with available data.
👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.
🧮 Formulas and Functions
💰 Median Salary by Job Titles

=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.
🍽️ Background Table

![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/ba24f94e-9607-4ad5-a6f3-3ae7d33b4a55)


📉 Dashboard Implementation

Salary Dashboard Title

⏰ Count of Job Schedule Type
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
🍽️ Background Table

![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/1e755209-7bb1-455a-a9d3-2318ac5b0815)


📉 Dashboard Implementation:

Salary Dashboard Type

❎ Data Validation
🔍 Filtered List
🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
🎯 User input is restricted to predefined, validated schedule types
🚫 Incorrect or inconsistent entries are prevented
👥 Overall usability of the dashboard is enhanced

Salary Dashboard Data Validation

Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles.It allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
