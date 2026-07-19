# Customer Support Ticket Resolution Pipeline

A Databricks/PySpark pipeline that ingests raw customer support ticket logs,
cleans and validates them, applies business rules (resolution quality threshold,
team scope filter, Day-2 carry-over), and produces Gold-layer KPIs for leadership reporting.

## Architecture
Bronze (raw ingestion) → Silver (cleaning + business rules) → Gold (aggregated KPIs)

## Notebooks
- `Config` — shared config and table names
- `bronze_ingestion` — reads CSVs from Unity Catalog Volume, writes Bronze tables
- `silver_transformation` — joins, filters, applies business rules
- `gold_aggregation` — computes final KPIs

## Business Rules
See full documentation in `docs/Customer_Support_Pipeline_Documentation.docx`

## Data
Sample data with intentional edge cases (nulls, malformed times, out-of-scope agents)
is in `data/raw/`.
