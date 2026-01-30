# Olist E-Commerce Analytics Pipeline

---

## Overview
This project implements an end-to-end data engineering pipeline for e-commerce analytics using AWS S3, AWS Glue, and Amazon Athena.  
The pipeline transforms raw transactional data into analytics-ready datasets using a medallion (Bronze–Silver–Gold) architecture.

---

## Business Problem
Raw e-commerce transactional data is not directly suitable for analytical querying and business intelligence.
This project demonstrates how raw data can be ingested, cleaned, transformed, and modeled into a star schema
to support analytical use cases such as revenue analysis and customer behavior insights.

---

## Architecture
High-level architecture:
- Data storage: Amazon S3
- Data processing: AWS Glue (PySpark)
- Analytics engine: Amazon Athena
- Architecture pattern: Medallion (Bronze, Silver, Gold)

---

## Data Flow
1. Raw CSV files are stored in Amazon S3 (Bronze layer)
2. AWS Glue jobs clean and standardize data into Parquet format (Silver layer)
3. AWS Glue transforms Silver data into a star schema (Gold layer)
4. Amazon Athena queries Gold tables for analytics

---

## Constraints
This project is developed under AWS sandbox constraints.
Details are documented in `docs/constraints.md`.

---

## Analytics Examples
Sample analytical queries are available in `athena/analytics_queries.sql`.

