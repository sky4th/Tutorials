## Data Facotry
- Cloud based ETL as a Service:- Orchestarte data extraction and transformation.
- Extarct/Load data from/to disparate data stores. for e.g. sql server, azure storage account etc
- ADF pipelines helps you build complex data processing either visually using data flows or by using Azure Big Data services like Azure HDInsight Hadoop, Azure Databricks, and Azure SQL Database.

## Steps
1. Extract:-
    - Connect:- Connect to required Data source and extract the data
2. Transform:-
    - Data flow graph:- Transformation executes on Spark, without any knowhow of Spark programming. 
    - Code Transformation:- transform using HDInsight, SPark, Data Lake Analytics and machine learning
3. Load:-
    - Coonect:- connect to required data sink and load the data
## DevOps
moving Data Factory pipelines from one environment (development, test, production) to another.
-  Azure Pipelines
-  Manually upload a Resource Manager template using Data Factory UX
## Monitor
Monitor ADF

## ADF Components
- Pipelines:-Logical Grouping of activities that peforms a task. For e.g. extract data from source, perform transformation and load the transformed data to sink. these all activities can be defined in a pipeline as sequence of task of can be configured to run in parallel.
    - Triggers:- When a pipeline execution should start. there are different types of events to trigger a pipeline
    - Pipeline runs:- An instance of pipeline execution.
    - Parameters:- key-value pairs of read-only configuration. Parameters are passed when a pipeline is triggered or started manually.
    - Control flow:- sequence of activities, defining variables, parameters, passing arguments etc
    - Variables:- Pipeline scope variables can be used
- Activities:- A step in a pipeline
- Datasets:- Data within the data source.
- Linked services:- Connection to a data source. can be either
    - Data Store for e.g. database
    - Compute resource that performs some activity. For example using Spark to perform some transformation using HDInsight
Data Flows :- Graphs of data transformation logic. Data Factory will execute your logic on a Spark cluster.
Integration Runtimes:- This is Compute environment where the activity either runs on or gets dispatched from.
- Data Flows:- Series of transformations. transform data at scale without any coding required. Design a data transformation job in the data flow designer by constructing Data Flows. 
- Integration Runtimes:- Compute environment where the activity either runs on or gets dispatched from.

# ADF implementation using 
- [Terraform](https://tutirials/cloud/azure/azure-data-factory/terraform)
