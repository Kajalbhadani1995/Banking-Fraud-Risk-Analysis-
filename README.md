# Banking-Fraud-Risk-Analysis | Python + MySQL + Power BI

Fraud is rare in banking data, but each case is costly, and a fraud team cannot review every transaction. This project analyses about 60,000 transactions (customers, accounts, transactions and fraud alerts) to find when, where, through which channel, and in which account segments fraud is concentrated, so monitoring can be focused on the highest-risk areas.
Note: The dataset is synthetic. This project shows the analysis method, not real-world findings.

### Business Questions
The project answers eight questions about how big fraud is, and when, where and in which segments it happens.
1. How big is the fraud problem in volume and value?
2. At what time of day does fraud happen?
3. Which channel is riskiest per transaction?
4. Which fraud types are most common?
5. Which months had the highest fraud rate?
6. Is there a weekday pattern in the high-risk months?
7. Where did fraud transactions occur?
8. Are newer or older accounts more exposed?

### End-to-End Banking Fraud Detection Analysis Using SQL, Python, and Power BI

* I created a database and 4 customers, accounts, transactions, fraud_alerts and Imported the datadet in MySQL
* Connected that database to python using SQLAlcgemy

     #### Data Cleaning & Transformation 

     * Handled the Null Values in each column
     * converted date column from object dtype to Datetime dtype.
     * Removed duplicate values.
     * Converted Inconsistent formating of values.
     * Checked outliers.
     * Merged all 4 dataset and make it one and named it df_merged.
     * created column transaction_weekday, transaction_month_year, acnt_open_days_category.
     * created logical column using def function in pandas.

     
     #### Data Analysis & visualisation
  
     * Non-Fraud Transaction VS Fraud Transaction
          * Pie Chart
     * Fraud Count by hour, colored by time category 
          * Bar chart
     * Top 8 Highest Risk Monthly by Fraud Rate
          * Line chart
     * Weekday-wise Fraud for the Top 8 Highest-Risk Months
          * Subplot Bar chart
     * Avg Count Rate of Channel
          * Bar chart
     * Fraud Rate by Tenure
          * Pie chart
     * Top 15 Fraud Location by case count
          * Treemap Chart
     * Comman Fraud Type
          * Bar chart

* After cleaning and analysing went to Power BI and created Dashboard.

### Dashboard | Power BI 

![image alt]([https://github.com/Kajalbhadani1995/Banking-Fraud-RiskAnalysis-/blob/main/Banking_fraud_risk_analysis.pngior%20analysis.jpg](https://github.com/Kajalbhadani1995/Banking-Fraud-Risk-Analysis-/blob/main/Banking_fraud_risk_analysis.png)) 

 
   
### Key Findings

Fraud is small in count but large in value, and it happens only at night.
1. Small in count, large in value. There are 720 fraud cases, which is 1.20% of transactions. They add up to about INR 9.34 crore, roughly 46% of the total transaction value. The average fraud transaction is about INR 1.3 lakh, against about INR 1,850 for a normal one.
2. Fraud happens only at night. All fraud falls between 11 PM and 3:59 AM. The peak hour is 12 AM (155 cases), followed by 3 AM (151).
3. Net Banking is the riskiest channel. Its fraud rate is 2.23%, followed by UPI (1.56%) and Mobile App (1.30%). POS is the lowest at 0.47%. UPI has the most fraud cases, but Net Banking is riskier per transaction.
4. Fraud types are evenly spread. Each of the six types has 105 to 127 cases. No single type dominates.
5. Monthly differences are small. October 2024 has the highest rate (1.62%). The top 8 months range from 1.35% to 1.62%, against 1.20% overall. There is no strong monthly spike.
6. No consistent weekday pattern. No weekday is riskiest across the top 8 months. Each weekday has very few cases, so this result is indicative only.
7. Fraud is spread across locations. Surat (50), Bhopal (47) and Nagpur (45) lead, but all 15 locations have between 31 and 50 cases.
8. Account tenure shows a small gap. Medium-tenure accounts have the highest fraud rate (1.27%), then Old (1.20%) and New (1.08%).
   
### Recommendations

The bank should focus its checks on night-time transactions, starting with Net Banking and UPI.
1. Add step-up verification for night-time transactions (11 PM to 4 AM), starting with Net Banking and UPI. This is where the strongest signals are.
2. Focus monitoring resources on the night window, especially around 12 AM and 3 AM, instead of reviewing all hours equally.
3. Set amount-based alerts. Fraud transactions are far larger than normal ones, so unusually high amounts should trigger a review.
4. Use broad controls across all fraud types. No single type dominates, so a fix for only one type will miss most cases.
5. Compare segments by rate, not count. Channel, month and tenure rankings change when volume is taken into account.
6. Treat weekday, month, location and tenure as secondary signals. Their differences are small, so they should not drive rules on their own.

### Tools

The project uses MySQL for storage, Python for analysis and Power BI for the dashboard.
* MySQL: storage for four related tables (customers, accounts, transactions, fraud_alerts)
* Python (pandas, matplotlib, SQLAlchemy): cleaning, feature engineering and exploratory analysis
* Power BI (DAX): 2-page dashboard with KPI cards and measures such as Fraud Rate % (fraud cases divided by total transactions)

### 🔗 Links and Contacts

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/me?trk=p_mwlite_feed-secondary_nav)
[![Github](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Kajalbhadani1995)
