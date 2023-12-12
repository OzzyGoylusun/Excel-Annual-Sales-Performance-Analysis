# Excel-Annual-Sales-Performance-Deep-Dive

## Table of Contents

- [Data Analysis](#data_analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)


### Excel Data Analysis Overview
---
Coming into existence in the shape of a dashboard in Excel, this data analysis work particularly sheds light on an annual sales performance of a global supplier of office and stationary products for the time period 2011-2014 as per the dataset at hand.

It also highlights in what type of a trend in profits (i.e., in the sense of uptrend/growth, sideways or downtrend/decline) the stationery retailer experiences, compared to previous three years, while running its day-to-day operations.

Based on a number of findings, the Excel dashboard also draws attention to which markets and countries stand out most, which customer segments contributes most to the bottom line and proposes a number of actions accordingly. 

### Data Sources

Order Data: Alongside with two others, the primary dataset used for this analysis is the "order_dataset.csv" file, containing detailed information about orders, their categories and impacts in dollar value.

### Tools

- Microsoft Excel - Data Analysis
  - [Download Here](https://www.microsoft.com/en-us/microsoft-365/excel)

### Data Preparation

In the data preparation phase, I performed the following tasks:

1. Data loading and inspection
2. Data migration
3. Handling missing values
4. Data cleaning
5. Data manipulation, including but not limited to:
- Divide & conquer on date/time data
- Concatenation
- Conversion of data types
   
### Exploratory Data Analysis (EDA)

In an attempt to extract meaningful insights, EDA involved exploring the order data to answer these key questions:

- In which year did the retailer experience the highest figures in profit?
- Which month of the most profitable year did the retail obtain the maximum profit?
- From which country has the retailer received the most orders?
- Which product category in year 2012 resulted in the highest shipping cost?
- Which customer segment in year 2013 received the highest discount rates on average?

Based on resulting answers from these initial lines of query, EDA went on to generate more actionable findings:

### Data_Analysis

While migrating data from *order_location.csv* into our main order dataset, I appreciated the value that the joint use of **INDEX and MATCH** functions have brought to the table:

In the following instance, the INDEX function takes an absolute reference array as its first parameter while the MATCH function helps returning on which row the lookup value is located in our lookup array and also on which column (i.e., in this case, it is 2).

Going beyond **VLOOKUP** and **HLOOKUP**, such use of these functions can more dynamically traverse through any intended dataset, both vertically and horizontally

```excel
=INDEX(order_location!$A$1:$E$51291; MATCH('1_manipulated_data_sheet'!A2; order_location!$A$1:$A$51291;0); 2)
```
<img width="576" alt="Screen Shot 2023-12-10 at 16 12 20" src="https://github.com/OzzyGoylusun/Excel-Annual-Sales-Performance-Deep-Dive/assets/152992554/2813f228-03bf-4c31-83d4-c19ac491d21b">


### Findings

For the period 2011-2014, the analysis results are predominantly summarised as follows:

1. The retailer has been in a parabolic uptrend in terms of experiencing a **45% growth in profits** achieved in 2014 compared to last year.
2. There has been a continuous downtrend with piling losses in the regions of *Africa* and *EMEA* (i.e., Europe, Middle East and Asia), whereas total profits made in the regions of **LA (i.e., Latin America) and US** overall continues to aggressively grow.
3. Both in the **LA and US** markets in 2014, the retailer received the highest number of orders from the **Consumer** segment.
4. While **the United States** has brought in nearly $1.8 billion in total profits as number 1, also along with the highest order count ~ nearly 10000 orders, the country **Barbados** has come out on top by contributing to the bottom-line with a whopping $3.24 million in average profits per order.


### Recommendations

Based on the analysis, I recommend the following actions:

- Consider

### Limitations: 

The following records needed to be removed from the RFM analysis in order to ensure the utmost accuracy of my conclusions:

- Cancelled invoices
- Missing/corrupted customerIDs
- Prices lower than $0
- Records associated with manuals and postage fees


### References:

