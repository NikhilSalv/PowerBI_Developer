# Data Catalogue: Revenue Information Data 2022-23

This data catalogue describes the Revenue Information for the years 2022-23.

## Original Data Fields

| Field Name        | Description                                                 |
|-------------------|-------------------------------------------------------------|
| FBU               | Field representing a unique identifier for each record      |
| createdate        | Date when the data entry was created                        |
| invoicedate       | Date of the invoice                                         |
| BillingStatus     | Billing status (e.g., 0 for not billed)                    |
| Client number     | Client identification number                                |
| Invoicecategory   | Category of the invoice (e.g., STORAGE)                    |
| Revenue           | Revenue generated for the specified services                |
| Quantity          | Quantity of items associated with the revenue               |
| Price             | Price per item                                              |
| BASEPrice         | Base price per item (not used in analysis)                  |
| ServiceCode       | Code representing the type of service                        |
| Description       | Description of the service                                  |
| datefrom          | Start date of the service period                            |
| dateto            | End date of the service period                              |
| Monthly Value     | Monthly revenue value                                       |
| Nr of month       | Number of months within the date range                      |

## Data Enhancement Fields

To improve data quality, various steps are taken for data enhancement using Power Query. New columns have been added to the dataset:

| Field Name             | Description                                                       |
|------------------------|-------------------------------------------------------------------|
| Month Name             | Field representing the month of the invoice date                  |
| Year                   | Field representing the year of the invoice date                   |
| Quarter of the year    | Quarter of the year in which the invoice is dated                |
| Calculated price       | The calculated price after dividing revenue by quantity          |
| Background calculations| Absolute difference between calculated price and price           |

These additional columns provide further insights and analysis capabilities to the dataset.


