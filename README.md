# tokyo-olympic-azure-data-engineering-project

## Introduction

This project showcases an end-to-end Azure data engineering pipeline built using the Tokyo Olympics 2020 dataset. Although the entire workflow could be implemented solely within Azure Synapse Analytics, the primary goal of this project is to gain hands-on experience with multiple Azure services and understand how they integrate within a modular, real-world data pipeline. The solution ingests raw data from a public Kaggle dataset, stores it in Azure Data Lake Storage Gen2, performs data transformations using Azure Databricks, and exposes the curated data for analytics and reporting through Azure Synapse Analytics.

## Architecture

<img width="687" height="191" alt="image" src="https://github.com/user-attachments/assets/f1edb66f-27de-4f62-94fb-b97bcc8717be" />

**Data Source** - DataSet sourced from Kaggle

**Data Ingestion** – Azure Data Factory

Used Azure Data Factory (ADF) to build a pipeline. It copies data from Kaggle (via GitHub or HTTP) into Azure. This is the Extract step in ETL

**Raw Data** – Azure Data Lake Storage Gen2 - The raw CSV files are stored in ADLS Gen2 in a folder like /raw-data

**Transformation** – Azure Databricks

**Transformed Data** – Azure Data Lake Storage (Curated Layer) - After transformation, data is written back to ADLS Gen2, under /transformed-data. Now it's clean, structured, and ready for analytics

**Analytics** – Azure Synapse Analytics

## Technologies Used
Azure Services: Data Factory, Data Lake Gen2, Azure Databricks, Synapse Analytics Programming: Python, SQL, Pyspark 
