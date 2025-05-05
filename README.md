# DBT Snowflake Project

## Objective:

This project demonstrates a data pipeline using DBT (Data Build Tool) with Snowflake as the data warehouse and Airflow for orchestration. It processes the TPCH dataset, creates staging tables, performs transformations, and loads fact tables for further analysis.

## Project Structure:

- **dags/dbt_dag.py**: Airflow DAG to orchestrate DBT runs.
- **models/staging/**: Staging models to ingest raw data.
- **models/marts/**: Data marts and transformations to build business-ready tables.
- **macros/**: Custom macros for transformations, like discounted amount calculation.
- **tests/**: Singular and generic tests for data quality checks.
- **requirements.txt**: Dependencies for the Airflow environment.
- **profiles.yml**: DBT profile configuration for Snowflake connection.

## Prerequisites:

- Snowflake account with sample data (TPCH dataset).
- Airflow setup with Astronomer Cosmos.
- DBT installed (using virtual environment).

## Steps to Run:

1. Setup Snowflake connection in **profiles.yml**.
2. Install dependencies with:
    ```bash
    pip install -r requirements.txt
    ```
3. Set up and configure Airflow to use the provided DAG.

## Deployment:

- The pipeline will run daily to process and transform the TPCH data, with tests to ensure data integrity and quality.
