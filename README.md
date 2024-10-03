# ETL Pipeline Project

## Description
This project implements an ETL (Extract, Transform, Load) pipeline that extracts data from simulated sources, transforms the data, and loads it into a SQL Server database. The project generates customer and product data, handles null values, and ensures data integrity during the loading process.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [ETL Process Overview](#etl-process-overview)
- [Testing](#testing)
- [Automation and Scheduling](#automation-and-scheduling)
- [Reports](#reports)


## Installation
1. Clone the repository:
    

    git clone <repository-url>
    cd <repository-name>

2. Install dependencies:
    
bash
    pip install pandas faker pyodbc requests


## Usage
To run the ETL pipeline, execute the following command:
bash
python etl_pipeline.py
Ensure your SQL Server is running and that the database connection details in the script are configured correctly.

## ETL Process Overview
Extract: Data is generated using the Faker library to simulate customer and product data.
Transform:
Data is cleaned and normalized (handling null values, stripping whitespace).
Duplicates are checked before inserting into the database.
Load: The transformed data is inserted into the SQL Server database, ensuring integrity by avoiding duplicates.
Testing
To run the tests, use:
## Testing
pytest
Tests are included to validate the transformation logic and data integrity.

## Automation and Scheduling
The ETL pipeline can be automated using Windows Task Scheduler. Create a batch file (run_etl.bat) with the following content to run your script:

@echo off
cd C:\Users\HP\Desktop
python etl_pipeline.py


## Reports
Basic reports can be generated from the data warehouse using SQL queries. Examples include:

Total sales by product
Customer segmentation
Daily sales trends
