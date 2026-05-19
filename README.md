# Brazilian Ecommerce Data Engineering Project
 
## Overview
This project builds a complete end-to-end data engineering pipeline using a Brazilian e-commerce datasetsfrom Kaggle Dataset.  
It follows a Medallion Architecture (Bronze → Silver → Gold) and demonstrates data ingestion, cleaning, transformation, and analytical modelling using SQL, PostgreSQL and DBeaver.

The goal is to simulate a real-world analytics engineering environment and build a production-style data warehouse.

## Architecture

The pipeline follows a 3-layer structure:

- **Bronze Layer**: Raw data ingestion (unchanged csv source tables)
- **Silver Layer**: Cleaned, standardized, and validated datasets
- **Gold Layer**: Business-ready star schema (facts & dimensions)

## Data Model

- ## Fact Table
  - fact_orders
    -This shows : - Order lifecycle metris
                  - Delivery performance
                  - Customer review scores

- ## Dimension Tables
  - dim_customers
  - dim_products
  - dim_sellers
 
## Tech Stack
- PostgreSQL
- SQL (ETL + transformations)
- DBeaver (development environment)
- Git & GitHub (version control)


## ETL Process

### 1. Bronze Layer (Raw Ingestion)
- Data is loaded directly from the source files
- No transformations were applied

### 2. Silver Layer (Data Cleaning)
- Removed duplicates (DISTINCT)
- Standardised text fields (TRIM, LOWER, UPPER)
- Handled NULLs and empty strings (NULLIF)
- Converted data types (timestamps, numeric fields)

### 3. Gold Layer (Data Modelling)
- Built a star schema
- Created fact and dimension tables
- Added business metrics:
  - Delivery time
  - Delay flags
  - Late delivery indicators

## Key Business Metrics

- Delivery time (days between purchase and delivery)
- Delivery delays vs estimated dates
- Customer review scores
- Order fulfilment performance

## Data Quality Checks

- Duplicate detection on primary keys
- NULL validation on critical fields (order timestamps, IDs)
- Negative or invalid delivery time checks
- Referential integrity between fact and dimension tables

## Key Learnings

- Built a full ETL pipeline using SQL
- Implemented a medallion architecture
- Designed a star schema for analytics
- Handled real-world messy ecommerce data
- Applied data cleaning and transformation techniques at scale

## Future Improvements

- Build Power BI / Tableau dashboard
- Automate pipeline using dbt or Airflow
- Add partitioning and performance optimisation

## Project Structure

sql/
-bronze/
-silver/
-gold/

docs/
-architecture.md
-data_dictionary.md
-etl_pipeline.md
-data_quality_checks.md

## Author
Data Engineering Project by Ayanda Angel Matshata  
Focused on Data Engineering, Analytics, and Data Science applications.
