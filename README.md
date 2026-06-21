[Wersja polska (Polish version)](./README_PL.md)
# Telco-Customer-Churn-Analysis
This project analyzes customer churn in a telecommunications company using Python for data preparation and Power BI for business intelligence reporting. 

The objective was to identify the key factors associated with customer attrition, quantify the financial impact of churn, and provide actionable recommendations to improve customer retention. The project combines data engineering, exploratory data analysis (EDA), dimensional modeling, DAX calculations, and dashboard development to transform raw customer data into actionable business insights.

---
## Dataset
The dataset used in this project comes from Kaggle:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data

The dataset contains customer demographic information, subscribed services, contract details, billing information, and churn status for over 7,000 telecommunications customers.

---

## Business Question
> **Which customer characteristics and service patterns are most strongly associated with customer churn, and where should retention efforts be focused?**

---

## Project Structure & Workflow
### 1. Data Preparation & Cleaning (Python)
The dataset was cleaned, engineered, and transformed using Python and **Pandas**. Key preprocessing steps included:
* Converting `TotalCharges` to a numeric format.
* Handling missing values.
* Creating customer tenure segments.
* Calculating the total number of subscribed services per customer.
* Performing exploratory data analysis (EDA).
* Analyzing correlations between numerical variables.
* Exporting a cleaned dataset for Power BI.

---

### 2. Data Modeling (Power BI)
To improve scalability, data integrity, and reporting performance, the original flat dataset was refactored into a **Star Schema** model.

* **Fact Table:** `Fact_Churn`.
* **Dimension Tables:** `Dim_Demographics`, `Dim_Services`, `Dim_Contracts`.
* **Relationship Design:** Strict **One-to-many (1:N)** relationships, optimized for analytical reporting and DAX calculations.

---

### 3. Dashboard Development
An interactive dashboard was built in Power BI to provide insights into customer churn and revenue loss.

Key dashboard features include:
* Dynamic filtering by customer demographics and services.
* Churn analysis by tenure.
* Churn analysis by contract type.
* Churn analysis by payment method.
* Customer service adoption analysis.
* Revenue loss monitoring.

---

## Key Metrics (DAX)

* **Total Customers:** Unique count of customers in the dataset.
* **Churn Rate:** Percentage of customers who left the company.
* **Lost Revenue:** Estimated monthly revenue lost due to customer churn.

---

## Key Findings & Strategic Recommendations

### Customers Are Most Likely to Churn During Their First Year
Customers with less than 12 months of tenure showed the highest churn rates.

This finding is supported by a moderate negative correlation (-0.35) between customer tenure and churn.

**Recommendation:**
* Improve onboarding processes.
* Introduce first-year loyalty programs.
* Increase proactive customer engagement during the first 12 months.

### Contract Type Has a Strong Impact on Retention
Customers on month-to-month contracts were significantly more likely to leave than customers with longer commitments.

**Recommendation:**
* Encourage migration to longer-term contracts.
* Offer retention discounts for annual contracts.
* Introduce loyalty incentives for contract renewals.

### Payment Method Is Associated With Churn Risk
Customers using Electronic Check showed noticeably higher churn rates than customers using automatic payment methods.

**Recommendation:**
* Promote AutoPay enrollment
* Offer small incentives for switching to automated payments
* Reduce payment friction where possible

---

## Tools & Technologies
* **Python:** Pandas, NumPy, Matplotlib, Seaborn
* **Power BI Desktop:** Power Query, Star Schema Modeling, DAX (Data Analysis Expressions)
