# Comprehensive Data Pipeline

This project implements a comprehensive data pipeline to process and analyze large datasets, leveraging Azure services for data ingestion, transformation, and visualization. It is designed to integrate data from diverse sources, ensuring high-quality outputs for analytics and insights.

## Project Overview

### Key Features
- **Complex Workflow Handling**: Cloud-based pipelines enable scalable and robust data processing.
- **Data Quality Assurance**: Medallion architecture ensures data accuracy and reliability.
- **Data Extraction**: Retrieves data from Azure-managed SQL Database for processing.
- **Analysis Efficiency**: Loads essential, high-quality data for visualization, minimizing overhead.

### Benefits of Azure Services
- **Seamless Connectivity**: Integrates data from diverse sources.
- **Efficient Orchestration**: Automated workflows with Azure Data Factory.
- **High Availability**: Durable and reliable pipeline performance.

---
![Azure Diagram Architecture](https://github.com/Tramnddle/WaterQualityDatapipelineAzureMedalionArchitect/blob/1d907f74dc72a5b5a99ecaa85c67c1945bd7349e/Medalion%20Architecture.png)
## Pipeline Flow

1. **Data Extraction**: Azure Logic App pulls data from an Azure-managed SQL Database.
2. **Raw Data Storage**: Raw data is stored in Azure Blob Storage and structured in ADLS Gen2.
3. **Orchestration**: Data is moved from Blob Storage to ADLS Gen2 using Azure Data Factory.
4. **Data Transformation**: Medallion architecture transforms data into Bronze (raw), Silver (cleaned), and Gold (ready-to-use) layers.
5. **Visualization**: Power BI visualizes the processed data for actionable insights.

---

## Data Description

### Dataset Overview
- **Size**: Over 1 million rows, 32 columns.
- **Features**:
  - Country and water body categories.
  - Determinands information (concentration levels, timestamps).
  - Quality samples (conducted vs. total).

### Notes
Each data point is tied to a specific country and monitoring site, providing detailed insights into water quality across Europe.

---

## How to Use

### Prerequisites
- **Azure Account**: Access to services like SQL Database, Blob Storage, Data Factory, and Power BI.
- **Development Environment**: Python and Power BI installed locally.

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/data-pipeline.git
   cd data-pipeline
