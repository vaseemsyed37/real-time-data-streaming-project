# data-warehouse-snowflake-for-data-engineering
data-warehouse-snowflake-for-data-engineering

## Screenshots


### Architecture Diagram
![Architecture](screenshots/architecture.png)


This project is designed to demonstrate the integration of several technologies to create a real-time data pipeline. The pipeline involves data generation, transformation, and loading into a target system, leveraging services such as AWS EC2, S3, Nifi, Jupyter Notebook, and Snowflake.

### Project Overview
The goal of this project is to automate the data streaming and processing workflow, starting from data generation (using Jupyter Notebook), moving to data transfer (via Nifi), and finally loading the data into a cloud-based data warehouse (Snowflake) for analytics.

The project sets up a real-time data pipeline with the following steps:

Data Generation: A Python script running in Jupyter Notebook generates a dataset with 10,000 rows.

Data Transfer: Apache Nifi is used to move the data into AWS S3.

Data Loading: The data is then loaded into Snowflake for further analysis and reporting.

### Use Case

The use case for this project is a scenario where we want to generate a fake dataset, transfer it to the cloud, and store it for further processing. The use case can be expanded to real-time data ingestion in various data-driven applications such as:

Customer analytics systems

Real-time reporting systems

Data lakes for big data analysis

### ELT Lifecycle

The ELT (Extract, Load, Transform) process in this project is broken down as follows:

## Extract:

Jupyter Notebook generates fake data using a Python script (faker library) and outputs the data in a CSV format.

## Load:

The data is loaded into AWS S3 using Apache Nifi. The data is transferred securely with the help of IAM roles and access keys.

## Transform:

The data is transformed once it is in Snowflake. Snowflake performs any necessary transformations (like data cleansing, aggregations) using SQL scripts, and stores it in staging or history tables.

### Visualize:

Finally, the transformed data can be used for analysis, reporting, and visualization. The data can be queried from Snowflake and integrated with BI tools for real-time insights.

### Tech Used

AWS EC2: Virtual servers to run the applications and manage infrastructure.

Jupyter Notebook: Python-based interactive environment for creating and testing data generation scripts.

Apache Nifi: Data ingestion tool for moving data from one system to another securely and efficiently.

AWS S3: Cloud storage service to store the raw and processed data.

Snowflake: Cloud data warehouse used to store, process, and analyze the data.

IAM: AWS Identity and Access Management for securely managing access to AWS resources.

Python: Scripting language used to generate fake data in Jupyter Notebook.




### Setup Instructions

Prerequisites

AWS Account: You’ll need an AWS account with access to EC2, S3, and IAM.

Snowflake Account: A Snowflake account is required for data loading and processing.

Jupyter Notebook: Python environment to run the script for generating fake data.

### Steps to Run

# Start EC2 Instance:

Launch an EC2 instance and set up the necessary environment for Python and Jupyter.

SSH into the instance to access the terminal.

# Run Data Generation Script:

Use Jupyter Notebook to execute the Python script (faker.ipynb) to generate the fake data.

# Set Up Apache Nifi:

Configure Apache Nifi to fetch the data and load it into S3 using proper IAM credentials.

# Load Data into Snowflake:

Set up Snowflake for receiving the data.

Create staging tables, and load the raw data into these tables.

# Monitor and Analyze:

Once data is loaded into Snowflake, you can query it for analysis or integrate it with BI tools.

### Conclusion
This project demonstrates how to integrate multiple services and technologies for real-time data processing. By automating the data pipeline from generation to storage, we can achieve seamless data flow and faster decision-making. The project can be extended to handle real-time streams and large-scale datasets.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

