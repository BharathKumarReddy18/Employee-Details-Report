# Part-Time Employees Dataset

## Overview
This dataset contains information about part-time employees, including their demographic details, employment history, and termination reasons. The data spans from 2013 to 2014 and includes various attributes related to the employees' job and personal details.

## Columns
- **Offer Date**: The date when the job offer was made to the employee.
- **EmplID**: Unique identifier for each employee.
- **Gender**: Gender of the employee (all entries are female).
- **Age**: Age of the employee (all entries are 20 years old).
- **Ethnic Group**: Ethnic group of the employee (all entries belong to Group A).
- **Job Type**: Type of job (all entries are part-time).
- **Termination Date**: The date when the employee's job was terminated.
- **Region**: The region where the employee was located (e.g., 4-East, 5-Central).
- **Vice President**: The vice president responsible for the employee's region (e.g., Brett Jones, Angelita Bowley).
- **Join Date**: The date when the employee joined the company.
- **Pay Type**: The type of pay (all entries are hourly).
- **Termination Reason**: The reason for termination (all entries are voluntary).

## Summary Statistics
- **Total Records**: 43,120
- **Age**: All employees are 20 years old.
- **Gender**: All employees are female.
- **Job Type**: All employees are part-time.
- **Termination Reason**: All terminations are voluntary.

## Data Insights
- The dataset provides a comprehensive view of part-time employees' employment history and demographics.
- It can be used for various analyses, such as turnover rates, regional employment trends, and demographic studies.

## Database Schema
The dataset has been structured into multiple tables with relationships to facilitate analysis. Below are the details of each table and their connections:

### Tables and Relationships
1. **Date Table**
   - **Columns**: Date, Day, Month, Year
   - **Connected to**: Employee_Fact New (Date)

2. **Region**
   - **Columns**: Region
   - **Connected to**: Employee_Fact New (Region)

3. **Pay Type**
   - **Columns**: Pay Type
   - **Connected to**: Employee_Fact New (Pay Type)

4. **Ethnic Details**
   - **Columns**: Ethnic Group
   - **Connected to**: Employee_Fact New (Ethnic Group)

5. **Job Type**
   - **Columns**: Job Title
   - **Connected to**: Employee_Fact New (Job Title)

6. **Termination Reason**
   - **Columns**: Termination Reason
   - **Connected to**:
     - Vice President (Termination Reason)
     - Employee_Fact New (Termination Reason)

7. **Vice President**
   - **Columns**: Vice President
   - **Connected to**: Employee_Fact New (Vice President)

8. **Employee_Fact New**
   - **Columns**: Age, Age Group, Date, Department Name, EmpID, Ethnic Group, Gender, Hire Status, Job Title, Pay Rate, Pay Status, Region, Termination Date
   - **Connected to**: All other tables

---

