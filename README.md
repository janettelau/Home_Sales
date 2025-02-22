# Home_Sales

## Overview
The objective of this project is to analyze home sales data using SparkSQL to determine average home prices based on different filters. This project involves performing SQL queries, creating temporary views, and optimizing queries for performance through techniques like caching and partitioning the data using PySpark.

## Setup and Usage
1. Clone this repository to your local machine using `git clone`.
2. To run the initial model, create a new notebook on [Google Colab](https://colab.research.google.com/) then upload the Jupyter Notebook `Home_Sales.ipynb` from your local repository.
3. Check the latest version of Spark and modify the `spark_version` at the beginning of the notebook if needed.
4. Run each cell sequentially to load the data and perform SQL queries for data analysis.

## Methodology Breakdown
* Data Loading
  * Read the `home_sales_revised.csv` file into a PySpark DataFrame and create a local temporary view.
* Perform SQL Queries and Analysis
  * Perform queries to calculate average home prices based on the sizes of homes and the number of bedrooms and bathrooms. 
* Caching and Uncaching in Spark
  * Cache the temporary table `home_sales` to speed up subsequent queries by storing the data in memory.
* Partitioning Parquet Data 
  * Partition the formatted Parquet data `home_sales_partitioned` to reduce memory requirements and the runtime of queries.

## Runtime Comparison
| Query Type          | Runtime (seconds) |
|---------------------|-------------------|
| Uncached            | 1.309             |
| Cached              | 0.578             | 
| Partitioned Parquet | 1.039             |

The above results suggest that caching provides the best optimization for repeated queries in this case, followed by partitioning the Parquet data, which still improves the query runtime compared to the uncached version.
