**Title: Customer Churn Prediction Analysis and Reduction Strategies**

**Problem Statement:**
Customer churn is a significant challenge that impacts business profitability. The goal is to predict whether customers will churn, allowing the business to take preemptive retention measures. This project uses machine learning models to predict churn, analyze data, and provide actionable strategies for reduction.


**Dataset Overview:**

Rows: 43,718

Columns: 17

Main Features: Transaction data (e.g., transaction_date, net_total, discount_amount), customer location data, and delivery details.

Key Data Cleaning Steps:

Datetime Conversion: Converted transaction_date and delivery_date to proper datetime types.

Duplicate Removal: Dropped 10 duplicate records.

Churn Definition: Churn is no purchases in the last 30 days.

**Feature Engineering:**

Order Frequency: Number of orders per customer.

Average Order Value: Mean value of purchases per customer.

Total Discounts: Cumulative discounts received by each customer.

Delivery Time: Time difference between transaction and delivery dates.

Discount Percentage: Ratio of discount to net total per transaction.

Label Encoding: Encoded customer_group and territory columns for modelling.

**Exploratory Data Analysis (EDA):**

Churn Distribution: 2.9% churned, 97.1% active customers.

Geographical Focus: Major territories include Kawangware, Juja, and Eastlands.

Customer Groups: Majority are individual customers.

**Key Insights:**

Churn by Customer Group: Higher churn for individuals.

Churn by Territory: The highest churn rate is in Nakuru, and the lowest is in Ruai.

Discount Amount: Higher discounts are correlated with better retention.

Bivariate & Multivariate Analysis:

Net Total vs. Quantity: Positive correlation (0.85).

Discount vs. Net Total: Positive correlation (0.90).

Churn Status: Higher discounts are associated with lower churn.

Correlation Heatmap:

Top Correlations:

total_qty and net_total (0.85)

net_total and discount_amount (0.90)

**Modelling:**

Train-Test Split:

X Features: Order frequency, total quantity, net total, total discounts, territory encoding, customer group encoding, etc.

Target: Churn (binary classification: 0 = No, 1 = Yes)

Handling Imbalance: Applied SMOTE to address class imbalance (since churn cases are few).

**Logistic Regression Results:**
Accuracy: 82%
Precision (Class 1): 12%
Recall (Class 1): 92%
F1-Score (Class 1): 21%

**Random Forest Results:**
Accuracy: 99%
Precision (Class 1): 81%
Recall (Class 1): 87%
F1-Score (Class 1): 84%
Decision Tree Results:
Accuracy: 98.98%

Classification Report: Balanced performance across churn and non-churn classes.

**Conclusion:**
Best Model: The Random Forest Classifier performed best, with an overall accuracy of 99% and strong F1 Scores for both churn and non-churn classes.

Key Drivers of Churn:
Order Frequency: Higher frequency is linked to lower churn.

Discount Amount: Offering greater discounts correlates with higher retention.

Territories: Geographical differences in churn rates suggest targeted regional interventions.

**Recommendations:**
Targeted Discounts: Use the predictive model to identify at-risk customers and offer tailored discounts to improve retention.

Territory-Based Interventions: Focus customer retention efforts on high-churn regions like Nakuru.

Improving Customer Engagement: Provide incentives or loyalty programs for individuals, as they have higher churn rates.
