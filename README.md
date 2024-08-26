🚀 From On-Premises to Azure: My Data Migration Journey 🌐

Overview
In this project, I migrated data from an on-premises SQL Server to Azure using various Azure services. Below is a detailed breakdown of the process.
![Alt_text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/mini-project.png)

1. Azure Data Factory (ADF)
Setup:
Self-Hosted Integration Runtime: Configured to connect ADF to the on-premises SQL Server.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/ir.png)

Data Extraction:
Extracted Raw Data: Retrieved data from the SQL Server.

Data Retrieval:
Lookup Activity: Used to fetch table names.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/lookup.png)

For Each Activity: Iterated through all tables.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/foreach.png)

Parameterization:
Parameterized Datasets: Avoided manual entry by using parameters for table names and schema names.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/dataset3.png)

Scheduling:
Scheduled Triggers: Ensured efficient pipeline execution.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/trigger.png)

Data Loading:
Loaded Data into ADLS Gen2: Data was saved in Parquet format.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/storagemount.png)

2. Azure Data Lake Storage Gen2 (ADLS Gen2)
Medallion Architecture:
Implemented to organize and manage data through different layers.

Data Segmentation:
Bronze Layer: Raw data ingested from the on-premises SQL Server.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/bronze.png)

Silver Layer: Transformed raw data.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/silver.png)

Gold Layer: Curated, aggregated, and transformed data.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/gold.png)



4. Databricks Community Edition
   
Data Transformation:
Column Renaming: Standardized column names.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/stog.png)

Date Formatting: Formatted dates for consistency.
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/btos.png)

Data Output:
Transformed Data: Data was converted to Delta format and saved back to ADLS Gen2.

4. Azure Key Vault
Credential Management:
Stored Credentials: Securely stored SQL Server credentials (username and password).
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/sqlserverekv.png)

Integration with ADF: Utilized stored credentials in ADF for linked services.

LinkedServices:
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/linkedservice.png)

DataSets:
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/dataset1.png)
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/dataset2.png)
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/dataset3.png)

PipeLine:
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/pipeline.png)

Monitor (PipelineRun):
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/pipelinerun.png)

Storage Account:
![Alt text](https://github.com/VarunK715/azuredataproject/blob/main/screenshot/storageac.png)


