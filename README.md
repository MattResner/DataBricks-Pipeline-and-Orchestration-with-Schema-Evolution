# Databricks Pipeline with Schema Evolution and Medallion Architecture

This project demonstrates the development of a robust data pipeline in Databricks with simulated data from Trader Joes Stores, focusing on schema evolution and efficient data orchestration. The pipeline processes data through a typical multi hop architecture with stages—Bronze, Silver, and Gold—ensuring data quality and facilitating analytics with one source of truth (rather than many downstream semantic models).

## Project Structure

1. **Database Configuration**:
   - Sets up the initial database environment, defining schemas and preparing the workspace for data ingestion.

2. **Bronze Fact Pipeline**:
   - Handles the ingestion of raw data into Bronze tables, implementing schema enforcement to manage evolving data structures.

3. **Silver Fact Pipeline**:
   - Processes data from Bronze tables, performing cleansing and transformations to create refined Silver tables.

4. **Gold Fact Pipeline**:
   - Aggregates and further refines Silver data into Gold tables, optimized for reporting and analytics.

5. **Reporting Queries**:
   - Executes analytical queries on Gold tables to generate insights and support business intelligence needs.

6. **Delta Log History**:
   - Explores Delta Lake's transaction log to monitor data changes, ensuring data integrity and facilitating auditing of landed files and extracts data for schema evolution.

7. **Cleanup**:
   - Provides scripts to clean up resources, maintaining an organized and efficient workspace.

## Key Features

- **Schema Evolution Management**:
  - Utilizes Delta Lake's capabilities to handle changes in data schema seamlessly, ensuring the pipeline adapts to new data structures without manual intervention (when required data is present for subsequesent transformation).

- **Data Orchestration**:
  - Modules Permit Databricks workflows to automate the progression of data through various pipeline stages, enhancing efficiency and reliability. 

- **Data Quality Assurance**:
  - Implements validation and transformation steps to maintain high data quality across all pipeline stages.

## Getting Started

To explore and run this project:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/MattResner/DataBricks-Pipeline-and-Orchestration-with-Schema-Evolution.git
   ```

2. **Set Up Databricks Environment**:
   - Access your Databricks workspace.
   - Create a new cluster with the necessary configurations.

3. **Import Notebooks**:
   - Upload the project notebooks into your Databricks workspace.

4. **Execute Notebooks Sequentially**:
   - Begin with the Database Configuration notebook and proceed through the pipeline stages in order.

## References

- [Diving Into Delta Lake: Schema Enforcement & Evolution](https://www.databricks.com/blog/2019/09/24/diving-into-delta-lake-schema-enforcement-evolution.html)
- [Schedule and Orchestrate Workflows - Azure Databricks](https://learn.microsoft.com/en-us/azure/databricks/jobs/)

This project serves as a practical example of building a scalable and adaptable data pipeline in Databricks, leveraging schema evolution and orchestration features to maintain data integrity and support advanced analytics. 
