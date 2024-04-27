# Call Center - Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

The objective is to provide insights into call center operations, including the total number of calls, call duration, response time, and distribution of calls by various parameters such as state, reason, channel, sentiment, and call center.


## Project Overview
Your project aims to analyze call center data to derive insights and facilitate better decision-making. It consists of two main dashboards: "HOME" and "GRID." The "HOME" dashboard focuses on key performance indicators (KPIs) and charts, while the "GRID" dashboard provides a granular analysis of call details.


### Dashboard 2: HOME: 

## KPIs
- Step 1 : Total Number of Calls
- Step 2 : Total Call Duration in Hours
- Step 3 : Total Call Duration in Minutes
- Step 4 : Average Call Duration in Minutes
- Step 5 : Response Time Percentage
## Charts
- Step 1 : Total Call by Day (Column Chart)
- Step 2 : Total Calls by State (Filled Map Chart)
- Step 3 : Top Reason for Calls (Tree Map)
- Step 4 : Total Calls by Channel (Donut Chart)
- Step 5 : Total Calls by Sentiment (Column Chart)
- Step 6 : Total Calls by Call Centre (Bar Chart)

### Dashboard 2: GRID:
This dashboard provides a detailed table view of call details, allowing users to apply filters and export data. It includes columns such as ID, Customer Name, Channel, State, Reason, Response Time, City, and Call Duration.

### Additional Actions:
I've created calculated columns and measures to derive additional insights, such as total calls, total call duration, response time percentage, and average call duration. Filters have been implemented for date range, city, and channel to facilitate specific data analysis.

### Comparison with Reference Example:
Your project shares similarities with a reference example related to airline customer satisfaction analysis. Both projects involve data visualization, KPI tracking, and insights generation to improve service quality based on customer feedback.

Overall, your project appears to be well-structured and aligned with the objectives of analyzing call center performance and improving customer satisfaction. By implementing the suggested components and actions, you can effectively leverage Power BI to derive actionable insights from your data.



## DAX Formulas been used

#### Total Calls:
Total Calls = COUNT('Call Center_Call Center'[Id])

#### Total Call Duration (Minutes):
Total Call Duration (min) = SUM('Call Center_Call Center'[Call Duration In Minutes])

#### Total Call Duration (Hours):
Total Call Duration (hrs) = [Total Call Duration (min)] / 60

#### Response Time Percentage:
Response Time Percentage = CALCULATE(
    [Total Calls], 
    'Call Center_Call Center'[Response Time] = "Within SLA" || 'Call Center_Call Center'[Response Time] = "Above SLA"
) / [Total Calls]

#### Average Call Duration (Minutes):
Avg Call Duration (min) = AVERAGE('Call Center_Call Center'[Call Duration In Minutes])

### Additional Column:
#### Date Num:
Date Num = WEEKDAY('Date Table'[Date], 1)

Snap of new calculated column ,

![Snap_1]![Screenshot 2024-04-28 042505](https://github.com/somnath-97/Call-Center---Dashboard/assets/148855296/dfd8ba5e-47cc-4af6-9e58-770bf909ba01)

   
#### A short of the HOME page of the project.

![Snap_Count]![Screenshot 2024-04-28 033328](https://github.com/somnath-97/Call-Center---Dashboard/assets/148855296/39699c6e-4bc5-46cb-92b3-395a8405e1fb)


#### A short of the GRID page of the project.
 
 ![Snap_Percentage]![Screenshot 2024-04-28 033345](https://github.com/somnath-97/Call-Center---Dashboard/assets/148855296/d5d7df35-685d-4d4f-8be7-10841e7b7c14)

 
 
