**E-Commerce Customer Churn Analysis**
**📌 Project Overview**

This project analyzes e-commerce customer churn using historical customer and transactional data to identify patterns and factors associated with customer attrition.

The analysis focuses on customer tenure, purchase behavior, preferred payment methods, satisfaction scores, complaints, cashback, and other customer attributes to understand churn behavior and generate insights that can support customer retention strategies and business decision-making.

**🎯 Problem Statement**

Customer churn is a major challenge for e-commerce businesses because losing existing customers can impact revenue and long-term profitability.

This project aims to:

Identify the number of churned and active customers.
Analyze customer behavior and characteristics associated with churn.
Understand the relationship between complaints, satisfaction, and churn.
Analyze purchasing patterns, payment preferences, and order categories.
Identify factors that may contribute to customer attrition.
Generate actionable insights to support customer retention strategies.
📂 Dataset

The dataset contains customer demographics, purchasing behavior, satisfaction information, payment preferences, and churn-related attributes.

Key Features
Customer ID
Gender
Tenure
City Tier
Warehouse-to-Home Distance
Preferred Login Device
Preferred Payment Mode
Preferred Order Category
Satisfaction Score
Number of Devices Registered
Number of Address
Complain
Coupon Used
Order Count
Cashback Amount
Churn

Dataset: Download E-Commerce Customer Churn Dataset

🧹 Data Cleaning

The following data-cleaning techniques were applied:

Handled missing values using mean imputation for:
WarehouseToHome
HourSpendOnApp
OrderAmountHikeFromLastYear
DaySinceLastOrder
Applied mode imputation for:
Tenure
CouponUsed
OrderCount
Removed records where WarehouseToHome > 100 to handle extreme outliers.
Standardized inconsistent values in login device and order category columns.
Standardized payment modes:
COD → Cash on Delivery
CC → Credit Card
🔄 Data Transformation

The dataset was transformed to improve consistency and analysis:

Renamed PreferedOrderCat to PreferredOrderCat.
Renamed HourSpendOnApp to HoursSpentOnApp.
Created ComplaintReceived:
Yes when Complain = 1
No otherwise
Created ChurnStatus:
Churned when Churn = 1
Active otherwise
Removed the original Churn and Complain columns after creating the descriptive fields.
Created Warehouse Distance Categories:
≤5 km → Very Close Distance
≤10 km → Close Distance
≤15 km → Moderate Distance




15 km → Far Distance

📊 Data Analysis

The project explores customer churn from multiple perspectives.

🔹 Customer Churn Analysis
Counted Churned vs. Active customers.
Calculated the average tenure of churned customers.
Calculated the total cashback amount received by churned customers.
Determined the percentage of churned customers who complained.
🔹 Customer Behavior Analysis
Identified the city tier with the highest number of churned customers in the Laptop & Accessory category.
Identified the most preferred payment mode among active customers.
Analyzed order amount increases among single customers preferring mobile phones.
Calculated average registered devices among customers using UPI.
Identified the city tier with the highest number of customers.
Identified the gender using the highest number of coupons.
🔹 Order & Category Analysis
Analyzed customer count and maximum app usage hours by preferred order category.
Calculated total order count for customers using credit cards with the maximum satisfaction score.
Identified order categories preferred by customers using more than five coupons.
Identified the top 3 order categories by average cashback amount.
🔹 Satisfaction & Complaint Analysis
Calculated the average satisfaction score of customers who complained.
Examined the relationship between customer complaints and churn.
Analyzed churn status across different warehouse-to-home distance categories.
🔹 Advanced Customer Analysis
Identified payment modes of customers with an average tenure of 10 months and more than 500 orders.
Retrieved order details for married customers living in City Tier-1 whose order count exceeded the overall average.
Analyzed return transactions for customers who had churned and submitted complaints.
🗄️ SQL Analysis

A customer_returns table was created in the ecomm database to analyze customer returns.

The table includes:

ReturnID
CustomerID
ReturnDate
RefundAmount

The return data was then joined with customer information to identify churned customers who had also submitted complaints and made returns.

🛠️ Tools & Technologies
SQL / MySQL
Data Cleaning
Filtering
Aggregations
GROUP BY
Subqueries
Joins
Conditional Logic
Table Creation
Data Insertion
Data Analysis
Customer Churn Analysis
Customer Segmentation
Behavioral Analysis
Aggregation & Trend Analysis
💡 Key Insights

The project helps identify:

The proportion of customers who are churned vs. active.
Customer characteristics and behaviors associated with churn.
The impact of complaints and satisfaction levels on customer retention.
Preferred payment methods and order categories among different customer groups.
Customer purchasing behavior based on tenure, coupons, orders, and cashback.
Churn patterns across different city tiers and warehouse distances.
Customer return behavior among churned and complaining customers.
High-performing order categories based on average cashback.                                                               
📁 Project Structure
E-Commerce-Customer-Churn-Analysis/
│
├── Dataset/
│   └── E-Commerce Customer Churn Dataset
│
├── SQL/
│   └── Customer Churn Analysis.sql
│
├── README.md
│
└── Results/
    └── Analysis Results
🎯 Project Outcome

This project demonstrates practical skills in SQL, data cleaning, data transformation, customer segmentation, exploratory analysis, aggregation, joins, and business-oriented data analysis.

The analysis provides insights into customer churn drivers and purchasing behavior, helping e-commerce businesses identify at-risk customers and develop targeted customer retention strategies.
