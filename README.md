🏦 Banking Risk Analytics Dashboard – Power BI 
📘 Project Overview

This project aims to develop a Banking Risk Analytics Dashboard using Power BI, helping financial institutions analyze, visualize, and minimize lending risks through data-driven insights.

The dashboard evaluates clients’ financial behavior and engagement patterns to help decide whether a loan should be approved or not — based on multiple factors like deposits, loan history, income, and fees.

🎯 Problem Statement

Banks and financial institutions face high risks while lending money. This project focuses on:

Understanding risk analytics in the banking sector.

Using data visualization and DAX functions to minimize the risk of loan defaults.

Providing actionable insights to help in loan approval decisions.

💡 Solution Approach

Using Power BI, I developed an interactive dashboard that helps decision-makers:

Analyze loan and deposit trends.

Identify client engagement duration.

Evaluate processing fees, income bands, and account balances.

Generate KPI summaries to understand customer and business performance at a glance.

📂 About the Dataset

The dataset contains multiple interlinked tables through primary and foreign keys:

Banking Relationship

Client–Banking

Gender

Investment Advisor

Period

Each table provides different aspects of client-bank interactions.

🧹 Data Cleaning & Transformation
Transformation	Description
Engagement Timeframe	Created to calculate each client’s active duration with the bank.
Engagement Days	Calculated using DAX DATEDIFF between joining date and today’s date.
Income Band	Categorized income: < 100000 = Low, < 300000 = Mid.
Processing Fees	Derived as 5% of the total fee structure for high-fee clients.
🧮 DAX Calculations & Measures
📊 Basic Aggregations

Bank Deposit:
SUM('Clients - Banking'[Bank Deposits])

Total Clients:
DISTINCTCOUNT('Clients - Banking'[Client ID])

Total Loan:
[Bank Loan] + [Business Lending] + [Credit Cards Balance]

Total Fees:
SUMX('Clients - Banking', [Total Loan] * 'Clients - Banking'[Processing Fees])

⚙️ Key DAX Functions Used
Function	Description
SUM()	Adds numeric values across a column.
SUMX()	Evaluates and sums an expression for each row in a table.
DISTINCTCOUNT()	Counts unique client IDs.
SWITCH()	Used for logical expressions in risk categorization.
DATEDIFF()	Calculates the difference between two date fields.

📈 Key Performance Indicators (KPIs)
KPI	Description
Total Clients	Count of unique clients associated with banks.
Total Loan	Total of loans, business lending, and credit card balances.
Total Deposit	Combined deposits from savings, checking, and foreign accounts.
Total Fees	Sum of processing and service fees applied per client.
Engagement Length	Total duration (days) clients stayed active in the bank.
📊 Dashboard Views

🏠 Home Page – Overview of client summary and navigation.

💳 Loan Analysis – Visualizes total loan distribution by gender, relationship, and type.

💰 Deposit Analysis – Displays deposits across savings, foreign currency, and checking accounts.

📋 Summary Dashboard – A combined view showing overall financial metrics and KPIs.

🔍 Insights & Results

Identified which banks have higher client bases (e.g., private vs public).

Determined which nationalities carry the highest loan balances.

Showed client income trends and engagement durations for better targeting.

Helped visualize processing fees and risk categories across clients.

🚀 Tools & Technologies Used

Power BI – Data visualization and dashboard creation

SQL – Data querying and relationship management

Python (Pandas) – Initial data cleaning and transformation

Excel – Preliminary dataset inspection

🧭 Future Scope

Integration with real-time banking data APIs for live updates.

Building a machine learning model to predict loan repayment probability.

Extending the dashboard for customer segmentation and risk scoring.

📑 Conclusion

The Banking Risk Analytics Dashboard provides a powerful visualization tool for banks to:

Monitor financial KPIs,

Minimize credit risk,

Improve decision-making for loans and deposits,

Strategically plan client engagement and retention.

This project demonstrates the integration of data analytics, DAX modeling, and business intelligence to solve real-world banking problems.

👩‍💻 Developed By: Prerana Kamble

📍 Data Analyst | Power BI | Python | SQL | Excel
