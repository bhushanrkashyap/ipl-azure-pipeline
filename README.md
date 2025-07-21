# IPL Azure Data Pipeline
A scalable, end-to-end data engineering pipeline for Indian Premier League (IPL) analytics, built using Microsoft Azure services. The solution demonstrates modern data ingestion, transformation, storage, and visualization with a focus on scalability, automation, and extensibility.

# 📦 Features

Raw Data Ingestion: Upload IPL datasets (CSV) to Azure Blob Storage.

Data Transformation: Use PySpark on Azure Databricks to clean and process raw datasets.

Data Storage: Store cleansed and transformed data in Azure Cosmos DB SQL API for structured, queryable storage.

Image Storage: Visualization plots and generated artefacts are saved in Azure Blob Storage.

Visualization: Create analytical graphs using Python’s Matplotlib for IPL data insights.

# 🚀 Architecture Overview
1.Data Upload:
Raw IPL CSV files are uploaded to an Azure Blob Storage container.

2.Compute & Transform:
Azure Databricks reads from Blob Storage, transforms and cleanses data using PySpark.
Processed data is exported as structured records.

3.Storage
Transformed datasets are written to Cosmos DB (SQL API) for scalable, queryable storage.
Visualization outputs (graphs, plots) are saved as images in Blob Storage.

4.Visualization & Analytics
Python Matplotlib scripts generate insights from processed IPL data and output PNG/JPG files to Blob Storage.

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


