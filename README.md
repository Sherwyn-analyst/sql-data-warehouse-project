# SQL Data Warehouse and Analytics Project

An end-to-end SQL data warehouse project independently implemented as part of the Data With Baraa SQL course.

The project demonstrates how raw source data can be loaded, cleaned, transformed, validated, and organised into analysis-ready tables. It also includes analytical SQL queries for generating business insights.

## Project Context

This project was completed as part of the SQL Data Warehouse course by Data With Baraa.

The course provided the project structure, source data, and overall workflow. I independently followed the lessons, implemented and executed the SQL scripts, investigated data-quality issues, and reviewed the results throughout the project.

This repository is intended to document my learning and demonstrate my practical SQL and data warehousing skills.

## Objectives

The main objectives of this project were to:

- Build a structured SQL data warehouse.
- Load raw data from multiple source files.
- Clean and standardise inconsistent data.
- Transform raw records into analysis-ready tables.
- Apply data-quality checks.
- Create a dimensional data model.
- Write analytical SQL queries.
- Generate business insights from the final data layer.

## Architecture

The project follows a layered data warehouse structure:

- **Bronze layer:** Stores raw data with minimal transformation.
- **Silver layer:** Cleans, standardises, and integrates the source data.
- **Gold layer:** Contains business-ready tables and views for analysis and reporting.

![Data warehouse architecture](docs/data_architecture.png)

## Data Sources

The project uses source data related to **sales, customers, products and orders**.

The main source files include:

 **source_crm:** Customer Relationship Management data containing information about customers, products, and sales-related transactions
 **source_erp:** Enterprise Resource Planning data containing supporting business information such as product details, customer attributes, and sales or operational records


The datasets and overall project structure were provided through the course. Please refer to the original course and data source for the applicable usage and redistribution conditions.

## ETL Workflow

The project follows these main steps:

1. Load raw source files into the Bronze layer.
2. Inspect the source data and identify quality issues.
3. Clean missing, duplicate, and inconsistent records.
4. Standardise column names, formats, and values.
5. Integrate related source tables using SQL joins.
6. Load transformed data into the Silver layer.
7. Build business-ready fact and dimension tables.
8. Validate the final data using quality checks.
9. Query the Gold layer to generate analytical insights.

## Data Cleaning and Transformation

The project includes:

- Handling missing values.
- Removing duplicate records.
- Standardising text values and naming conventions.
- Converting columns to appropriate data types.
- Cleaning invalid dates and numeric values.
- Resolving inconsistent source values.
- Joining related tables.
- Creating derived columns.
- Removing unnecessary fields.
- Validating relationships between tables.

## Data Model

The final warehouse contains **1** fact table and **2** dimension tables.

### Fact tables

- **`gold.fact_sales`** — contains details about order ship dates, quantity, price due dates.
- 
### Dimension tables

- **`gold.dim_customers]`** — contains information of customers like name, country, birthdate etc.
- **`gold.dim_products`** — contains information of products like product numbers, category, cost etc.

## Data Quality Checks

The project includes checks for:

- Duplicate records.
- Missing values in required columns.
- Invalid dates.
- Invalid or negative numeric values.
- Missing primary keys.
- Unmatched records after joins.
- Duplicate records in the final tables.
- Referential integrity between fact and dimension tables.
- Unexpected values in categorical columns.

## Analysis Questions

The final analytical queries answer questions such as:

- **Which products or categories generated the most revenue?**
- **How did sales change over time?**
- **Which customers contributed the most sales?**
- **Which regions or markets performed best?**
- **Which products had the highest order volume?**

Replace these with the questions you actually analysed.

## Skills Demonstrated

- SQL Server
- Data warehouse architecture
- ETL and ELT concepts
- Bronze, Silver, and Gold data layers
- Data cleaning and standardisation
- Table creation and transformation
- Joins and aggregations
- Fact and dimension modelling
- Data-quality validation
- Analytical SQL queries
- Database documentation
- Git and GitHub

## Repository Structure

```text
sql-data-warehouse-project/
│
├── datasets/
│   └── README.md
│
├── docs/
│   ├── data_architecture.png
│   ├── data_flow.png
│   ├── data_model.png
│   └── data_catalog.md
│
├── scripts/
│   ├── bronze/
│   │   ├── ddl_bronze.sql
│   │   └── load_bronze.sql
│   │
│   ├── silver/
│   │   ├── ddl_silver.sql
│   │   └── load_silver.sql
│   │
│   └── gold/
│       ├── ddl_gold.sql
│       └── analysis.sql
│
├── tests/
│   └── quality_checks.sql
│
├── README.md
└── LICENSE
```

> Update this structure so it matches your actual folders and filenames.

## How to Run

This project was developed using **SQL Server** and **SSMS**.

1. Install the required database system and SQL client.
2. Create a new database.
3. Run the database and schema setup scripts.
4. Load the raw source data.
5. Run the Bronze-layer scripts.
6. Run the Silver-layer cleaning and transformation scripts.
7. Run the Gold-layer table or view scripts.
8. Run the data-quality checks.
9. Run the analytical SQL queries.

Run the scripts in the following order:

```text
1. Database and schema setup
2. Bronze table creation
3. Bronze data loading
4. Silver table creation
5. Silver data cleaning and transformation
6. Gold table or view creation
7. Data-quality checks
8. Analytical queries
```

## Limitations

- The project is based on the source data provided by the course.
- The analysis is limited to the fields and time period available in the datasets.
- The quality of the results depends on the completeness and accuracy of the source data.
- The project does not currently include automated pipeline scheduling.
- Incremental loading and historical-change tracking were not implemented.
- The results describe historical data and should not be treated as predictions of future performance.

## Attribution

This project was completed as part of the Data With Baraa SQL Data Warehouse course.

The course provided the project structure, learning material, source data, and overall workflow. The SQL scripts were independently implemented, executed, tested, and reviewed by me as part of my learning process.

Please refer to the original course for the complete instructional material and source-data information.

## Author

Sherwyn

Aspiring data analyst building projects with SQL, Python, pandas, data cleaning, data warehousing, and data visualisation.
