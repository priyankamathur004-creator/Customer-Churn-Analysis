## OTT Customer Churn & Engagement Analytics System
 # Project Overview
 This project addresses a critical business challenge for a subscription-based digital OTT platform: understanding customer churn and inconsistent user engagement. 
 By integrating fragmented data across multiple touchpoints (demographics, subscription tiers, platform usage, and support logs), this analytics solution provides a $360^{\circ}$ view of the customer lifecycle.
 The primary goal is to uncover data-driven insights to identify at-risk users, evaluate the impact of customer support and service upgrades, and optimize retention strategies to maximize customer lifetime value (CLV).

# Key Features & Architecture
1. Data Integration & Cleaning
Unified Pipeline: Integrated five disparate data streams (Customers, Subscriptions, Usage, Support, and Churn) into a single, clean master dataset of 4,000 unique records.

Data Sanitation: Handled missing values, standardized timestamps (JoinDate, LastLoginDate, ChurnDate), and eliminated duplicate entries.

2. Advanced Feature Engineering

 To deepen behavioral tracking, several custom metrics were calculated:Customer Tenure: Measures total customer relationship duration ($Today - JoinDate$).
 Recency Tracking: Calculated DaysSinceLastLogin to monitor immediate inactivity risks.
 Engagement Score: A composite metric blending platform usage and feedback loops:$$\text{Engagement Score} = f(\text{WatchHoursPerWeek}, \text{AvgRatingGiven})$$
 Financial Metrics: Derived RevenueGenerated per customer based on subscription tier histories.

# 3. Customer Segmentation & Behavioral Insights

Tiered Segmentation: Classified users into High, Medium, and Low Engagement segments based on custom behavioral thresholds.

Churn Diagnostics: Analyzed the correlation between operational metrics (e.g., SupportTickets, SubscriptionType) and the eventual churn status (Is_Churned).

Upgrade Effectiveness: Evaluated how offering and accepting premium upgrades influences retention.

#  Dataset Insights & Schema
The final engineered dataset contains the following core dimensions:

Demographics: Age, Gender, City (Primary market: Mumbai)

Subscription Details: SubscriptionType (Basic, Standard, Premium), MonthlyFee, DevicesUsed, PaymentMethod

Engagement Metrics: WatchHoursPerWeek, AvgRatingGiven, Engagement_Score, Customer_segmentation

Operational Logs: SupportTickets, UpgradeOffered, UpgradeAccepted

Status Indicators: Status, ChurnDate, Customer_Tenure, Is_Churned, RevenueGenerated

# Dashboard Overview

<img width="813" height="463" alt="image" src="https://github.com/user-attachments/assets/5a7881ca-2531-4d5c-b99a-90a998472f8e" />


# Tech Stack Used
Language: Python

Libraries: Pandas, NumPy (Data manipulation & Feature Engineering)

Development Environment: Jupyter Notebook

Target BI Tooling: Power BI (for dashboard development)

# Deliverables Included
Customer_data.xlsx / CustomerOtt_Final_Clean.csv: The finalized, clean, feature-engineered dataset ready for modeling/dashboard consumption.

Untitled-1.ipynb: The core Exploratory Data Analysis (EDA) and data engineering pipeline notebook.

Project Documentation: Complete mapping from business requirements to technical implementation.
