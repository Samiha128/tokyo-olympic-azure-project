# tokyo-olympic-azure-project
# Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Data Pipeline](#data-pipeline)
- [Repository Structure](#repository-structure)
- [How to Run](#How-to-Run)
- [Dashboard](#dashboard)
##  Project Overview:
Beginning with the 2021 Olympics data stored in GitHub’s CSV files, this project employs Azure Data Factory (ADF) to smoothly bring this information into the raw layer of Azure Data Lake Storage (ADLS). Moving forward, Azure Databricks takes the lead, refining the dataset and storing the processed data in ADLS’s transformed layer. Azure Synapse Analytics steps in, primarily for robust data warehousing and detailed analysis, allowing deeper exploration and insights. Finally, Power BI visualizes these insights, marking the completion of a step-by-step process and providing a rich and comprehensive view of the 2021 Olympics dataset.


##  technologies-used:
- **Github**: Host the Tokyo Olympic data as raw data.
- **Azure Data Factory**: Utilized for orchestration of data pipelines.
- **Azure Data Lake Storage Gen2**: Used for storing data.
- **Azure Databricks**: Employed for data analysis.
- **Azure Synapse Analytics**: Used for data warehousing.
- **Power BI**: Utilized for creating interactive dashboards.
  
## data-pipeline

  ![workflow of the project](https://github.com/Samiha128/tokyo-olympic-azure-project/assets/120471620/67fae82a-f2fc-443e-84eb-cbd170c70663)
  
####  1. Extract from GitHub Repository : Azure Data Factory is configured to extract the Tokyo Olympics data from a specified GitHub repository. This ensures that the most recent data is always available for subsequent processing. The extracted data is stored as raw data in Azure Data Lake Storage Gen2 (ADLS Gen2).

####  2. Load to Azure Data Lake Gen2 : The extracted data is loaded into Azure Data Lake Gen2 for storage. This raw data serves as the initial dataset for further transformations.

<img width="626" alt="data pipeline" src="https://github.com/Samiha128/tokyo-olympic-azure-project/assets/120471620/ae455cef-38df-465c-b6c5-86740c951634">


####  3. Transform Data with Azure Databricks : Azure Databricks, powered by PySpark, is used to perform data transformations. Data cleansing, enrichment, and preparation are done in Databricks notebooks to ensure the data is ready for analysis.

####  4. Load Transformed Data into Azure Data Lake Gen2 : After transformation, the processed data is stored back into Azure Data Lake Gen2 in a dedicated 'transformed data' container. This segregates raw and processed data for better organization

####  5. Load Data into Azure Synapse Analytics :  In Synapse, SQL queries can be applied to the data for further analysis and reporting. This step allows for efficient querying and reporting through data warehousing.

####  6. Create Dashboards with Power BI : Power BI is connected to Azure Synapse Analytics and loads the transformed data to create interactive dashboards. Power Query is used for additional data transformations within Power BI. These dashboards provide visual insights and facilitate data-driven decision-making.

## repository-structure


```
tokyo-olympic-azure-project
│   README.md
│
├── data
│   │   Athletes.csv
│   │   Coaches.csv
│   │   EntriesGender.csv
│   │   Medals.csv
│   │   Teams.csv
│
├── images
│   │   workflow of the project data pipeline.png
│   │   data-pipeline.png
│
└──  Tokyo Olympic Transformation.ipynb
```
## How to Run
- To execute this data pipeline, follow these steps:

## Azure Subscription: 
  Firstly, you need an Azure subscription. In our case, we used a student subscription which provides $100 free credit for students.

### Create Azure Resources:

  Azure Data Factory: Create an Azure Data Factory instance to orchestrate and automate data movement and transformation processes.
  Azure Data Lake Storage Gen2: Set up a Storage Account with Azure Data Lake Storage Gen2 to store both raw and transformed data securely.
  Azure Databricks: Create an Azure Databricks instance. During creation, ensure to configure a cluster in the compute zone within Databricks.
  Azure Synapse Analytics: Set up an instance of Azure Synapse Analytics (formerly SQL Data Warehouse) for data warehousing and SQL-based analytics.

### Install Power BI Desktop:

  Install Power BI Desktop for editing and viewing dashboards. Power BI will connect to Azure Synapse Analytics to visualize and analyze the transformed data.


# Dashboard
  

       






