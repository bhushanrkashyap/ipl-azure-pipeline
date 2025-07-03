IPL Azure Pipeline:

An end-to-end data engineering project that processes Indian Premier League (IPL) datasets using Azure cloud services.

Overview:

This project demonstrates a complete data pipeline built on Microsoft Azure. It takes raw IPL CSV data, transforms it using Databricks (PySpark), generates insights and visualizations, and stores both the cleaned data and graphs in Azure services.

---

Technologies Used:

- Azure Blob Storage – for storing raw and processed data.
- Azure Databricks – for data transformation and analysis using PySpark
- Azure Cosmos DB – for storing final datasets and graph metadata
- Python (Pandas, Matplotlib) – for data manipulation and visualization

---

Pipeline Steps:

1. Raw IPL CSV files are uploaded to Azure Blob Storage.
2. Azure Databricks notebooks process and transform the data using PySpark.
3. Graphs and visualizations are generated in Databricks using Matplotlib.
4. Graph images are saved to Azure Blob Storage.
5. Cleaned datasets and graph metadata (image URLs) are uploaded to Cosmos DB.

---
