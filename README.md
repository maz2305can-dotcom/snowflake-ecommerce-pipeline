# Snowflake E-Commerce ELT Pipeline (Snowpipe + dbt-style Models)

This project demonstrates a small but realistic Snowflake ELT pipeline for an
e-commerce business. Raw CSV files land in cloud storage and are auto-ingested
into Snowflake using Snowpipe, then transformed into analytics-ready tables
using dbt-style layer conventions (raw → staging → marts).

The goal is to showcase:

- Snowflake data platform fundamentals  
- External stages + file formats  
- Snowpipe for near real-time ingestion  
- Raw / staging / marts modeling pattern  
- A simple dimensional model for e-commerce analytics

> Tech focus: **Snowflake, Snowpipe, SQL, ELT modeling**

---

# Architecture


Cloud Storage (e.g. S3) 
   └── raw/ecommerce/*.csv
        ↓ (auto-ingest via S3 event)
Snowpipe
        ↓
RAW tables (orders_raw, customers_raw, products_raw)
        ↓
Staging views (stg_orders, stg_customers, stg_products)
        ↓
Dimensional model (dim_customer, dim_product, fact_orders)
        ↓
BI / analytics (not included)
