Credit Risk Analysis

## Project Overview

This project presents a comprehensive Exploratory Data Analysis (EDA) of the **UCI Credit Card Default Dataset**. The primary goal is to identify the key factors and behavioral patterns that are strong predictors of credit default. By analyzing demographic data, financial history, and payment behavior, this project simulates the work of a data analyst aiming to provide actionable insights for risk management in a financial institution.

-----

## Project Goals

  * **Identify Key Drivers:** Determine the most significant variables that correlate with a client defaulting on their credit card payments.
  * **Profile At-Risk Clients:** Create a profile of clients who are most likely to default based on their financial and demographic characteristics.
  * **Analyze Payment Behavior:** Investigate how past repayment statuses, bill amounts, and payment amounts influence the likelihood of future defaults.
  * **Provide Business Recommendations:** Translate data-driven insights into actionable strategies for minimizing credit risk and improving client monitoring.

-----

## Dataset

  * **Source:** [UCI Machine Learning Repository: Default of Credit Card Clients Dataset](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)
  * **Total Records:** 30,000 clients
  * **Features:** 24, including demographic information, credit limit, historical payment status, bill statements, and past payments.
  * **Target Variable:** `default payment next month` (1 = default, 0 = no default).

**Key Variables:**

  * `LIMIT_BAL`: Amount of given credit (NT dollar).
  * `SEX`: Gender (1=male, 2=female).
  * `EDUCATION`: (1=graduate school, 2=university, 3=high school, 4=others).
  * `MARRIAGE`: Marital status (1=married, 2=single, 3=others).
  * `AGE`: Age in years.
  * `PAY_0` to `PAY_6`: Repayment status in the last 6 months (e.g., -1=pay duly, 1=payment delay for one month, 2=payment delay for two months, …).
  * `BILL_AMT1` to `BILL_AMT6`: Amount of bill statement in the last 6 months.
  * `PAY_AMT1` to `PAY_AMT6`: Amount of previous payment in the last 6 months.

-----

## Tools and Technologies

  * **Language:** Python
  * **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
  * **Environment:** Jupyter Notebook (Google Colab)

-----

## Analysis & Key Findings

The analysis revealed several critical factors that strongly influence the probability of a client defaulting.

### 1\. Repayment History is the Strongest Predictor

The status of past payments (`PAY_0`...`PAY_6`) is the most significant indicator of default risk.

  * **Critical Point: 2+ Month Delay:** The default rate skyrockets for clients with a payment delay of two or more months. These clients have a **69% to 77% probability of defaulting** in the next month.
  * **Early Warning Sign:** A delay of just one month (`PAY_0 = 1`) increases the default risk to **34%**, which is significantly higher than the average default rate of 22%.
  * **Reliable Clients:** Clients who pay on time or early (`PAY_` value of 0, -1, or -2) have the lowest default rates, ranging from **13% to 17%**.

### 2\. Financial Indicators Offer Clear Insights

  * **Credit Limit (`LIMIT_BAL`):** There is a clear inverse relationship. Clients who defaulted have a significantly lower median credit limit (\~80,000 NT$) compared to those who did not (\~150,000 NT$). This suggests that lower credit limits are associated with higher risk.
  * **Payment Amount (`PAY_AMT`):** Non-defaulters consistently make larger payments than defaulters. The boxplots of the log-transformed payment amounts clearly show that the median payments for non-defaulters are substantially higher across all six months.
  * **Bill Amount (`BILL_AMT`):** This factor is less predictive. The bill amounts for both groups are widely distributed. However, the median bill amount for defaulters is slightly lower, which may indicate lower overall financial activity.

### 3\. Demographic Profile of Defaulters

While less impactful than behavioral data, some demographic trends emerged:

  * **Education (`EDUCATION`):** Default risk decreases as education level increases.
      * High School graduates have the highest default rate (**25.2%**).
      * University graduates have a rate of **23.7%**.
      * Graduate School alumni have the lowest rate (**19.2%**).
  * **Gender (`SEX`):** Men show a slightly higher tendency to default (**24.2%**) compared to women (**20.8%**).
  * **Marital Status (`MARRIAGE`):** Married clients have a slightly higher default rate (**23.5%**) than single clients (**20.9%**).
  * **Age (`AGE`):** The analysis showed a very slight increase in default risk with age, but the trend is not strong enough to be a primary predictor. The highest default rate is observed in the 50-65 age group.

### 4\. Overall Default Rate & Data Imbalance

  * The dataset is **imbalanced**, with **22.1%** of clients defaulting and **77.9%** paying on time. This is a critical consideration for any future machine learning modeling.

-----

## Business Recommendations

Based on these findings, the following actions are recommended to mitigate credit risk:

1.  **Implement an Early Warning System:**

      * For clients with a **one-month delay (`PAY_` = 1)**, trigger automated alerts and offer flexible payment options to prevent further delinquency.
      * For clients with a **two-month delay or more (`PAY_` ≥ 2)**, implement stricter measures such as temporarily freezing the credit line and assigning a risk agent for personalized follow-up.

2.  **Refine Credit Limit Policies:**

      * Incorporate `LIMIT_BAL` and `EDUCATION` level into credit scoring models. New applicants with lower education levels and no established credit history could be assigned more conservative initial credit limits.
      * Offer performance-based credit limit increases to clients who consistently pay on time.

3.  **Encourage Proactive Repayments:**

      * Develop loyalty programs that reward clients for making timely and substantial payments (`PAY_AMT`). This could include cashback incentives or reduced interest rates.

4.  **Segment Client Communication:**

      * Tailor communication and financial education resources based on demographic segments. For example, provide financial literacy tools for younger clients or those with a high school education to help them manage their credit better.

-----

## How to Run This Project

1.  Clone the repository:
    ```bash
    git clone https://github.com/ilyayath/credit-risk-analysis.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd credit-risk-analysis
    ```
3.  Install the required libraries:
    ```bash
    pip install pandas numpy seaborn matplotlib openpyxl
    ```
4.  Launch Jupyter Notebook and open the file:
    `eda_credit.ipynb`

-----

\<a href="[https://docs.google.com/spreadsheets/d/1hw0Hc1at1As9ak680XT4Z10BMpS-HcAxHmTBEltydpY/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1hw0Hc1at1As9ak680XT4Z10BMpS-HcAxHmTBEltydpY/edit?usp=sharing)" target="\_blank"\>
  📊 View Dashboard
\</a\>
