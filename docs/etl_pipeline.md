# ETL Pipeline Documentation

This project follows a structured ETL pipeline implemented using PostgreSQL SQL scripts.

## Extraction
- The data is sourced from a Brazilian e-commerce dataset from Kaggle datasets.
- It is then imported into PostgreSQL using DBeaver GUI (manual ingestion)
- Then finally loaded into Bronze schema tables

## Transformation

Transformations were applied in the Silver layer:

### Data Cleaning
- Removed duplicate records
- Handled missing values
- Standardised categorical fields (e.g., case formatting)

### Data Type Conversion
- Converted timestamp fields to proper `TIMESTAMP` format
- Then ensured numeric consistency across all measures

### Business Enrichment
- Calculated delivery duration (delivery_time_days)
- Created late delivery flag (is_late_delivery)
- Derived delay metrics

## Load

The final transformed datasets were loaded into the Gold layer:

- Fact Table:
  - `fact_orders`
- Dimension Tables:
  - `dim_customers`
  - `dim_products`
  - `dim_sellers`

These tables are optimised for analytical queries and reporting tools.