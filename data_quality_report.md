# Data Quality Audit Report

## 1. Duplicate Records
* **Issue:** The `orders.csv` dataset contains intentional duplicate-like entries where the `order_id` ends with a `_DUP` suffix. 
* **Treatment Plan:** I will use pandas drop_duplicates to remove these before aggregating the order totals.

## 2. Missing Values
* **Issue:** `customers.csv` has missing values in `loyalty_tier` and `skin_type`. `orders.csv` contains null values in the `rating` column.
* **Treatment Plan:** I will fill missing categorical values like skin_type with 'Unknown' and impute the missing ratings with the median rating.

## 3. Outliers
* **Issue:** `gross_amount` in the orders table contains unusually high values.
* **Treatment Plan:** I will apply a cap (clipping) to the top 1% of gross_amount values so they do not skew the averages.

## 4. Date Consistency & Data Leakage
* **Issue:** `orders.csv` contains transaction rows dated after the strict snapshot date of 2025-09-30.
* **Treatment Plan:** Applied a strict datetime filter (`order_date <= '2025-09-30'`) prior to any aggregation to prevent target leakage.
