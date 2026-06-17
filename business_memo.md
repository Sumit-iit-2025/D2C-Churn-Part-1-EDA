# Business Understanding Memo: Churn Retention Strategy

**To:** Product, Marketing, and Customer Support Leadership
**From:** Data Engineering & Analytics 
**Date:** 2025-09-30

## Executive Summary
Before deploying capital toward retention campaigns, we conducted an audit of customer behavior, support interactions, and transactional data up to the snapshot date. 

## Key Churn-Risk Hypotheses Identified

1. **The 120-Day Recency Drop-Off Hypothesis:** Recency is the strongest leading indicator of churn. Customers whose last purchase occurred over 129 days ago have a massive **89.2% probability of churning**. In contrast, customers who purchased within the last 25 days show only a 9.7% churn rate. Retention efforts must intercept customers long before the 4-month mark.

2. **The Second-Purchase Threshold Hypothesis:** The data reveals a clear retention milestone. Customers who have only made 1 purchase in the last 180 days churn at a high rate of **53.1%**. However, getting a customer to make a 3rd purchase drops their churn rate down to **16.1%**. Early onboarding campaigns should focus exclusively on driving that second and third order.

3. **The "Healthy Abandonment" App Hypothesis:** Counterintuitively, cart abandonment is a sign of healthy engagement, not just risk. Customers with 0 to 1 abandoned carts in the last 30 days actually churn at **50.1%**, while those with higher cart abandonment (>1) churn at only **24.3%**. A total lack of browsing/app exploration is a far more dangerous signal than abandoning a cart.

4. **The Baseline Discount Sensitivity Hypothesis:** Customers receiving an average discount of under 16% exhibit a severe **67.6% churn rate**. However, customers receiving mid-tier discounts (16%–26%) only churn at a rate of 36.2%. This suggests that removing discounts entirely to save margin will severely damage retention; the business must optimize the discount floor rather than eliminate it.

5. **The Loyalty Tier Buffer Hypothesis:** The loyalty program effectively reduces churn, but only at the highest tiers. Unenrolled customers and entry-level "Silver" members churn at a nearly identical high rate (~48%). However, customers who achieve "Gold" or "Platinum" status see their churn rates drop to **40.7%** and **37.1%** respectively. 

## Immediate Recommendations for Investigation
Before launching widespread retention campaigns, the business should investigate our **post-first-purchase onboarding flow**. Given that the churn rate plummets from 53% to 16% once a customer crosses the multi-purchase threshold, deploying a targeted, mid-tier discount (16-26%) specifically designed to convert first-time buyers into second-time buyers will yield the highest immediate ROI.
