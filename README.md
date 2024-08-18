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

![architecture#1](https://github.com/user-attachments/assets/1eb688a3-dfdb-487b-9f8b-dea9db7a2eba)


- **Datasets**: Stored in AWS S3.
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

    ![s3_1](https://github.com/user-attachments/assets/5411a275-dc14-4f2d-b4ef-42f8b76b3e09)
   
    ![dataset_bucket](https://github.com/user-attachments/assets/0947a4d5-9822-4893-bd12-19f84062a7e3)
   

    ![ds1](https://github.com/user-attachments/assets/2c3f3047-27e3-4ca2-9f6d-6f65346d033a)


    ![ds2](https://github.com/user-attachments/assets/2dc9652c-835f-4430-bbe0-3bd4d0ff35bf)


    ![ds3](https://github.com/user-attachments/assets/3512e336-b055-4ecd-91b7-8ddc82cb4f15)




3. **Data Processing**: AWS Glue is used to define the schema and process the data.
   
    ![glue2](https://github.com/user-attachments/assets/7342bae3-0eb6-4a46-ab51-18f868ad0270)

   
    ![glue1](https://github.com/user-attachments/assets/6552bcfa-4221-428b-a6ca-c9ebdc5176bc)

   

4. **Querying**: Data is queried using AWS Athena to verify correctness.
   
   ![athena1](https://github.com/user-attachments/assets/83b0b178-9522-4998-8529-d24dd00cac56)

   
   ![athena2](https://github.com/user-attachments/assets/96217ffc-d132-4c03-ad83-8272e9dd2dd9)

   

4. **Data Warehousing**: Data is moved to Redshift for further processing and storage.
   
   ![redshift1](https://github.com/user-attachments/assets/878b5bd1-ce93-401c-9d52-4684fb2a8aef)

   
   ![redshift2](https://github.com/user-attachments/assets/35ade64a-d975-4276-bea6-20eb7eb31aab)

   
   ![red](https://github.com/user-attachments/assets/8e93673c-81f9-4f9e-b75a-70e83329dc10)



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

 ![out](https://github.com/user-attachments/assets/6a3c89dd-0bcd-45cd-979b-dc80b6305b82)

 
 ![output_bucket](https://github.com/user-attachments/assets/806dc4fb-f088-4a06-93be-b88b23e7443c)
 


### 5. Glue Deployment

AWS Glue was used to deploy crawlers and jobs for data processing, ensuring the data schema is continuously updated and accurate.

 ![crawler](https://github.com/user-attachments/assets/def8fa93-3076-40a9-8b49-e85ea75843b6)

 
 ![role1](https://github.com/user-attachments/assets/263c2987-f2c4-4596-8fd9-31484587ce8e)

 
 ![crawler2](https://github.com/user-attachments/assets/ee0f1ec0-b043-480f-b485-95f2bd8d864b)

 

### 6. Build Tables on Redshift

Created tables in AWS Redshift to match the relational data model, preparing the data warehouse for data import.

### 7. Copy Data to Redshift

Used Python scripts to execute the `COPY` command, transferring the data from S3 to Redshift tables, followed by verification through SQL queries.

### 8. Data Visualization

Finally, the data in Redshift was connected to Power BI or Tableau for visualization, enabling insightful analysis through interactive dashboards.

## Usage

### Prerequisites

- An AWS account with access to S3, IAM, Glue, Athena, and Redshift.
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
