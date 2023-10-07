# Uber-Data Engineering Project in GCP cloud using mage.ai ETL orchestration tool

## Introduction
The primary goal of this work is to build end to end pipeline for collecting data either through API from various sources or from google cloud storage. Further using GCP compuute instance (Virtual Machine for computing) and mage.ai( an ETL orchestration tool) to load data in GCP BigQuery. For the data modelling part, A star schema was built to make connection between fact and dimension tables. SQL query was developed to further organise the data set for the analytics team. Looker studio, a data visualisation tool , was used to see the patterns and trend in the data set.


## Architecture 
<img src="architecture.jpg">

## Technology Used
A.) Programming Language - Python for initial developement

B.) Google Cloud Platform
  1. Google Storage: for storing the data set
  2. Compute Instance: VM used to compute
  3. BigQuery: Data warehouse whcih will be used by analytics team for further analysis
  4. Looker Studio: Data visualisation for reporting and insights

C.) Modern Data Pipeine Tool -mage.ai 
    Reference:
  1. https://www.mage.ai/
  2. https://arunrnair.hashnode.dev/mageai-vs-apache-airflow)
  3. Contibute to this open source project - https://github.com/mage-ai/mage-ai


## Dataset Used
TLC Trip Record Data
Yellow and green taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. 

Here is the dataset used in the video -https://github.com/RNGNITC/Uber-End-to-End-data-engineering-ETL-pipeline-mage.ai-orchestration-GCP-cloud/blob/main/uber_data.csv

More info about dataset can be found here:
1. Website - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
2. Data Dictionary - https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Data Model
<img src="data_model.jpeg">![data_modelling_star_schema](https://github.com/RNGNITC/Uber-End-to-End-data-engineering-ETL-pipeline-mage.ai-orchestration-GCP-cloud/assets/125100033/38ca157f-5943-4e11-9310-48553e342f01)


## how does mage ai works:
1. we can use mage ai (which is modern orchestrtaion tool for ETL task)
2. as data is available on cloud storage and can be accessed through API. mage ai have blcok of function for each task (extract, load, transform). with url we can access data for transformation and next process. then loading all data set on biq query.
3. click on data exporter>python/sql/R>bigquery(choose location under same tab). You wokd get the data exporter code. We will be needing google service key and API key (for that go to GCP API and srvices and clikc on credentials
