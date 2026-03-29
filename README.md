# Food-Delivery-Operations-Analysis-SQL

#### This project analyzes food delivery operations data using MySQL to identify factors affecting delivery time and operational efficiency.  The analysis focuses on traffic conditions, weather, delivery workload, time of order, and location performance to understand what causes delays and how delivery performance can be improved.

---

## Business Problem

#### Food delivery services often face delays due to multiple operational factors such as traffic, weather, and workload.

* Drivers' relation with delivery delays
* Peak delay periods
* Conditions that negatively impact delivery performance

## Dataset Description

### Row: 45594
### Column:21

#### Food delivery is a service where restaurants or companies deliver ordered food to customers through online platforms or mobile apps. Deliveries are typically made using vehicles like cars, bikes, or scooters, depending on location.

#### Fields:
* ID (ID,	Delivery person ID)
* Delivery (person Age,	person Ratings, location latitude, location longitude
* Restaurant location ( latitude, longitude)
* Order (Date, Time, pickup Time) 
* Conditions(Weather,traffic density, Vehicle condition, Order Type , vehicle Type, No of deliveries,Festival,City	Time taken )

 ---

## Tools & Skills Used

#### MySQL

- SQL (Data Cleaning, Aggregations, CASE, GROUP BY)
- Data Cleaning & Transformation
- Feature Engineering
- Exploratory Data Analysis

## Steps in Data Cleaning and Validation 

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

---

## Key Business Questions

* Do traffic conditions affect delivery time?
* What weather conditions lead to delays?
* Which hours have the highest delivery time?
* Do multiple deliveries increase delivery time?
* Which cities have slower delivery performance?
* Do festivals impact delivery efficiency?
* Does vehicle type affect delivery speed?
* Do driver rating and age influence delivery time?
* How do combined factors (traffic + weather) impact delivery time?
  
## Key Analysis Performed

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

---

## Project Structure

* food-delivery-operations-analysis
* │
* ├── 01_database_setup.sql
* ├── 02_data_inspection.sql
* ├── 03_data_cleaning.sql
* ├── 04_data_validation.sql
* ├── 05_analysis.sql
* └── README.md

---

## Top 5 Insights of this Project 

#### 1. Order and Time in Different Conditions 
<img width="335" height="127" alt="image" src="https://github.com/user-attachments/assets/e02bbd64-3501-4d35-9322-de80279a0728" />
#### Delivery time increases significantly with higher traffic levels, with traffic jams causing the longest delays, making traffic one of the most critical factors affecting delivery performance.

#### 2. Impact of Festival on Delivery Time
<img width="359" height="98" alt="image" src="https://github.com/user-attachments/assets/912b88db-6019-4876-be0c-6578b963ac9e" />
#### Deliveries during festivals take significantly longer, with average delivery time nearly doubling compared to non-festival periods, indicating increased operational load and congestion.

#### 3. Impact of Multiple Deliveries on Delivery Time
<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/ac776087-d18d-41c1-bc8b-a14652ff6e88" />
#### Delivery time increases significantly as the number of assigned deliveries increases, with orders involving multiple deliveries taking nearly twice as long compared to single deliveries.

#### 4. Impact of Weather Conditions on Delivery Time
<img width="423" height="156" alt="image" src="https://github.com/user-attachments/assets/6e62fd2e-992f-4dfb-a38e-66058314def6" />
#### Poor weather conditions increase delivery time, while sunny conditions result in faster deliveries.

#### 5. Peak Delay Periods Under High Traffic Conditions
<img width="402" height="176" alt="image" src="https://github.com/user-attachments/assets/5ac161c4-a9ff-4cc4-bdb2-15692be4ceae" />
#### The highest delivery delays occur during late evening hours under traffic jam conditions, indicating peak congestion periods as the primary driver of maximum delivery time.

---

### What I Learned
1. How to clean and prepare real-world messy datasets
2. How to perform operational analysis using SQL
3. How to analyze multiple factors affecting performance
4. How to convert raw data into actionable business insights
   
### Conclusion

This project demonstrates how SQL can be used to analyze operational data, identify delivery inefficiencies, and generate insights to improve delivery performance.
