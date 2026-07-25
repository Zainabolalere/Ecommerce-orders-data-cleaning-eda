# E COMMERCE ORDERS: DATA CLEANING & EXPLORATORY ANALYSIS (PYTHON)

## TABLE OF CONTENTS
- [Description](#description)
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Dataset](#dataset)
- [Insights](#insights)
- [Recommendations](#recommendations)
- [Contact](#contact)

## Description
This project uses Python (pandas, matplotlib, seaborn) to clean a raw e commerce orders dataset and explore it for patterns in order value, pricing, and customer behavior.

## Overview
The dataset contains 1,200 order records across 14 columns, covering product details, pricing, payment methods, order status, shipping addresses, coupon usage, and referral sources.

The project covers two phases: cleaning the raw data into an analysis ready state, then exploring it through distribution analysis, outlier detection, and correlation analysis.

## Problem Statement
The raw dataset contained missing values, unverified duplicate identifiers, and inconsistent date and currency formatting. Beyond cleaning, the business needed to understand what patterns exist in customer order behavior, in terms of value, pricing, and quantity, and what that means for decision making.

## Objectives

1️⃣ Clean the raw dataset by handling missing values, duplicates, and inconsistent formatting.

2️⃣ Understand the shape, spread, and outliers within order value data.

3️⃣ Analyze relationships between quantity, price, cart size, and total order value.

4️⃣ Provide data driven recommendations based on the findings.

## Tools
Python for data cleaning, exploratory analysis, and visualization

pandas for data manipulation, matplotlib and seaborn for visualization

## Data Cleaning
The following data cleaning steps were performed to ensure data quality:

Filled 309 missing CouponCode values with an explicit 'No Coupon' label rather than a statistical guess, since the blanks represented orders where no coupon was used

Audited OrderID and TrackingNumber for duplicates, confirming zero duplicates across all 1,200 rows

Converted the Date column from text to a true datetime type (ISO 8601)

Rounded UnitPrice and TotalPrice to 2 decimal places, while leaving Quantity and ItemsInCart as whole numbers since they represent counts, not currency

## Dataset
The dataset used for this project is `Dataset_for_Data_Analytics_Sheet1.csv`, containing 1,200 rows and 14 columns: OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, and TotalPrice.

## Insights
1️⃣ Order Value Distribution

TotalPrice is right skewed. The mean order value (₦1,053.97) sits 28% above the median (₦823.62), meaning a small number of large orders pull the average upward.

2️⃣ High Value Orders

8 orders (0.67% of the dataset) fall above the IQR outlier threshold, all at maximum Quantity (5) on premium products such as Tablet, Laptop, Monitor, and Printer. These are verified legitimate high value orders, not data errors.

3️⃣ Price Point vs Quantity

UnitPrice correlates with TotalPrice more strongly (0.72) than Quantity does (0.62), meaning what customers buy matters slightly more than how many units they buy.

4️⃣ Cart Size vs Purchase Value

ItemsInCart shows only weak correlation with TotalPrice (0.39), suggesting cart contents and final purchase reflect different stages of the customer journey rather than cart size being a reliable predictor of spend.

## Recommendations
1️⃣ Reporting Standard → Use the median (₦823.62), not the mean (₦1,053.97), when reporting typical order value, since the mean is skewed by a small number of large orders.

2️⃣ Customer Retention → Flag the 8 high value orders as a VIP customer segment for retention outreach, not fraud review.

3️⃣ Product Strategy → Prioritize premium product visibility over cart size driven promotions, since price point is the stronger driver of revenue.

4️⃣ Forecasting → Avoid using ItemsInCart alone to forecast order value, given its weak relationship with actual spend.

## Contact

Created by **Zainab Olalere**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/zainabolalere)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/Zainabolalere)
