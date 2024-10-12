# On_Premise(SQL SERVER)_to_Delta_Lake

## Agenda
I have data in SQL Server (AdventureWorks), and I want to migrate all this data into a Delta Lake, where the BI team can connect and create reports.

### Technologies 
`SQL`
`Python`
`Azure Databricks`
`Azure Data Factory`
`Azure Data Lake`
`Logic App`
### ETL
Extracted data from SQL Server using **Azure Data Factory** and loaded it into the **Azure Data Lake** Bronze layer. The data was then moved into an archive layer for future reference. Null values and duplicate records were removed from the Bronze layer using **Azure Databricks**, and the cleaned data was placed into the Silver layer. In the Silver layer, business logic was applied, such as dropping unnecessary data and deriving business columns. Finally, Delta tables were created in the Hive Metastore for further analysis.Additionally, **Azure Logic Apps** was used to send email notifications when a pipeline failed.

