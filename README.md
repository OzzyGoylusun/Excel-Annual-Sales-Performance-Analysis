# Annual Sales Performance Review and Dashboard

## Table of Contents

- [Data Analysis](#data-analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)


### Excel Data Analysis Overview
---
This Excel data analysis work sheds light on an annual sales performance of a global supplier of office and stationary products **for the time period 2011-2014 as per the dataset at hand.** 

<p align="center">
  <img src="https://github.com/OzzyGoylusun/Excel.-Sales-Performance-Review-and-Dashboard/blob/main/Visuals/Main%20Dashboard%20Figures.png" alt="Main Dashboard Figures" width="1200">
</p>

It also highlights in what type of a trend in profits (i.e., growth, sideways or decline) the stationery retailer experiences, compared to previous three years.

Based on a number of findings, the Excel dashboard draws attention to which markets and countries stand out most abd which customer segments contributes most to the bottom line to assist the retailer with handing over a roadmap as to increase their profit margins in 2015 and onwards.

<img width="886" alt="Screen Shot 2023-12-12 at 15 42 08" src="https://github.com/OzzyGoylusun/Excel-Sales-Performance-Review-with-Descriptive-Stats/assets/152992554/dd4582e3-a1ce-47fe-9857-60aa307fd8e3">


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
- Dividing & conquering on date/time data
- Concatenation
- Conversion of various other data types
   
### Exploratory Data Analysis (EDA)

EDA first involved exploring the order data to answer these key questions in an attempt to start building an actionable roadmap for upcoming years:

- In which year did the retailer experience the highest figures in profit?
- Which month of the most profitable year did the retail obtain the maximum profit?
- From which country has the retailer received the most orders?
- Which product category in year 2012 resulted in the highest shipping cost?
- Which customer segment in year 2013 received the highest discount rates on average?

Based on resulting answers from these initial lines of query, EDA went on to generate deeper findings mapped out on a comprehensive Excel dashboard.

### Data Analysis

While migrating data from *order_location.csv* into our main order dataset, I appreciated the value that the joint use of **INDEX and MATCH** functions have brought to the table:

In the following instance, the INDEX function takes an absolute reference array as its first parameter while the MATCH function helps returning on which row the lookup value is located in our lookup array and also on which column (i.e., in this case, it is 2).

Going beyond **VLOOKUP** and **HLOOKUP**, such use of these functions can more dynamically traverse through any intended dataset, both vertically and horizontally:

```excel
=INDEX(order_location!$A$1:$E$51291; MATCH('1_manipulated_data_sheet'!A2; order_location!$A$1:$A$51291;0); 2)
```
<img width="576" alt="Screen Shot 2023-12-10 at 16 12 20" src="https://github.com/OzzyGoylusun/Excel-Annual-Sales-Performance-Deep-Dive/assets/152992554/2813f228-03bf-4c31-83d4-c19ac491d21b">


### Findings

For the period 2011-2014, the primary analysis results are summarised as follows:

1. The retailer has experienced a parabolic uptrend with **a 45% growth in profits** achieved in 2014 compared to last year.
2. There has been a continuous downtrend with piling losses in the regions of *Africa* and *EMEA* (i.e., Europe, Middle East and Asia), whereas total profits made in the regions of **LA (i.e., Latin America) and US** thus far continues to aggressively grow.
3. Both in the **LA and US** markets, the retailer received the highest number of orders from the **Consumer** segment in 2014.
4. While **the United States** has brought in nearly $1.8 billion in total profits as the top premium market, also having the highest order count w/ ~10000 orders, the country **Barbados** has come out on top by contributing to the bottom-line most in terms of average profits made per order processed, with a whopping **$3.24 million**.


### Recommendations

Based on this analysis, I recommend the following actions:

- Consider lifting up the total order count in stronghold regions, such as **LA and US** since it was observed that the uptrend in # of orders placed has gradually slowed down despite the parabolic growth in profits.
- Indefinitely pause operations on losing markets such as **Africa** and **EMEA** to curtail cost.
- Distinguish well-performing countries from others in the **Latin America** region. For instance,
  - Concentrate more marketing efforts on some LA countries, such as **Mexico and Cuba**.
  - Pause operations on other LA countries, such as **Panama and Argentina**.
- Undertake further product-market fit research on niche countries that have produced high average profits per order, such as **Barbados and Trinidad-Tobago**.


### References:

1. [YouTube Tutorial: Advanced Index-Match Functions](https://www.youtube.com/watch?v=-4yCXpv-drg)
2. [Microsoft Excel: Create a Map Chart in Excel](https://support.microsoft.com/en-au/office/create-a-map-chart-in-excel-f2cfed55-d622-42cd-8ec9-ec8a358b593b)
