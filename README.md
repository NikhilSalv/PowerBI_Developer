# Revenue Analysis Report Documentation

## Abstract

This report presents critical business insights derived from a comprehensive analysis of revenue data spanning over three Quarters of years between 2022 and 2023. The study delves into revenue trends, patterns, and notable fluctuations within this period, providing a deep understanding of financial performance and its implications for the organization.

## Introduction

The dataset of “Revenue Information Case study” contains records of individual invoices, its starting date, closing date, category, revenue, etc. The data catalogue is as below:

| Field Name                | Description                                            |
|---------------------------|--------------------------------------------------------|
| FBU                       | Field representing a unique identifier for each record |
| createdate                | Date when the data entry was created                   |
| invoicedate               | Date of the invoice                                    |
| BillingStatus             | Billing status (e.g., 0 for not billed)               |
| Client number             | Client identification number                           |
| Invoicecategory           | Category of the invoice (e.g., STORAGE)               |
| Revenue                   | Revenue generated for the specified services          |
| Quantity                  | Quantity of items associated with the revenue         |
| Price                     | Price per item                                         |
| BASEPrice                 | Base price per item (not used in analysis)             |
| ServiceCode               | Code representing the type of service                  |
| Description               | Description of the service                             |
| datefrom                  | Start date of the service period                       |
| dateto                    | End date of the service period                         |
| Monthly Value             | Monthly revenue value                                  |
| Nr of month (months between cell Q&R) | Number of months within the date range        |

Systematic steps are taken to identify objectives, KPIs, and build insightful dashboard using PowerQuery and PowerBI.

## Key Performance Indicators (KPIs)

1. Total revenue amount in each Quarter.
2. Percentage of revenue generated by top 10 clients in each quarter.
3. Total Price in each quarter.
4. Total number of unique clients in each quarter.
5. Top 10 client names.
6. Percentage of total revenue contribute by top 10 clients in each quarter.
7. Total revenue contributed by each category.
8. Patterns throughout time for every category with regard to generating revenue.
9. Patterns throughout time for every category with regard to quantity.
10. Background calculations for total difference between Actual Price and calculated.

## Data Enhancement

Data enhancement is necessary for several reasons, and it plays a crucial role in improving the quality and usefulness of data for various purposes. Data enhancement helps fill in missing or incomplete information in your dataset, making it more accurate and complete. This is particularly important for data-driven decision-making, as accurate data leads to better insights.

1. Append Data:
   - The original dataset has two tabs, “Storage”, and “Services”. These two tabs are appended together to create a master dataset, named “Transformed Data”.
   - Several extreme columns are blank, and those are ignored.

2. New Columns based on Invoice Date:
   - The revenue of each record is recognized by “Invoice Date” column. For data enhancement, four new columns are further created based on this column, which are “Month name”, “Month”, “Quarter of the Year” and “Year”.
   - The data and info graphs are majorly divided by Quarter of the year. There are 3 quarters in this data. Q3 and Q4 are the last two quarters of year 2022, and Q1 is the first quarter of 2023.

3. Background calculations columns:
   - As the actual price is different in the case of annual and quarter invoices due to background calculations, but the quantity is always correct. Hence, new column named “Calculated Price” has been added by dividing revenue by quantity. By taking the absolute difference between calculated price and price in the data, another column named “Background calculations” is created. This column will provide insights on the total background calculations.

## KPI’s with Infographics

### Slicers

<img width="851" alt="slicers" src="https://github.com/NikhilSalv/PowerBI_Developer/assets/74225565/1c55e3ff-90ce-45e5-9727-b314371d1dca">


As shown in the picture, the slicers provide options to choose the FBU, quarter of the years, Year, category of invoice and Client number.

### KPIs

<img width="854" alt="Main KPIs" src="https://github.com/NikhilSalv/PowerBI_Developer/assets/74225565/095de3b4-904f-480b-bef9-8110e7a4f55d">

As shown in the above figure, the important KPIs in this project are Total Revenue, total price, and revenue contribution in percentage by top 10 clients of the company. On the top right corner, the top 3 clients number of those clients who contributed to most of the revenue, are displayed. The background calculation is the total absolute difference in the actual price and calculated price.

### Info graphs


<img width="874" alt="infographs" src="https://github.com/NikhilSalv/PowerBI_Developer/assets/74225565/7a339f11-e23e-4606-9d78-6d7d3105d475">

The above figure shows the main info graphs as stated below:

- Revenue contribution by clients: This represent the revenue contribution by top 10 client with pie chart.
- Sum of Revenue by Quarter of the Year: This pie chart represents total revenue contribution in each quarter of the years.
- Inventory volume trend: This info graph provides insights of quantity / Volume of inventory over the period of time.
- Revenue Distribution over time and categorized by Invoice category: With this info graph, pattern in the revenue contribution by each category of invoice over the period of time is analysed.
- Tree chart of revenue contribution by invoice category: This info graphs provides visual representation of total revenue contribution by each category of service.

## Observations

Quarter | Total revenue | Revenue % by top 10 | Unique No. of clients | Top 3 clients | Top service | Total revenue by top service | Total Price
------- | ------------- | -------------------- | --------------------- | ------------- | ----------- | --------------------------- | -----------
Q3 (2022) | 33.12 M | 4.35% | 1436 | ROBOI lxL, ROPOK_2342342345, ROPOK_SHE0234 | Services | 20.88 M | 998.59 k
Q4 (2022) | 34.38 M | 3.64% | 1845 | ROBOI lxL, ROPOK_2342342345, ROPOK_SHE0234 | Services | 16.55 M | 680.64 k
Q1 (2023) | 27.65 M | 3.77% | 1726 | ROBOI lxL, ROPOK_2342342345, ROxOIL-00023428 | Services | 12.38 M | 555.28 k

### Quarter 3 (2022)

The total revenue of quarter 3 is $33.12 M, which is the second-highest revenue in the 3 quarters. It is significant to note that in this quarter, the least number of unique clients have contributed as compared to those of other 2 quarters. The number of unique clients is 1436 only. The reason behind this is, clients ROPOK_2342342345, ROPOK_SHE0234 have set a record in this quarter by contributing $4.03 million each! A company’s revenue is more secured when it has a loyal customer base. Retaining existing customers costs less than acquiring new ones. Which means the CAC (Customer Acquisition Cost) remains low. Happy customers are more likely to purchase additional products and services, which can increase revenue grow opportunities. The top 3 clients by the revenue contribution are ROBOI lxL, ROPOK_2342342345, ROPOK_SHE0234. Overall 4.35 % revenue is
