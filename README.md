# Food-Delivery-Operations-Analysis-SQL

## This project analyzes food delivery operations data using MySQL to identify factors affecting delivery time and operational efficiency.  The analysis focuses on traffic conditions, weather, delivery workload, time of order, and location performance to understand what causes delays and how delivery performance can be improved.

## Business Problem

#### Food delivery services often face delays due to multiple operational factors such as traffic, weather, and workload.

Key drivers of delivery delays
peak delay periods
conditions that negatively impact delivery performance

### Dataset Description

#### Food delivery is a service where restaurants or companies deliver ordered food to customers through online platforms or mobile apps. Deliveries are typically made using vehicles like cars, bikes, or scooters depending on location.

#### Row: 45594
#### Column:21
#### fields:
ID,	Delivery_person_ID,Delivery_person_Age,	Delivery_person_Ratings,Restaurant_latitude,Restaurant_longitude,	Delivery_location_latitude,Delivery_location_longitude,Order_Date,Time_Orderd,Time_Order_picked,Weatherconditions	Road_traffic_density,Vehicle_condition,Type_of_order,Type_of_vehicle,multiple_deliveries,Festival,City	Time_taken(min)

 ---
### Tools & Skills Used
#### MySQL

- SQL (Data Cleaning, Aggregations, CASE, GROUP BY)
- Data Cleaning & Transformation
- Feature Engineering
- Exploratory Data Analysis

### Steps in Data Cleaning and Validation 

#### 1. Data Cleaning

1. Converted "NaN" values to NULL
2. Standardized text fields using TRIM and NULLIF
3. Converted date and time columns into proper formats
4. Created cleaned table: deliveries_clean
   
#### 2. Feature Engineering

1. Created delivery_minutes from raw text
2. Extracted order_hour from order time
3. Built analysis-ready view: deliveries_analysis

#### 3. Data Validation

1. Checked for null values across key columns
2. Verified duplicate records using ID
3. Validated delivery time ranges
4. Filtered invalid rows (missing time or delivery values
   
#### 4. Analysis

Performed SQL-based analysis using:

* Aggregations (AVG, COUNT, Sum, MIN, Max)
* Grouping (GROUP BY)
* Conditional logic (CASE)
* Multi-factor comparisons
* Cleaning ( Cast, NUllif, Trim)

### Key Business Questions

* Do traffic conditions affect delivery time?
* What weather conditions lead to delays?
* Which hours have the highest delivery time?
* Do multiple deliveries increase delivery time?
* Which cities have slower delivery performance?
* Do festivals impact delivery efficiency?
* Does vehicle type affect delivery speed?
* Do driver rating and age influence delivery time?
* How do combined factors (traffic + weather) impact delivery time?
  
### Key Analysis Performed

* Delivery time is affected by traffic conditions
* Delivery time is affected by weather conditions
* Hour-wise delivery performance
* Impact of multiple deliveries
* City-level performance analysis
* Festival and vehicle type impact
* Driver performance (rating and age)
* Pickup delay analysis
* Multi-factor analysis (traffic + weather, traffic + hour)
  
### Key Findings

* High traffic conditions significantly increase delivery time
* Weather conditions such as fog and rain contribute to delays
* Peak delays occur during evening hours
* Multiple deliveries per rider increase delivery time
* Some cities consistently show higher delivery times
* Lower-rated drivers tend to have slightly higher delivery times
* Pickup delays also contribute to the overall delivery delay
  
### Business Recommendations

* Increase delivery partner allocation during peak hours
* Avoid assigning multiple deliveries during high traffic periods
* Optimize routing based on traffic conditions
* Implement weather-aware delivery planning
* Focus on improving operations in high-delay cities
* Reduce pickup delays through better coordination with restaurants

### Project Structure

food-delivery-operations-analysis
│
├── 01_database_setup.sql
├── 02_data_inspection.sql
├── 03_data_cleaning.sql
├── 04_data_validation.sql
├── 05_analysis.sql
└── README.md

### What I Learned
1. How to clean and prepare real-world messy datasets
2. How to perform operational analysis using SQL
3. How to analyze multiple factors affecting performance
4. How to convert raw data into actionable business insights
   
### Conclusion

This project demonstrates how SQL can be used to analyze operational data, identify delivery inefficiencies, and generate insights to improve delivery performance.
