# Credit Risk Analysis 

## Project Overview

This project simulates a typical Data Analyst task — exploring and analyzing credit card clients' data to identify risk factors associated with credit default. We use the well-known **UCI Credit Card Default Dataset**, containing demographic, financial, and payment history information.

---

## Project Goals

* Understand the profile of clients likely to default on payments
* Identify key factors influencing default risk
* Analyze historical repayment behavior and its correlation with defaults
* Explore financial variables such as bill amounts, credit limits, and payment patterns
* Provide actionable insights based on data exploration

---

## Dataset Summary

* **Total records:** 30,000 clients
* **Target variable:** `default.payment.next.month` (1 = default, 0 = no default)

**Key variables:**

* Demographics: `SEX`, `EDUCATION`, `MARRIAGE`, `AGE`
* Credit Limit: `LIMIT_BAL`
* Repayment Status (last 6 months): `PAY_0` to `PAY_6`
* Bill Amounts: `BILL_AMT1` to `BILL_AMT6`
* Payment Amounts: `PAY_AMT1` to `PAY_AMT6`

---

## Business Questions to Answer

* What demographic groups are associated with a higher risk of default?
* How does previous repayment behavior influence the likelihood of default?
* Are there significant correlations between financial indicators (e.g., credit limit, bill amount) and default?
* What percentage of clients tend to default? Is the data imbalanced?
* Can we segment clients based on their risk profile?
* Are there statistically significant differences between defaulters and non-defaulters?

---

## Analysis Plan

1. **Data Cleaning & Preprocessing**
2. **Exploratory Data Analysis (EDA)**

   * Target variable distribution
   * Demographic analysis
   * Repayment history exploration
   * Correlation analysis
3. **Visualization of Insights**
4. **Statistical Testing (U-test, Chi-square)**
5. **Business Recommendations & Conclusions**

---

## Tools & Technologies

* **Python (Pandas, Seaborn, Matplotlib)**
* **Jupyter Notebook**
* *(Optional)* Tableau / Power BI for dashboard creation

---

## Conclusion

This project reflects a real-world analytical workflow — from data exploration to actionable insights — simulating the role of a business data analyst working with financial risk data.

---

*This is a personal learning project aimed at practicing data analysis skills.*

## [Check dashboard on Google Sheets]([https://docs.google.com/spreadsheets/d/ID_ТВОГО_ФАЙЛУ](https://docs.google.com/spreadsheets/d/1hw0Hc1at1As9ak680XT4Z10BMpS-HcAxHmTBEltydpY/edit?usp=sharing))
