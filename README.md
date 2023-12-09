# Excel-Annual-Sales-Performance-Deep-Dive

## Table of Contents

- [Data Analysis](#data_analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)


### Excel Data Analysis Overview
---
Coming into existence in the shape of a dashboard in Excel, this data analysis work particularly sheds light on an annual sales performance of a global supplier of office and stationary products. 

It also highlights in what type of a trend in profits (i.e., in the sense of uptrend/growth, sideways or downtrend/decline) the stationery retailer experiences, compared to previous three years, while running its day-to-day operations.

Based on a number of findings, the Excel dashboard also draws attention to which markets and countries stand out most, which customer segments contributes most to the bottom line and proposes a number of actions accordingly. 


### Data Sources

Order Data: Alongside with two others, the primary dataset used for this analysis is the "order_dataset.csv" file, containing detailed information about orders, their categories and impacts in dollar value.

### Tools

- PostgreSQL Server - Data Analysis
  - [Download Here](https://www.postgresql.org/download/)
  

### Data Cleaning/Preparation

In the data preparation phase, I performed the following tasks:

1. Data loading and inspection
2. Handling missing values
3. Data cleaning
   
### Exploratory Data Analysis (EDA)

EDA primarily involved exploring the complex transaction data to answer these key questions:

- What percentage of all customers have achieved an ultimate RFM score of 100 or 125 out of 125 as its **Champions**?
  
  - For your information, customers receive a score from 1 to 5 from each category based on how recently, frequently and monetarily they have transacted with the retailer, benchmarked against other customers. For instance:
 
      |Recency|Frequency|Monetary|
      |--------|--------|--------|
      |5*|5*|5|
      | | |=125|

- How many potentially loyal customers can the retailer identify to upgrade them to Champions?
- How many customers is the retailer at the risk of losing due to lack of interaction or some other reasons? 


### Data_Analysis

Compared to my *Frequency* and *Monetary* tables, I found the coding with the **Recency** table a bit more complex due to the natural need to also have to calculate the customers' last booking date beforehand:

```sql
```

### Findings

The analysis results are predominantly summarised as follows:

1. Approx. 15% of all customers have achieved a total Ultimate RFM Score of 100 or 125, considered **Champions**.
2. 96 customers out of 4335 have achieved 4 points on Recency, 3 points on Frequency and 4 points on Monetary, considered **Potential Loyalists**.
3. There are nearly 200 valuable customers who scored less than 3 points on Recency, but scored 4 or 5 points on Frequency and Monetary, considered **At Risk Customers**.

Please note that there were no repetititons/crossovers of customers amongst each customer segment analysed.

### Recommendations

Based on the analysis, I recommend the following actions:

- Consider further rewarding the **Champions** as they could very well become early adopters for new products and also assist with the promotion of the retailer's brand.
- Offer membership/loyalty  programs to the **Potential Loyalists** in an attempt to upgrade them to the **Champions** segment.
- Put in more effort to reconnect with the **At Risk Customers** via personalised communications which include coupons and/or other incentives of some sort.

### Limitations: 

The following records needed to be removed from the RFM analysis in order to ensure the utmost accuracy of my conclusions:

- Cancelled invoices
- Missing/corrupted customerIDs
- Prices lower than $0
- Records associated with manuals and postage fees


### References:
