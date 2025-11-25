Run initialization script

- sql/01_init_db_and_warehouse.sql


Create file format & external stage

- sql/02_file_format_and_stage.sql


Update the URL='s3://...' to match your bucket or external location.

Create raw tables

- sql/03_create_raw_tables.sql


Create Snowpipe

- sql/04_create_snowpipe_orders.sql


In a real environment, configure S3 event notifications or use ALTER PIPE ... REFRESH for manual loading.

Load sample data

Upload the CSV files from /sample_data to your cloud storage path, e.g.:

s3://your-bucket/raw/orders/orders_2024_01.csv

s3://your-bucket/raw/customers/customers_2024_01.csv

s3://your-bucket/raw/products/products_2024_01.csv

Create staging and marts

Run the SQL files under /dbt_models to create views and tables.
