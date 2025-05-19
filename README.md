This project demonstrates a compact example of an end-to-end data extraction and processing pipeline using Azure Databricks. It follows the Medallion Architecture to process earthquake data retrieved from a public API:

- Bronze Layer: Raw data is extracted directly from the earthquake API.

- Silver Layer: Basic cleaning is performed, including handling missing or unexpected values and standardizing column names.

- Gold Layer: More advanced transformations are applied. This includes creating new informative columns and using a reverse geocoder to append country codes based on longitude and latitude coordinates.

The entire pipeline is organized into a sequence of tasks that can be scheduled to run at regular intervals, ensuring that the (imaginary) organization receives up-to-date earthquake insights in near real time.

The data is stored in separate ADLS containers from a storage account, the entirety of the data processing and manipulation is done in pyspark.
