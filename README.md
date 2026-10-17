# Data Warehouse and Analytics Project

Welcome to the **Data Warehouse and Analytics Project** repository! 🚀

This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehouse to generating actionable insights. Designed as a portfolio project, it highlights industry best practices in data engineering and analytics.

The materials of the data warehouse project: the source files, every script from the videos, and the docs.

You take raw files from two systems, a CRM and an ERP, and build one data warehouse in SQL Server. At the end, the data is clean and ready for analysis.

New here? Open the setup guide in the 00_setup folder. It walks you through installing SQL Server and creating the database, on Windows and Mac, with the fixes for the common errors.

```text
sql-data-warehouse-project/
├── 00_setup/                  # Setup guide and Docker configuration for Mac
├── 01_datasets/               # Six source files used in the project
│   ├── source_crm/            # Three files from the CRM system
│   └── source_erp/            # Three files from the ERP system
├── 02_docs/                   # Requirements, diagrams, and documentation
├── 03_scripts/                # SQL scripts organized by processing layer
│   ├── init_database.sql      # Creates the database; run first
│   ├── bronze/                # Loads raw data from CSV files
│   ├── silver/                # Cleans and prepares the data
│   └── gold/                  # Builds tables for analysis
└── 04_tests/                  # Validates Silver and Gold data quality
````


The project reads the six files from C:\sql\dwh_project\01_datasets\. Put the folder there, or change the six paths in 03_scripts/bronze/proc_load_bronze.sql. The videos show the folders without numbers: datasets there is 01_datasets here, scripts is 03_scripts.



## 🏗️ Data Architecture
The data architecture of this project follows the **Medallion Architecture**, which consists of three layers: **Bronze**, **Silver**, and **Gold**.

![Data Architecture](https://github.com/flasherer/sql-data-warehouse-project/blob/main/docs/Data%20Architecture.png)






1. **Bronze Layer:** Stores raw data from CRM and ERP source systems by loading CSV files into SQL Server without applying transformations.

2. **Silver Layer:** Performs data cleansing, standardization, and transformation to improve data quality and ensure consistency.

3. **Gold Layer:** Contains business-ready data organized into fact and dimension tables using a star schema for reporting and analytics.


---

## 🚀 Project Requirements

### Building the Data Warehouse (Data Engineering)

#### Objective

Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

#### Specifications

- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into a single, user-friendly data model designed for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of data is not required.
- **Documentation**: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

--- 


### BI: Analytics & Reporting (Data Analysis)

#### Objective

Develop SQL-based analytics to deliver detailed insights into:

- **Customer Behavior**
- **Product Performance**
- **Sales Trends**

These insights empower stakeholders with key business metrics, enabling strategic decision-making.

--- 


## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.
