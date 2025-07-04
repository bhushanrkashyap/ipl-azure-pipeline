# IPL Azure Pipeline 

An end-to-end data pipeline project to process IPL (Indian Premier League) data using Azure services. This project demonstrates how raw CSVs are transformed, analyzed, and stored efficiently across the Azure ecosystem.

## 🚀 Project Overview

This pipeline performs:
- Data Ingestion: Uploading IPL CSV files to Azure Blob Storage
- Data Transformation: Processing using PySpark in Azure Databricks
- Graph Generation: Creating visual insights using Matplotlib
- Data Storage: Saving transformed data and graph metadata into Azure Cosmos DB

---
## Architecture diagram:

                +-------------------+
                |   CSV Datasets    |
                +-------------------+
                         |
                         v
             +-------------------------+
             | Azure Databricks (ETL)  |
             |  - PySpark processing   |
             |  - Data cleaning        |
             +-------------------------+
                   |              |
       Cleaned Data|              | Graphs (Matplotlib)
                   v              v
        +-----------------+    +----------------------+
        | Azure Cosmos DB |    |  Azure Blob Storage  |
        |  (5 containers) |    |    Stores images     |
        +-----------------+    +----------------------+
                 |                 |
                 v                 v
        +---------------------------------+
        |     Cosmos DB Metadata          |
        |   - Image metadata stored       |
        +---------------------------------+

## 🛠 Technologies Used

- Azure Blob Storage – for storing raw and processed files
- Azure Databricks – for ETL using PySpark
- Azure Cosmos DB – for final structured storage
- Python – for scripting and visualization (`pandas`, `matplotlib`)

---
