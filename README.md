# Palmora-Gender-Equality-Analysis-Capstone
This is also one of the first Project done while learning Data Analysis under Incubator Hub
## Project Name: Palmora Gender Equality Analysis.

### Project Overview
This project aims to generate insight into the gender equality analysis of Palmora and the impact. By analysing the various parameters in the data recieved we seek to gather enough insight to make a reasonable decisions and suggestions which enable us to tell compelling stories around our data from the insight gotten and to know the best reviews from our data. And more importantly to eradicate any grudges or issues surrounding the gender bias of the organization.

### Data Source
The primary source of Data used here is Pamora Gender Equality analysis.csv and this is provided by Capstone.

### Tools Used
  *Microsoft Power Bi Desktop for Data Cleaning and Visualization* [Download Here](https://www.Microsoft.com)
  - For Manipulation
    - For Munchin 
- *Microsoft Power Bi for Querryind and Analysis*
- *Microsoft power Bi for creating report with a better visualization*

### Explanatory Data Analysis
EDA involved the exploring of Data to answer some questions about the data...

Importing the employee data into Power BI.
Do a proper cleaning E.g
1. Remove employees without salaries and departments indicated as "NULL".
2. Assign a generic gender status to employees who refused to disclose their gender.

1: Gender Distribution Analysis
1. Create a bar chart:
    - Axis: Region/Department
    - Value: Count of Employees by Gender
2. Use a slicer to filter by region/department.
3. Visualize the overall gender distribution using a pie chart.

Visualization: 
- Bar chart: "Gender Distribution by Region"
- Pie chart: "Overall Gender Distribution"

Measures
- Gender Count = COUNT('Employee'[Gender])
- Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))

2: Ratings Insights Based on Gender
1. Create a histogram/box plot:
    - Axis: Rating
    - Value: Count of Employees by Gender
2. Use a slicer to filter by gender.
3. Calculate the average rating by gender using a measure.

Visualization:
- Histogram: "Ratings Distribution by Gender"
- Box plot: "Ratings Comparison by Gender"

Measures
- Average Rating by Gender = AVERAGE('Employee'[Rating])
- Rating Count by Gender = COUNT('Employee'[Rating])

3: Salary Structure and Gender Pay Gap Analysis
1. Create a scatter plot:
    - X-axis: Salary
    - Y-axis: Gender
2. Calculate the average salary by gender using a measure.
3. Identify departments and regions with significant pay gaps.

Visualization:
- Scatter plot: "Salary vs. Gender"
- Bar chart: "Average Salary by Department and Region"

Measures 
- Average Salary by Gender = AVERAGE('Employee'[Salary])
- Salary Count by Department and Region = COUNT('Employee'[Salary])

4: Minimum Salary Requirement Analysis
1. Create a histogram:
    - Axis: Salary Band ($10,000 increments)
    - Value: Count of Employees
2. Use a slicer to filter by region.
3. Calculate the number of employees below the minimum salary threshold.

Visualization:
- Histogram: "Salary Distribution by $10,000 Band"
- Bar chart: "Employees Below Minimum Salary Threshold by Region"

Measures
- Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])

5: Bonus Payment Calculation
1. Create a measure to calculate the bonus amount based on performance ratings.
2. Calculate the total amount to be paid to individual employees (salary + bonus).
3. Create a bar chart to visualize the total amount to be paid out per region.

Visualization:
Bonus Payments
- Bar chart: "Total Bonus Payout by Region"
- Table: "Individual Employee Bonus Payments"

Measures
- Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)
- Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'

Clearing the product name by using Left function
-Create a new column beside the product name
-On the new column write your formula 
-Using Left function( Select the cell range,  number character (35))
-Create another column to clean your data by using Proper function 
-Create another new column 
-And copy from the Proper function column and left click on the new column, then click on special paste
-Edit by clicking on the value 
-Then you can delete the previous Product Name Column 
-You can then proceed to pivot table

 ## After a clear Analysis, A request came to add and determine a new result within the Data using a new set of Data shared by the company.

Create a new column beside your product name column, then write your LEFT function in the  new column 
Create another new column beside the LEFT function column 
Then alight LEFT function column, copy and paste into the new column using (Special paste)

Add custom Column .. New column "Gender _Final"  

= Gender_Final" =
If Is Null([Gender]) or [Gender] = "", "Undisclosed", [Gender]

I did a conditional column and give a new gender to those ones that didn't reveal their gender

Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)
- Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'

### Results
As shown in the above uploaded file. Includdes a clear Dashboard Visualization and Cocnclusion.
