# Data Quality Checks

To ensure reliability and integrity of the data warehouse, several validation checks were implemented across all layers.

## Primary Key Integrity
- Verified uniqueness of primary keys in all dimension tables
- Ensured no duplicate IDs exist in:
  - customers
  - products
  - sellers

## Missing Data Checks
- Identified and handled NULL values in critical fields:
  - order timestamps
  - customer IDs
  - product IDs

## Temporal Validations
- Ensured no negative delivery durations
- Validated logical timestamp order:
  - purchase_ts ≤ delivered_ts

## Referential Integrity
- Verified consistency between:
  - fact_orders and dimension tables
- Ensured all foreign keys in fact table map to valid dimension keys

## Business Logic Validation
- Late delivery flag correctly derived from delivery vs estimated time
- Review scores validated within expected range (1–5)