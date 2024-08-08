# AWS Data Pipeline Project

## Overview

This project demonstrates the creation of a scalable data pipeline using various AWS services. The pipeline covers the entire process from data ingestion and processing to storage in a data warehouse, followed by visualization. The technologies used include AWS S3, Glue, Athena, Redshift, and Python scripting in Jupyter Notebooks. The final output can be visualized using Power BI or Tableau.

## Table of Contents

- [Project Structure](#project-structure)
- [Tools and Technologies](#tools-and-technologies)
- [Architecture](#architecture)
- [Steps Followed](#steps-followed)
  - [1. Relational Data Model](#1-relational-data-model)
  - [2. Connect Athena and Query Data](#2-connect-athena-and-query-data)
  - [3. ETL Job in Python](#3-etl-job-in-python)
  - [4. Save Result to S3](#4-save-result-to-s3)
  - [5. Glue Deployment](#5-glue-deployment)
  - [6. Build Tables on Redshift](#6-build-tables-on-redshift)
  - [7. Copy Data to Redshift](#7-copy-data-to-redshift)
  - [8. Data Visualization](#8-data-visualization)
- [Usage](#usage)
  - [Prerequisites](#prerequisites)
  - [Running the Project](#running-the-project)
- [Conclusion](#conclusion)
- [License](#license)

## Project Structure

This project is organized as follows:

- **Datasets**: Stored in AWS S3.
  ![Data Flow](C:\Users\Welcome\Downloads\proj_aws\snips\dataset_bucket.png)
  
- **Data Processing**: Performed using AWS Glue.
- **Data Querying**: Handled through AWS Athena.
- **Data Warehousing**: Managed using AWS Redshift.
- **Scripting**: Automated ETL tasks using Python in Jupyter Notebooks.
- **Data Visualization**: Achieved through Power BI or Tableau.

## Tools and Technologies

- **AWS S3**: For storing raw and processed data.
- **AWS Glue**: To crawl the datasets and define schemas.
- **AWS Athena**: To run SQL queries on data stored in S3.
- **AWS Redshift**: For creating a data warehouse and running complex queries.
- **Python (Jupyter Notebooks)**: For scripting ETL processes.
- **Power BI / Tableau**: For visualizing data stored in Redshift.

## Architecture

The architecture of this data pipeline includes:

1. **Data Storage**: Raw data is stored in S3.
2. **Data Processing**: AWS Glue is used to define the schema and process the data.
3. **Querying**: Data is queried using AWS Athena to verify correctness.
4. **Data Warehousing**: Data is moved to Redshift for further processing and storage.
5. **Visualization**: Power BI or Tableau connects to Redshift to create visualizations.

## Steps Followed

### 1. Relational Data Model

Defined the relational data model to organize the data in a structured format, ensuring relationships between entities are clearly established.

### 2. Connect Athena and Query Data

Connected AWS Athena to the data stored in S3 to run queries and ensure the data is in the correct format and structure.

### 3. ETL Job in Python

Developed Python scripts to perform ETL (Extract, Transform, Load) operations:

- **Extract**: Load data from S3.
- **Transform**: Clean and transform the data.
- **Load**: Save the processed data back to S3.

### 4. Save Result to S3

After processing, the transformed data was saved as CSV files back to a specified S3 bucket for further steps.

### 5. Glue Deployment

AWS Glue was used to deploy crawlers and jobs for data processing, ensuring the data schema is continuously updated and accurate.

### 6. Build Tables on Redshift

Created tables in AWS Redshift to match the relational data model, preparing the data warehouse for data import.

### 7. Copy Data to Redshift

Used Python scripts to execute the `COPY` command, transferring the data from S3 to Redshift tables, followed by verification through SQL queries.

### 8. Data Visualization

Finally, the data in Redshift was connected to Power BI or Tableau for visualization, enabling insightful analysis through interactive dashboards.

## Usage

### Prerequisites

- An AWS account with access to S3, Glue, Athena, and Redshift.
- Python environment with necessary libraries (`boto3`, `psycopg2`, `redshift_connector`).
- Jupyter Notebook for running the ETL scripts.
- Power BI or Tableau for visualization.

### Running the Project

1. **Set up S3 buckets**: Upload your datasets to S3.
2. **Configure Glue**: Set up crawlers and jobs to process the data.
3. **Run Athena Queries**: Ensure data correctness using Athena.
4. **Execute Python Scripts**: Run the provided Jupyter Notebooks to perform ETL tasks.
5. **Set up Redshift**: Create the necessary tables and load data.
6. **Visualize**: Connect to Redshift from Power BI or Tableau to create visualizations.

## Conclusion

This project illustrates how to build a comprehensive data pipeline using AWS services, culminating in the ability to visualize data through Power BI or Tableau. It serves as a practical example of integrating cloud-based services for data processing and analysis.
---

*GitHub Repository: [shreykumar33](https://github.com/shreykumar33)*
