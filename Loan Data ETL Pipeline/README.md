## Featured Project: Loan Data ETL Pipeline

This project demonstrates a full Extract–Transform–Load (ETL) workflow built in Python, using pandas for data cleaning and PostgreSQL as the data warehouse.

It is designed as a modular, production-friendly ETL pipeline with error handling, logging, environment variables, and clean code structure.

## Project Overview
🔹 Purpose

To create a robust pipeline that:

Extracts raw loan, customer, and payment data from CSV files

Transforms them into clean dimensional tables

Loads them into a PostgreSQL database for analytics, reporting, and modeling

🔹 Data Warehouse Tables

The pipeline generates a star-schema-like structure:

Table Name	Type	Description
dim_customers	Dimension	Cleaned customer attributes (demographics, income, full name…)
dim_loans	Dimension	Loan-level info (principal, interest, monthly payment…)
stg_payments	Staging	Raw cleaned list of all payments
fact_payments	Fact Table	Aggregated loan performance metrics

The structure is ideal for:

Financial modeling

Loan risk scoring

Cohort tracking

Payment behavior insights

## ETL Architecture
1️⃣ Extract

The pipeline loads three CSV files:

customers.csv

loans.csv

payments.csv

Using:

def extract_csv(path: str) -> pd.DataFrame:
    ...


It includes:
✔ File validation
✔ Logging
✔ Row count summaries

2️⃣ Transform

Each dataset goes through a dedicated cleaning function.

✔ clean_customers()

Removes duplicates

Standardizes column names

Converts dates

Handles missing income with median imputation

Generates full_name

✔ clean_loans()

Converts numerics & dates

Computes monthly payment using annuity formula

Ensures uniqueness of loan_id

✔ clean_payments()

Parses dates

Standardizes numeric values

Removes duplicates

✔ build_fact_table()

Creates the analytics-ready fact table:

Total paid

Number of payments

Last payment date

Default flag (rule-based)

This brings financial intelligence into the dataset.

3️⃣ Load

All cleaned tables are inserted into PostgreSQL using SQLAlchemy.

Key features:

Transaction-safe bulk insert

replace mode for easy testing

Optional schema creation

Structured data warehouse design

## Core Technologies Used
---
Python 3.10+

pandas

SQLAlchemy

PostgreSQL

dotenv

Logging module

Docker (optional for deployment)
