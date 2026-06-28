\# Business Data Cleaning, Validation \& Excel Reporting



\## Project Overview



This project focuses on cleaning, validating, and transforming raw retail sales order data into a reliable, analysis-ready dataset using Microsoft Excel. The original dataset contained several quality issues including inconsistent text formatting, missing values, duplicate records, invalid discounts, date inconsistencies, and business rule violations. The objective of this project was to improve data quality while preserving the original dataset and creating meaningful summary reports for business decision-making.



\# Business Problem Summary



Retail organizations rely on accurate transactional data for reporting, forecasting, profitability analysis, and operational planning. However, data collected from multiple internal systems often contains inconsistencies and errors that reduce reporting accuracy.



The business required a standardized dataset that:



\- Removes inconsistencies from raw data.

\- Validates records against predefined business rules.

\- Identifies and documents data quality issues.

\- Produces accurate sales and profitability summaries.

\- Supports future dashboard creation and business analytics.



The cleaned dataset enables management to make informed business decisions using reliable and validated information.



\# Project Objectives



The primary objectives of this project were to:



\- Preserve the original raw dataset.

\- Clean and standardize business data.

\- Validate business rules.

\- Create additional calculated business metrics.

\- Identify and document data quality issues.

\- Build management-ready Pivot Table reports.

\- Prepare an analysis-ready dataset suitable for reporting and visualization.



\# Dataset Description



The dataset contains retail order-level transactional information covering customer details, product information, order status, payment details, shipping information, sales, costs, discounts, and profitability.



Major fields include:



| Category | Fields |

|-----------|--------|

| Order Information | Order ID, Order Date, Ship Date |

| Customer Details | Customer Name, Segment |

| Geography | Region, State, City |

| Product Details | Category, Sub Category |

| Sales Information | Quantity, Unit Price, Sales, Cost, Profit, Discount |

| Operational Details | Ship Mode, Payment Status, Order Status |



The dataset was intentionally designed with multiple data quality issues for cleaning and validation.



\# Tools Used



The project was completed entirely using Microsoft Excel.



Techniques and features used include:



\- Excel Formulas

\- TRIM

\- SUBSTITUTE

\- IF

\- IFERROR

\- MONTH

\- YEAR

\- DATEDIF

\- ROUND

\- Conditional Formatting

\- Sort \& Filter

\- Pivot Tables

\- Data Validation

\- Duplicate Identification



\# Data Cleaning Methodology



\## 1. Text Standardization



The following text fields were cleaned and standardized:



\- Customer Name

\- Segment

\- Region

\- State

\- City

\- Category

\- Sub Category

\- Ship Mode

\- Payment Status

\- Order Status



Cleaning activities included:



\- Removing leading spaces

\- Removing trailing spaces

\- Eliminating multiple spaces

\- Correcting inconsistent capitalization

\- Standardizing category names

\- Removing unwanted characters where applicable



\## 2. Date Cleaning \& Validation



The Order Date and Ship Date columns were validated and standardized.



The following checks were performed:



\- Converted dates into a consistent format.

\- Identified missing dates.

\- Flagged invalid dates.

\- Flagged records where Ship Date occurred before Order Date.

\- Calculated Shipping Delay Days.



\## 3. Missing Value Handling



Missing values were handled according to business requirements.



Business logic applied:



| Field | Action Taken |

|--------|--------------|

| Region | Filled with "Unknown" |

| Ship Mode | Filled with "Unknown" |

| Discount | Replaced with 0 only when remaining financial data was valid |



Missing values were documented in the Data Quality Report.



\## 4. Duplicate Handling



The dataset was reviewed for:



\- Exact duplicate records

\- Duplicate Order IDs

\- Conflicting duplicate records



Duplicate handling approach:



\- Exact duplicate rows were removed where appropriate.

\- Conflicting duplicate Order IDs were retained and flagged for manual review.

\- Duplicate statistics were documented in the Data Quality Report.



\## 5. Business Rule Validation



The following business rules were implemented.



| Business Rule | Validation |

|---------------|------------|

| Missing Region | Filled with Unknown |

| Missing Ship Mode | Filled with Unknown |

| Missing Discount | Treated as 0 where applicable |

| Negative Discount | Flagged Invalid |

| Discount above allowed range | Flagged Invalid |

| Cancelled Orders | Excluded from completed sales summary |

| Failed Payments | Excluded from completed sales summary |

| Refunded Orders | Reported separately |

| Ship Date before Order Date | Flagged Invalid |



\# Calculated Columns Created



The cleaned dataset contains the following calculated fields.



| Calculated Column | Description |

|-------------------|-------------|

| cleaned\_discount | Standardized discount value |

| calculated\_sales | Sales recalculated using quantity, unit price and discount |

| calculated\_profit | Profit recalculated using sales and cost |

| profit\_margin | Profit ÷ Sales |

| shipping\_delay\_days | Ship Date − Order Date |

| order\_month | Month extracted from Order Date |

| order\_year | Year extracted from Order Date |

| data\_quality\_flag | Clean / Warning / Invalid indicator |



\# Data Quality Summary



The dataset was validated for multiple quality dimensions including:



\- Missing values

\- Duplicate records

\- Invalid discounts

\- Date inconsistencies

\- Shipping validation

\- Order Status issues

\- Payment Status issues

\- Sales calculation mismatches

\- Profit calculation mismatches



Clean and flagged records were summarized separately within the Data Quality Report.



\# Pivot Reports Created



The project includes management-ready Pivot Table summaries covering:



\- Sales by Region

\- Profit by Region

\- Sales by Category

\- Sales by Sub Category

\- Order Count by Ship Mode

\- Profit Margin by Customer Segment

\- Cancelled / Failed / Refunded Orders by Region

\- Monthly Sales Trend



Sorting and filtering were applied wherever appropriate to improve readability.



\# Key Business Insights



Major observations obtained from the cleaned dataset include:



\- Sales performance differs significantly across regions.

\- Certain product categories contribute disproportionately to profit.

\- Some sub-categories generate high sales but comparatively lower profitability.

\- Customer segments demonstrate different profit margins.

\- Shipping methods influence delivery performance.

\- Cancelled and failed payment orders reduce realized revenue.

\- Monthly sales trends indicate seasonal demand fluctuations.

\- Standardized data significantly improves reporting accuracy.



\# Business Rules Applied



The project strictly followed all business rules provided in the assignment.



Key validations included:



\- Missing Region → Unknown

\- Missing Ship Mode → Unknown

\- Missing Discount → Zero (where applicable)

\- Negative Discounts → Invalid

\- Excessive Discounts → Invalid

\- Cancelled Orders excluded from completed sales summaries

\- Failed Payments excluded from completed sales summaries

\- Refunded Orders analyzed separately

\- Invalid shipping records flagged



\# Assumptions



The following assumptions were applied during data cleaning:



\- Unknown values were assigned where mandatory fields were missing.

\- Missing discounts were replaced with zero only when remaining financial information was valid.

\- Duplicate records with conflicting information were retained for manual review.

\- Shipping Delay was calculated using Ship Date minus Order Date.

\- Profit Margin was calculated using Profit divided by Sales.



\# Limitations



This project has the following limitations:



\- Validation was limited to information available within the dataset.

\- External system verification was outside project scope.

\- Customer master data was unavailable.

\- Product master validation could not be performed.

\- Some assumptions were necessary where source information was incomplete.



\# Repository Structure



part1\_data\_cleaning/

├── data/

│ ├── raw\_orders.xlsx

│ └── cleaned\_orders.xlsx

├── outputs/

│ ├── data\_quality\_report.xlsx

│ ├── pivot\_summary.xlsx

│ └── cleaning\_log.md

├── screenshots/

│ ├── raw\_data\_preview.png

│ ├── cleaned\_data\_preview.png

│ ├── pivot\_summary\_1.png

│ └── pivot\_summary\_2.png

└── README.md



\# Screenshots Included


The repository includes the following screenshots:



\- Raw Dataset Preview

\- Cleaned Dataset Preview

\- Pivot Summary Report 1

\- Pivot Summary Report 2



These screenshots provide visual evidence of the cleaning process and reporting outputs.



\# Conclusion


The project successfully transformed a raw transactional retail dataset into a standardized, validated, and analysis-ready dataset. Business rules were consistently applied, data quality issues were documented, and management-ready reports were developed using Microsoft Excel. The cleaned dataset now provides a reliable foundation for reporting, visualization, and future business analytics initiatives.

