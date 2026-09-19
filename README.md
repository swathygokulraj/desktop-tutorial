🏦 Bank Customer & Transaction Analysis
📌 Project Overview
The Bank Customer & Transaction Analysis project is a data analytics
project designed to analyze customer information, banking transactions,
loan details, EMI payments, credit scores. The project uses Excel and
Power BI to clean, transform, analyze, and visualize the data.
Interactive dashboards are created using KPIs, charts, graphs, and
slicers to identify important trends and patterns.
---
🎯 Objectives
To analyze bank customer information and transaction data.
To identify important trends and patterns in banking transactions.
To analyze loan and EMI payment details.
To evaluate customer credit scores and financial behavior.
To create interactive dashboards using Excel and Power BI.
To provide meaningful insights for better financial decision-making.
---
📂 Dataset
The dataset contains approximately 1,000 records.
Columns
`transaction_id`
`customer_id`
`transaction_date`
`transaction_time`
`account_type`
`transaction_type`
`transaction_amount`
`transaction_direction`
`account_balance`
`merchant_category`
`state`
`credit_score`
`has_loan`
`loan_type`
`emi_amount`
`transaction_status`
`channel`
`kyc_status`
`transaction_hour`
---
🛠️ Tools & Technologies Used
Microsoft Excel
Power Query
Power BI
DAX
Data Visualization
Power BI Navigation
Data cleaning, formatting, basic analysis, and data preparation
Data transformation, cleaning, filtering, and handling
missing/duplicate values
Data visualization, dashboard creation, interactive reports, and KPI
analysis
Creating calculated measures, KPIs, and analytical calculations
Charts, graphs, cards, maps, slicers, and interactive dashboards
Page navigation, buttons, bookmarks, and interactive dashboard
experience
---
📊 DAX Measures Formula & KPI's (12)
🏠 Overview
``` dax
LoanCustomers =
CALCULATE(
    DISTINCTCOUNT('Sheet1'[customer_id]),
    'Sheet1'[has_loan] = 1
)

AverageTransactionAmount =
AVERAGE('Sheet1'[transaction_amount])

Total Customers =
DISTINCTCOUNT('Sheet1'[customer_id])

Total Transaction Amount =
SUM('Sheet1'[transaction_amount])

Total Transactions =
COUNT('Sheet1'[transaction_id])
```
👤 Customers
``` dax
Total Customers =
DISTINCTCOUNT('Sheet1'[customer_id])

LoanCustomers =
CALCULATE(
    DISTINCTCOUNT('Sheet1'[customer_id]),
    'Sheet1'[has_loan] = 1
)

KYCVerifiedCustomers =
CALCULATE(
    COUNTROWS('Sheet1'),
    'Sheet1'[kyc_status] = "Verified"
)

Average credit score =
AVERAGE('Sheet1'[credit_score])
```
💳 Transactions
``` dax
SuccessfulTransactions =
CALCULATE(
    DISTINCTCOUNT('Sheet1'[transaction_id]),
    'Sheet1'[transaction_status] = "Successful"
)

FailedTransactions =
CALCULATE(
    DISTINCTCOUNT('Sheet1'[transaction_id]),
    'Sheet1'[transaction_status] = "failed"
)
```
Total transaction
Total transaction amount
Average transaction amount
⚠️ Loan & EMI
``` dax
Loan Customer% =
DIVIDE([Loan Customers], [Total Customers], 0)

Total EMI Amount =
SUM('Sheet1'[emi_amount])

Average EMI =
AVERAGE('Sheet1'[emi_amount])
```
Loan customers
---
📑 Page Wise Visuals & Slicers
🏠 Overview
Slicers
Account_type
State
Transaction_date
Visuals
Column & line chart --- Total transaction by transaction_type  
Transaction activity by type and hour to identify peak transaction
times.
Donut chart --- Total transaction by transaction_direction  
Compares credit and debit transactions to understand transaction flow.
Line chart --- Total transaction_amount by day  
Transaction patterns and changes across different days.
Bar chart --- Total transaction by channel  
To compare transaction activity across different banking channels and
directions.
---
👤 Customer Analysis
Slicers
Has_loan
Account_type
Kyc_status
State
Visuals
Column charts --- Total_customer by kyc_status  
To understand the number of customers based on their KYC verification
status.
Donut charts --- Total_customer by account_type  
To compare the number of customers using different account types.
Filled map --- Total_customer by state by state  
Geographical distribution of customers across different states.
---
💳 Transaction Analysis
Slicers
State
Transaction_type
Channel
Transaction_date
Transaction_status
Visuals
Waterfall charts --- Total_transaction_amount by transaction_type  
Transaction types contribute more/less to the total amount.
Ribbon charts --- Total_transaction_amount by day and channels  
Ranking of banking channels changes.
Scattercharts --- Sum_of_credit_score, Sum_of_transaction_amount,
transaction_type  
Customers with higher credit scores tend to make larger transactions.
---
⚠️ Loan & EMI Analysis
Slicers
Loan_type
Account_type
Kyc_status
Visuals
Pie charts --- Count_of_customer_id by loan_type  
Customers across different loan type.
Column charts --- Total_EMI amount by loan_type  
Loan type contributes the highest EMI amount.
Scatter charts --- Sum_of credit_score, Sum of EMI amount by
loan_type  
Customers with different credit score have different EMI amounts.
---
🔑 Key Features
Interactive Dashboard with multiple analysis pages
KPI Cards for total customers, transactions, transaction amount, and
EMI
Transaction Trend Analysis by type, day, and hour
Customer Analysis by state, account type, and KYC status
Loan Analysis by loan type, customer count, and EMI amount
Credit Score Analysis across transaction and loan types
Interactive Slicers for easy filtering
Page Navigation Buttons for smooth movement between dashboard pages
Geographical Analysis using state-wise customer/transaction data
---
author
Swathi
