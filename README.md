# BookPublisherDistributionDB Analytics Platform

I developed the **BookPublisherDistributionDB Analytics Platform** to streamline the data ingestion, transformation, and analytics workflows for a book distribution company. This project leverages Azure services like Azure Data Factory, Azure Data Lake Storage, and Azure Synapse Analytics to create an automated, end-to-end data solution.

## Table of Contents
1. [Overview](#overview)
2. [Project Architecture](#project-architecture)
3. [Technologies Used](#technologies-used)
4. [Setup and Configuration](#setup-and-configuration)
5. [Data Ingestion Pipeline](#data-ingestion-pipeline)
6. [Data Transformation & Processing](#data-transformation--processing)
7. [Automating the Pipeline](#automating-the-pipeline)
8. [Screenshots](#screenshots)

---

### Overview
This platform supports automated ingestion, scalable storage, and analytical insights for book distribution data. It is designed for a real-world environment where data comes from multiple sources and requires both efficient storage and robust transformation processes.

### Project Architecture
- **Data Ingestion**: Uses Azure Data Factory to import data into Azure Data Lake.
- **Data Storage**: Azure Data Lake Storage for raw and processed data.
- **Data Transformation**: Azure Synapse Analytics for processing, querying, and visualizing data.
- **Orchestration**: Automated pipeline scheduling and monitoring in Azure Data Factory.

### Technologies Used
- Azure Data Factory
- Azure Data Lake Storage
- Azure Synapse Analytics
- Azure SQL Database
- PowerShell
- GitHub

---

### Setup and Configuration

#### 1. **Create Storage Resources**
   - **Step 1**: Log in to the [Azure Portal](https://portal.azure.com).
   - **Step 2**: Search for "Storage Account" and click **+ Create**.
   - **Step 3**: Set up your storage account and create a Blob container named `raw-data`.
   - ![Storage account creation](images\Storage account creation.png)

#### 2. **Set Up Azure Data Factory**
   - **Step 1**: Search for "Data Factory" in the Azure Portal and click **+ Create**.
   - **Step 2**: Name your Data Factory instance and configure for your region.
   - **Step 3**: Open **Azure Data Factory Studio** to manage pipelines and datasets.
   - ![Data Factory Setup](images\Data Factory Setup.png)

#### 3. **Create Synapse Analytics SQL Pool**
   - **Step 1**: Open **Azure Synapse Analytics** and create a new SQL pool.
   - **Step 2**: Name and configure your SQL pool as per your project needs.
   - ![SQL Pool Creation](images\sql pool created.png)

---

### Data Ingestion Pipeline

#### 1. **Create a New Pipeline for Data Ingestion**
   - **Step 1**: In Azure Data Factory Studio, go to the **Author** section.
   - **Step 2**: Click **+ New Pipeline** and name it `IngestSampleDataPipeline`.
   - ![Pipeline Creation](images\Pipeline Creation.png)

#### 2. **Configure Source & Sink Datasets**
   - **Step 1**: Define the **Source Dataset** pointing to the `raw-data` container.
   - **Step 2**: Configure the **Sink Dataset** to store data in the `processed-data` container.
   - ![Source & Sink Dataset Configuration](C:\Users\Sairam\Azure Data analytics\Source & Sink Dataset Configuration.png)
   - ![Source & Sink Dataset Configuration2](images\Source & Sink Dataset Configuration2.png)

#### 3. **Add Copy Data Activity**
   - **Step 1**: Drag the **Copy Data** activity to the main pipeline canvas.
   - **Step 2**: Configure connections between Source Dataset and Sink Dataset.
   - ![Copy Data Activity Setup](images\Copy Data Activity Setup.png)

#### 4. **Run the Pipeline**
   - **Step 1**: Use **Debug** to test your pipeline.
   - **Step 2**: Go to **Trigger > Trigger Now** to run the pipeline completely.
   - ![Pipeline Run in Monitor](images\PipelineRun in Monitor.png)

---

### Data Transformation & Processing

1. **Data Transformation in Synapse Analytics** *(optional)*:
   - **Step 1**: Go to Synapse Studio > Develop > Data Flow.
   - **Step 2**: Configure transformations for ingested data as needed.
   - ![Synapse Analytics](images\synapse analytics.png)

2. **Load Data into Azure SQL Database** *(optional)*:
   - **Step 1**: Use **Copy Activity** to load transformed data into SQL Database for advanced analytics.

---

### Automating the Pipeline

1. **Create Scheduled Triggers**:
   - **Step 1**: In Data Factory Studio, go to **Manage** > **Triggers**.
   - **Step 2**: Set up a new trigger with a specified schedule for pipeline automation.
   - ![Data Factory Validation](images\data factory validation.png)

---

### Screenshots

Screenshots referenced in each section show the actual steps taken in this project for setup, configuration, and pipeline execution. These are found in the project’s **Azure Data Analytics** folder.

- **Storage Account Creation** ![Storage Account Setup](images\Storage Account Setup.png)
- **Data Factory Setup** ![Data Factory Setup](images\Data Factory Setup.png)
- **SQL Pool Created** ![SQL Pool Created](images\sql pool created.png)
- **Source & Sink Dataset Configuration** ![Source & Sink Dataset Configuration](images\Source & Sink Dataset Configuration.png)
- **Pipeline Run in Monitor** ![PipelineRun in Monitor](images\PipelineRun in Monitor.png)
- **Copy Data Activity Setup** ![Copy Data Activity Setup](images\Copy Data Activity Setup.png)
- **Synapse Analytics Setup** ![Synapse Analytics](images\synapse analytics.png)

---

### Conclusion
This project demonstrates how Azure Data Factory, Data Lake, and Synapse Analytics work together for scalable data ingestion and transformation in a real-world book distribution context. 

--- 


