# Building a Cricket Statistics Pipeline with Google Cloud Services

In the world of data engineering, the journey from data retrieval to insightful visualization is an adventure filled with challenges and rewards. In this guide, we’ll walk through the intricate steps of constructing a comprehensive cricket statistics pipeline using Google Cloud services. From retrieving data via the Cricbuzz API to crafting a dynamic Looker Studio dashboard, each phase contributes to the seamless flow of data for analysis and visualization.

### Architecture

![Architecture](https://github.com/vishal-bulbule/cricket-stat-data-engineering-project/blob/master/Architecture.png)

## Data Pipeline for Cricket Statistics: From API to Visual Dashboard
### 1. Data Retrieval with Python and the Cricbuzz API
The project begins by leveraging Python's robust capabilities to interface with the Cricbuzz API. We will explore efficient methods for retrieving detailed cricket statistics, ensuring data accuracy and timeliness. Python's libraries, such as requests and json, will facilitate seamless API communication, fetching the necessary data in real-time or on-demand.

### 2. Storing Data in Google Cloud Storage (GCS)
Once the cricket data is retrieved, the next step is to securely store it in the cloud. We will store the data in a structured CSV format within Google Cloud Storage (GCS), providing scalability and easy access for future use. Using the google-cloud-storage Python library, we’ll automate the process of saving and managing files in GCS, making sure the pipeline is reliable and efficient.

### 3. Creating a Cloud Function Trigger
To automate the data pipeline, we will configure a Google Cloud Function that triggers upon file uploads to a designated GCS bucket. This serverless function serves as the entry point for the next stages of data processing, reacting instantly to the presence of new data and minimizing latency in the workflow.

### 4. Executing the Cloud Function
Once triggered, the Cloud Function will contain custom logic to start a Dataflow job. It will pass necessary parameters such as the file path, ensuring a smooth transition to the data processing stage. This function is crucial for orchestrating the pipeline, as it ensures that all processes downstream are initiated automatically and accurately.

### 5. Dataflow Job for BigQuery Ingestion
At the core of our pipeline is the Dataflow job, which handles the transformation and loading of data from the CSV file in GCS to Google BigQuery. Dataflow will process the data, applying any required transformations or aggregations, and then ingest the data into BigQuery. Proper configuration of the job’s settings will ensure efficient data handling and loading, optimized for performance and scale.

### 6. Building a Looker Studio Dashboard
To complete the pipeline, we will visualize the cricket data using Looker Studio. By configuring BigQuery as a data source, we can create dynamic, visually compelling dashboards. These dashboards will provide powerful insights into the cricket statistics, allowing users to interact with and analyze the data in real-time. The visualization will serve as the final step, bringing data to life for stakeholders.


![Looker](https://github.com/vishal-bulbule/cricket-stat-data-engineering-project/blob/master/Looker.png)
