US Workforce Trends ETL Pipeline

## Overview

This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline developed using SQL Server Integration Services (SSIS) and SQL Server. The pipeline integrates multiple public datasets related to employment, education attainment, and population statistics to produce a unified dataset for workforce trend analysis at the county level.

## Objective

The objective of this project is to build a structured and queryable dataset that enables analysis of workforce patterns and regional disparities across counties in the United States.
The ETL pipeline focuses on cleaning, standardizing, and integrating heterogeneous datasets to support workforce analytics.

## Data Sources

The project integrates three primary datasets:

• Census of Employment and Wages (BLS – 2023)
Approximately 64,000 records used as the primary workforce dataset.

• Education Attainment Dataset (2023)
Approximately 900 records containing county-level education statistics.

• Population and Area Density Dataset
Approximately 3,000 records providing demographic context.

All datasets are integrated using county-level FIPS codes.

## ETL Process

The ETL pipeline was built using SSIS and performs the following steps:

**Data Extraction**
Source datasets were imported from CSV and Excel files.

**Data Cleaning**
Industry code prefixes were removed, geographic identifiers were standardized, and metadata rows were filtered to ensure consistent structures across datasets.

**Data Transformation**
Transformations included data type conversions, derived columns, and conditional filtering to produce structured datasets.

**Data Integration**
Datasets were merged using SSIS Merge Join transformations based on county FIPS codes.

**Data Loading**
The final integrated dataset was loaded into SQL Server for further querying and analysis.

## Business Questions Addressed

The integrated dataset enables analysis of workforce trends such as:

• Which counties demonstrate strong employment levels despite lower education attainment?
• Do counties with higher population and education levels show higher average wages?
• Which regions have strong educational attainment but lower employment in high-wage industries?

## Technologies Used

SQL Server
SQL Server Integration Services (SSIS)
SQL Server Data Tools (SSDT)
T-SQL
CSV and Excel datasets

## Repository Contents

Census_data_Clean.dtsx – SSIS package responsible for data cleaning
Team7_ETL_Project.dtsx – Main ETL pipeline integrating datasets
Project.params – Project configuration parameters
sjanapati_ETL_PRJ.dtproj – SSIS project definition

## Learning Outcomes

This project provided hands-on experience in designing ETL pipelines, integrating heterogeneous datasets, performing data transformations using SSIS, and building structured datasets for workforce analytics.

## License

MIT License
