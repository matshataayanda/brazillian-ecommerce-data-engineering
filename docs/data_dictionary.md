# Data Dictionary

This document describes the structure and meaning of key tables in the data warehouse.

## fact_orders

It is the ventral fact table capturing order level transactions.

- order_id: Unique identifier for each order
- customer_id: Customer placing the order
- purchase_ts: Order purchase timestamp
- delivered_ts: Delivery timestamp
- delivery_time_days: Time taken to deliver the order
- is_late_delivery:  Indicator of delayed delivery (1 = late, 0 = on-time)
- review_score: Customer satisfaction rating (1–5)

## dim_customers

This is the customer dimension table.

- customer_id: Unique customer identifier
- customer_city: City of customer
- customer_state: State of customer
- customer_zip_code_prefix: Postal region identifier

## dim_products

This is the product dimension table.

- product_id: Unique product identifier
- product_category_name: Product category
- product_weight_g: Weight in grams
- product_length_cm: Length in cm
- product_height_cm: Height in cm
- product_width_cm: Width in cm

## dim_sellers

This is the seller dimension table.

- seller_id: Unique seller identifier
- seller_city: Seller location city
- seller_state: Seller location state