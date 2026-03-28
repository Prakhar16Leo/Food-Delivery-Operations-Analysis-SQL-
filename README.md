# Food-Delivery-Operations-Analysis-SQL

## This project analyzes food delivery operations data using MySQL to identify factors affecting delivery time and operational efficiency.  The analysis focuses on traffic conditions, weather, delivery workload, time of order, and location performance to understand what causes delays and how delivery performance can be improved.

## Business Problem

Food delivery services often face delays due to multiple operational factors such as traffic, weather, and workload.

This project aims to identify:

Key drivers of delivery delays
peak delay periods
conditions that negatively impact delivery performance
📊 Dataset Description
Dataset: Food Delivery Orders
Each row represents one delivery
Key fields:
order time and pickup time
traffic condition
weather condition
city
delivery duration
delivery partner details
🛠️ Tools & Skills Used
MySQL
SQL (Data Cleaning, Aggregations, CASE, GROUP BY)
Data Cleaning & Transformation
Feature Engineering
Exploratory Data Analysis
⚙️ Approach
1. Data Cleaning
Converted "NaN" values to NULL
Standardized text fields using TRIM and NULLIF
Converted date and time columns into proper formats
Created cleaned table: deliveries_clean
2. Feature Engineering
Created delivery_minutes from raw text
Extracted order_hour from order time
Built analysis-ready view: deliveries_analysis
3. Data Validation
Checked for null values across key columns
Verified duplicate records using ID
Validated delivery time ranges
Filtered invalid rows (missing time or delivery values)
4. Analysis

Performed SQL-based analysis using:

aggregations (AVG, COUNT)
grouping (GROUP BY)
conditional logic (CASE)
multi-factor comparisons
❓ Key Business Questions
Does traffic condition affect delivery time?
What weather conditions lead to delays?
Which hours have the highest delivery time?
Do multiple deliveries increase delivery time?
Which cities have slower delivery performance?
Do festivals impact delivery efficiency?
Does vehicle type affect delivery speed?
Do driver rating and age influence delivery time?
How do combined factors (traffic + weather) impact delivery time?
📈 Key Analysis Performed
Delivery time by traffic condition
Delivery time by weather condition
Hour-wise delivery performance
Impact of multiple deliveries
City-level performance analysis
Festival and vehicle type impact
Driver performance (rating and age)
Pickup delay analysis
Multi-factor analysis (traffic + weather, traffic + hour)
🔍 Key Findings
High traffic conditions significantly increase delivery time
Weather conditions such as fog and rain contribute to delays
Peak delays occur during evening hours
Multiple deliveries per rider increase delivery time
Some cities consistently show higher delivery times
Lower-rated drivers tend to have slightly higher delivery times
Pickup delays also contribute to overall delivery delay
💡 Business Recommendations
Increase delivery partner allocation during peak hours
Avoid assigning multiple deliveries during high traffic periods
Optimize routing based on traffic conditions
Implement weather-aware delivery planning
Focus on improving operations in high-delay cities
Reduce pickup delays through better coordination with restaurants
📁 Project Structure
food-delivery-operations-analysis
│
├── 01_database_setup.sql
├── 02_data_inspection.sql
├── 03_data_cleaning.sql
├── 04_data_validation.sql
├── 05_analysis.sql
└── README.md
📌 What I Learned
How to clean and prepare real-world messy datasets
How to perform operational analysis using SQL
How to analyze multiple factors affecting performance
How to convert raw data into actionable business insights
✅ Conclusion

This project demonstrates how SQL can be used to analyze operational data, identify delivery inefficiencies, and generate insights to improve delivery performance.
