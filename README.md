# Customer Financial Portfolio & Risk Analytics Dashboard

## 📊 Project Overview

The **Customer Financial Portfolio & Risk Analytics Dashboard** is an interactive Power BI dashboard designed to analyze customer financial data, loan performance, investments, risk profiles, income, and cash flow.

The dashboard helps businesses understand customer financial behavior and make **data-driven decisions** related to financial performance, lending, risk management, and customer portfolio analysis.

---

## 🎯 Objectives

* Analyze customer account balances and income levels.
* Monitor deposits, withdrawals, and net liquidity flow.
* Analyze loan applications, approvals, and exposure.
* Understand customer risk tolerance and portfolio distribution.
* Compare financial performance across employment statuses.
* Analyze loan purposes and approval trends.
* Support better financial and business decision-making through interactive dashboards.

---

## 🛠️ Tools & Technologies

* **Power BI** – Dashboard development and visualization
* **Power Query** – Data cleaning and transformation
* **DAX** – Measures and financial calculations
* **Microsoft Excel** – Data source and preprocessing

---

## 📌 Key KPIs

The dashboard focuses on important financial and risk indicators such as:

* Total Deposits
* Total Withdrawals
* Net Liquidity Inflow
* Average Account Balance
* Average Income
* Total Loan Exposure
* Loan Approval Rate
* Loan Amount
* Interest Rate
* Investment Value
* Risk Tolerance
* Transaction Volume

---

## 📈 Dashboard Features

### 1. Financial Performance Analysis

Provides an overview of customer financial activity, including:

* Deposits
* Withdrawals
* Net liquidity flow
* Account balances
* Income levels
* Transaction activity

### 2. Risk Analytics

Analyzes the distribution of customers based on risk tolerance:

* Low Risk
* Medium Risk
* High Risk

This helps identify the overall risk profile of the customer portfolio.

### 3. Loan Performance Analysis

Provides insights into:

* Loan approval status
* Loan purposes
* Loan exposure
* Average loan amount
* Interest rates
* Default risk
* Loan terms

### 4. Employment & Financial Analysis

Compares financial performance across different employment categories such as:

* Employed
* Self-Employed
* Other employment categories

Key metrics include average income, account balance, deposits, withdrawals, loan exposure, and approval rate.

### 5. Executive Summary

The dashboard provides a consolidated view of major financial metrics to help stakeholders quickly understand portfolio performance and identify important trends.

---

## 📊 Key Visualizations

The dashboard includes:

* KPI Cards
* Line & Stacked Column Charts
* Donut Charts
* Clustered Bar/Column Charts
* Matrix Tables
* Slicers
* Interactive Filters

---

## 🔍 Example Business Questions

The dashboard can help answer questions such as:

* What is the total customer deposit and withdrawal volume?
* What is the current net liquidity inflow?
* Which risk category has the largest customer portfolio?
* Which loan purpose has the highest approval rate?
* How does employment status affect income and account balance?
* Which risk category has higher loan exposure?
* What is the average loan amount across different risk levels?
* How do interest rates vary according to customer risk tolerance?
* Which loan terms are associated with higher default risk?

---

## 💡 Business Insights

The dashboard can be used by financial and business teams to:

* Identify high-risk customer segments.
* Monitor cash flow and liquidity.
* Evaluate loan approval performance.
* Understand customer financial behavior.
* Compare financial performance across customer segments.
* Support lending and risk-management decisions.
* Identify opportunities for improving portfolio performance.

---

## 🗂️ Dashboard Structure

```text
Customer Financial Portfolio & Risk Analytics
│
├── Financial Performance
│   ├── Deposits
│   ├── Withdrawals
│   ├── Net Liquidity Inflow
│   └── Transactions
│
├── Risk Analytics
│   ├── Risk Tolerance
│   ├── Customer Distribution
│   └── Risk-Based Financial Metrics
│
├── Loan Analytics
│   ├── Loan Approval Status
│   ├── Loan Purpose
│   ├── Loan Exposure
│   ├── Interest Rate
│   └── Default Risk
│
└── Customer Financial Analysis
    ├── Employment Status
    ├── Income
    ├── Account Balance
    └── Portfolio Metrics
```

---

## 🧮 Key DAX Measures

The dashboard uses DAX measures to calculate important financial, liquidity, and loan performance metrics.

### Net Liquidity Inflow

```DAX
Net Liquidity Inflow =
SUM('Customer Financial Profiles & P'[Deposits])
-
SUM('Customer Financial Profiles & P'[Withdrawals])
```

Calculates the difference between total deposits and total withdrawals.

### Loan Approval Rate

```DAX
Loan Approval Rate =
DIVIDE(
    COUNTROWS(
        FILTER(
            'Customer Financial Profiles & P',
            'Customer Financial Profiles & P'[Loan Status] = "approved"
        )
    ),
    COUNTROWS('Customer Financial Profiles & P'),
    0
)
```

Measures the percentage of customer loan applications that are approved.

### Approved Credit Volume

```DAX
Approved Credit Volume =
CALCULATE(
    SUM('Customer Financial Profiles & P'[Loan Amount]),
    'Customer Financial Profiles & P'[Loan Status] = "approved"
)
```

Calculates the total loan amount for approved applications.

### Pending Credit Volume

```DAX
Pending Credit Volume =
CALCULATE(
    SUM('Customer Financial Profiles & P'[Loan Amount]),
    'Customer Financial Profiles & P'[Loan Status] = "pending"
)
```

Calculates the total loan amount currently pending approval.

### Average Account Balance

```DAX
Average Account Balance =
AVERAGE('Customer Financial Profiles & P'[Account Balance])
```

Calculates the average customer account balance.

### Average Income

```DAX
Average Income =
AVERAGE('Customer Financial Profiles & P'[Income Level])
```

Calculates the average customer income level.

### Average Loan Amount

```DAX
Average Loan Amount =
AVERAGE('Customer Financial Profiles & P'[Loan Amount])
```

Calculates the average loan amount across customers.

### Average Interest Rate

```DAX
Average Interest Rate =
AVERAGE('Customer Financial Profiles & P'[Interest Rate])
```

Calculates the average interest rate of loans.

### Average Loan Term

```DAX
Average Loan Term =
AVERAGE('Customer Financial Profiles & P'[Loan Term (Months)])
```

Calculates the average loan repayment term in months.

### Domestic Transfer

```DAX
Domestic Transfer =
[Total Transfers] - [Total International Transfers]
```

Calculates domestic transfers by excluding international transfers from total transfers.

### Liquidity Retention Ratio

```DAX
Liquidity Retention Ratio =
DIVIDE(
    [Net Liquidity Inflow],
    [Total Deposit]
)
```

Measures the proportion of deposited funds retained as net liquidity.

### Income Level Tier

```DAX
Income Level Tier =
SWITCH(
    TRUE(),
    'Customer Financial Profiles & P'[Income Level] < 30000, "Low",
    'Customer Financial Profiles & P'[Income Level] < 60000, "Medium",
    'Customer Financial Profiles & P'[Income Level] < 1000000, "High",
    "Very High"
)
```

Segments customers into income-level categories for financial analysis.

---

## 📌 DAX Skills Demonstrated

* `SUM()` – Financial volume calculations
* `AVERAGE()` – Customer and loan performance analysis
* `CALCULATE()` – Context-based financial calculations
* `FILTER()` – Conditional data analysis
* `COUNTROWS()` – Loan and customer counting
* `DIVIDE()` – Ratio and percentage calculations
* `SWITCH()` – Customer income segmentation
* Dynamic DAX Measures – Interactive Power BI analysis
   


## 🎨 Dashboard Design

The dashboard uses a professional and interactive design with:

* Clean financial-themed visuals
* KPI cards for important metrics
* Consistent formatting
* Interactive slicers and filters
* Easy-to-understand charts
* Business-focused visual hierarchy

---

## 🚀 Project Outcome

This project demonstrates the use of **Power BI, Power Query, and DAX** to transform customer financial data into an interactive business intelligence solution.

It provides stakeholders with a centralized view of **financial performance, loan activity, customer risk, investments, and cash flow**, enabling faster and more informed business decisions.

---

## 👩‍💻 Skills Demonstrated

* Power BI Dashboard Development
* Data Visualization
* Data Cleaning & Transformation
* Power Query
* DAX
* KPI Development
* Financial Data Analysis
* Risk Analytics
* Loan Analytics
* Business Intelligence
* Business Analysis
* Data-Driven Decision Making

---
Page 1: 
<img width="1322" height="745" alt="image" src="https://github.com/user-attachments/assets/0650aa37-1abd-4fa3-9e20-6fb871356328" />
Page 2:
<img width="1327" height="747" alt="image" src="https://github.com/user-attachments/assets/242be3fe-8d54-4ee6-a707-be6a5dee046c" />
Page 3:
<img width="1327" height="737" alt="image" src="https://github.com/user-attachments/assets/1e41ce65-4147-454c-95d4-2ad7ef70359c" />
Page 4:
<img width="1325" height="747" alt="image" src="https://github.com/user-attachments/assets/f10868d5-3c31-4c33-be06-d9f59bc95e48" />


## ⭐ Conclusion

The **Customer Financial Portfolio & Risk Analytics Dashboard** converts complex financial data into meaningful and actionable insights. It demonstrates how Power BI can be used to analyze customer portfolios, monitor financial performance, evaluate loan and risk metrics, and support strategic business decisions.
