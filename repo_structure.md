snowflake-ecommerce-pipeline/
├── README.md
├── sql/
│   ├── 01_init_db_and_warehouse.sql
│   ├── 02_file_format_and_stage.sql
│   ├── 03_create_raw_tables.sql
│   ├── 04_create_snowpipe_orders.sql
├── dbt_models/
│   ├── stg_orders.sql
│   ├── stg_customers.sql
│   ├── stg_products.sql
│   ├── dim_customer.sql
│   ├── dim_product.sql
│   ├── fact_orders.sql
└── sample_data/
    ├── customers.csv
    ├── products.csv
    └── orders.csv
