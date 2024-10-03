# Azure End-to-End Data Engineering Real-Time Project
 This project is a data engineering pipeline solution to a made-up business problem, created to aid in my learning and understanding of data pipelining.
 
 
 ## Project Overview
 This project aims to build a comprehensive data pipeline on Azure. The goal is to extract customer and sales data from an API, transform it in the cloud, and generate actionable insights through a Tableau dashboard.  

##  Business Requirements
 The business has identified a gap in understanding customer demographics—specifically gender distribution—and how it influences product purchases. The key requirements include:
1.	Sales by Gender and Product Category: A dashboard showing the total products sold, total sales revenue, and a gender split among customers.
2.	Data Filtering: Ability to filter the data by product category, gender, and date.
3.	User-Friendly Interface: Stakeholders should have access to an easy-to-use interface for making queries.

## Workflows
Here is the general workflow of the project:

![image](https://github.com/user-attachments/assets/b95b9ff1-cf0b-41d8-a4ce-11f5a80f6a65)

## Technology Stack
•	Azure Data Factory (ADF): For orchestrating data movement and transformation.
•	Azure Data Lake Storage (ADLS): For storing raw and processed data,  
•	Azure Databricks: For data transformation and processing.
•	Azure Synapse Analytics: For data warehousing and SQL-based analytics.
•	Tableau: For data visualization and reporting.


## Setup Instructions

### Step 1: Azure Environment Setup
1.	Create Resource Group: Set up a new resource group in Azure.
2.	Provision Services:
o	Create an Azure Data Factory instance.
o	Set up Azure Data Lake Storage .
o	Set up an Azure Databricks workspace and Synapse Analytics workspace.

### Step 2: Data Ingestion
1.	Ingest Data with ADF: Create pipelines in ADF to copy data from GitHub API to the storage ADLS.

### Step 3: Data Transformation
1.	Mount Data Lake in Databricks: Configure Databricks to access ADLS.
2.	Transform Data: Use Databricks notebooks to clean and aggregate the data, moving from source_data folder in ADLS to Transformed folder.  

### Step 4: Data Loading and Reporting
1.	Load Data into Synapse: Set up a Synapse SQL pool and load the Transformed_ data for analysis.
2.	Create Tableau Dashboard: Connect tableau to Synapse and create visualizations based on business requirements.

### Step 5: Automation and Monitoring
1.	Schedule Pipelines: Use ADF to schedule the data pipelines to run daily.
2.	Monitor Pipeline Runs: Use the monitoring tools in ADF and Synapse to ensure successful pipeline execution.



