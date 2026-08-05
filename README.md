# E-COMMERCE ORDERS: DATA CLEANING & PREPARATION (PYTHON)

## TABLE OF CONTENTS
- [Description](#description)
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Dataset](#dataset)
- [Verification Results](#verification-results)
- [Contact](#contact)

## Description
This project uses Python (pandas) to clean a raw e-commerce orders dataset, handling missing values, duplicate identifiers, and inconsistent formatting to produce an analysis-ready dataset. It's Part 1 of a two-part project — see Part 2: [Exploratory Data Analysis](https://github.com/Zainabolalere/project-2-eda).

## Overview
The raw dataset contains 1,200 order records across 14 columns, covering product details, pricing, payment methods, order status, shipping addresses, coupon usage, and referral sources.

## Problem Statement
The raw dataset contained missing values, unverified duplicate identifiers, and inconsistent date and currency formatting, making it unfit for reliable analysis. This project audits and resolves those issues to produce a clean, trustworthy dataset for downstream analysis.

## Objectives

1️⃣ Audit the raw dataset for missing values, duplicates, and formatting inconsistencies.

2️⃣ Resolve missing values using business logic rather than statistical guesses.

3️⃣ Standardize date and currency formats across all rows.

4️⃣ Verify the cleaned dataset meets integrity checks before handoff to analysis.

## Tools
Python for data cleaning

pandas for data manipulation and integrity auditing

## Data Cleaning
The following data cleaning steps were performed to ensure data quality:

1️⃣ Filled 309 missing CouponCode values with an explicit 'No Coupon' label rather than a statistical guess (mean/median/mode don't apply meaningfully here), since the blanks represented orders where no coupon was used — a legitimate business state, not an error

2️⃣ Audited OrderID and TrackingNumber for duplicates, confirming zero duplicates across all 1,200 rows

3️⃣ Converted the Date column from text to a true datetime type (ISO 8601)

4️⃣ Rounded UnitPrice and TotalPrice to 2 decimal places, while leaving Quantity and ItemsInCart as whole numbers since they represent counts, not currency

## Dataset
The dataset used for this project is `Dataset_for_Data_Analytics_Sheet1.csv`, containing 1,200 rows and 14 columns:

- **OrderID** — unique identifier for each order
- **Date** — date the order was placed
- **CustomerID** — unique identifier for each customer
- **Product** — the product purchased (e.g. Chair, Laptop, Printer)
- **Quantity** — number of units purchased in the order
- **UnitPrice** — price per unit of the product
- **ShippingAddress** — address the order was shipped to
- **PaymentMethod** — how the customer paid (e.g. Cash, Online, Credit Card)
- **OrderStatus** — current status of the order (e.g. Delivered, Cancelled, Pending)
- **TrackingNumber** — unique shipment tracking code for the order
- **ItemsInCart** — number of items in the customer's cart at checkout
- **CouponCode** — coupon applied to the order, if any
- **ReferralSource** — how the customer found the store (e.g. Instagram, Email, Google)
- **TotalPrice** — final order value (Quantity × UnitPrice)

## Verification Results
The cleaned dataset passed the following checks:

| Check | Result |
|---|---|
| Duplicate OrderIDs | 0 |
| Duplicate TrackingNumbers | 0 |
| Missing values remaining | 0 |
| Date format compliance | 100% ISO 8601 |

Full change log available in [`Data Cleaning and Preparation Change Log`](./CHANGE_LOG.md).

## Contact

Created by **Zainab Olalere**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/zainabolalere)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/Zainabolalere)
