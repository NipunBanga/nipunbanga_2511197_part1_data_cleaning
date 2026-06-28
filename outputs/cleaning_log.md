\# Data Cleaning Log



\## Project Objective



The objective of this project was to clean, validate, standardize, and prepare the retail sales dataset for accurate business reporting and analysis. The original dataset contained multiple data quality issues that could negatively impact business insights if left unresolved. All cleaning activities were performed on a separate copy of the dataset while preserving the original raw data.



\# Initial Data Assessment



Before performing any cleaning operations, the dataset was reviewed to identify potential quality issues. The assessment focused on text consistency, missing values, duplicate records, date validity, calculation accuracy, and business rule compliance.



The following areas were examined:



\- Customer Information

\- Geographic Information

\- Product Information

\- Order Details

\- Shipping Information

\- Sales \& Profit Data

\- Discount Values

\- Payment Status

\- Order Status



\# Data Quality Issues Identified



The following issues were identified during data profiling:



\## Text Issues



\- Leading spaces

\- Trailing spaces

\- Multiple spaces between words

\- Inconsistent capitalization

\- Inconsistent naming conventions

\- Similar values written differently



Examples:



\- East / east / EAST

\- Office supplies / Office Supplies

\- Standard Class / Standard class



\## Missing Values



Missing values were identified in:



\- Region

\- Ship Mode

\- Discount

\- Date fields (where applicable)



Missing mandatory information was documented and handled according to the business rules provided in the assignment.



\## Duplicate Records



The dataset was reviewed for two types of duplicate records:



\### Exact Duplicate Rows



Rows containing identical information across all columns were identified.



\### Duplicate Order IDs



Order IDs appearing multiple times with conflicting business information were identified and flagged for review.



\## Date Issues



The following date validations were performed:



\- Missing Order Dates

\- Missing Ship Dates

\- Invalid Date Formats

\- Ship Date earlier than Order Date



Invalid shipping records were clearly flagged.



\## Discount Validation



Discount values were reviewed for:



\- Missing Discount

\- Negative Discount

\- Discount exceeding acceptable business limits



Invalid discount values were marked for review.



\## Sales \& Profit Validation



Sales and Profit values were compared with calculated values to identify possible inconsistencies.



Validation included:



\- Sales calculation mismatch

\- Profit calculation mismatch

\- Incorrect discount impact



\# Cleaning Activities Performed



\## Step 1 — Text Standardization



The following Excel techniques were used:



\- TRIM()

\- SUBSTITUTE()

\- Find \& Replace

\- Proper formatting where appropriate



Fields cleaned:



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



Result:



\- Standardized text values

\- Improved consistency

\- Reduced duplicate category names



\## Step 2 — Date Standardization



Both Order Date and Ship Date were converted into a consistent date format.



The following checks were completed:



\- Invalid dates identified

\- Missing dates identified

\- Shipping dates validated

\- Shipping Delay calculated



New calculated column created:



\*\*shipping\_delay\_days\*\*



\## Step 3 — Missing Value Handling



Missing values were handled using assignment business rules.



| Field | Action Taken |

|--------|--------------|

| Region | Filled with "Unknown" |

| Ship Mode | Filled with "Unknown" |

| Discount | Replaced with 0 only when valid |



All replacements were documented within the Data Quality Report.



\## Step 4 — Duplicate Handling



Duplicate validation followed the assignment requirements.



Actions performed:



\- Exact duplicate rows identified

\- Duplicate Order IDs reviewed

\- Exact duplicates removed where appropriate

\- Conflicting duplicates retained and flagged



No potentially valid business records were removed without review.



\## Step 5 — Business Rule Validation



The following business rules were applied.



\### Missing Region



Replaced with:



Unknown



\### Missing Ship Mode



Replaced with:



Unknown



\### Missing Discount



Replaced with zero only when remaining financial information was valid.



\### Negative Discount



Marked as Invalid.



\### Excessive Discount



Flagged for business review.



\### Cancelled Orders



Excluded from completed sales summaries.



\### Failed Payments



Excluded from completed sales summaries.



\### Refunded Orders



Reported separately for business analysis.



\### Invalid Shipping



Ship Date occurring before Order Date was flagged as an invalid record.



\# Calculated Columns Created



The cleaned dataset contains the following calculated columns.



| Column | Purpose |

|---------|---------|

| cleaned\_discount | Standardized discount value |

| calculated\_sales | Recalculated sales amount |

| calculated\_profit | Recalculated profit |

| profit\_margin | Profit ÷ Sales |

| shipping\_delay\_days | Delivery duration |

| order\_month | Reporting month |

| order\_year | Reporting year |

| data\_quality\_flag | Clean / Warning / Invalid |



These calculations improve reporting consistency and simplify future analysis.



\# Data Validation Summary



The dataset was validated for:



\- Missing Values

\- Duplicate Records

\- Invalid Discounts

\- Invalid Dates

\- Shipping Validation

\- Order Status Validation

\- Payment Status Validation

\- Sales Calculation Accuracy

\- Profit Calculation Accuracy



Any records requiring manual review were clearly flagged instead of being silently removed.



\# Records Removed



Only confirmed duplicate rows were removed where duplicate information was identical.



No conflicting business transactions were deleted automatically.



\# Records Flagged



The following record categories were flagged for review:



\- Invalid Discount

\- Invalid Shipping Date

\- Duplicate Order IDs

\- Failed Payment

\- Cancelled Order

\- Refunded Order

\- Sales Calculation Mismatch

\- Profit Calculation Mismatch



\# Business Outcome



After completion of all cleaning activities, the dataset became:



\- Standardized

\- Consistent

\- Validation-ready

\- Reporting-ready

\- Suitable for Pivot Tables

\- Suitable for Dashboard Development

\- Suitable for Business Analytics



\# Assumptions



The following assumptions were made during the cleaning process:



\- Missing Region values were replaced with "Unknown".

\- Missing Ship Mode values were replaced with "Unknown".

\- Missing Discount values were considered zero only where remaining financial information was complete.

\- Duplicate Order IDs with conflicting information were retained for manual review.

\- Shipping Delay was calculated as Ship Date minus Order Date.

\- Profit Margin was calculated using Profit divided by Sales.



\# Limitations



Although extensive cleaning was performed, the following limitations remain:



\- Validation was limited to information available within the provided dataset.

\- External customer or product master data was unavailable.

\- Certain business validations require domain knowledge beyond the assignment scope.

\- Some assumptions were necessary due to incomplete source information.



\# Final Summary



The project successfully transformed the raw retail sales dataset into a clean, validated, and analysis-ready dataset. All required business rules were implemented, calculated columns were created, duplicate and missing data issues were addressed, and comprehensive quality checks were documented. The final output supports accurate reporting, reliable business analysis, and future dashboard development.

