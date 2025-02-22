# Home_Sales

## Overview

## Setup and Usage
1. Clone this repository to your local machine using `git clone`.
2. To run the initial model, create a new notebook on [Google Colab](https://colab.research.google.com/) then upload the Jupyter Notebook `Home_Sales.ipynb` from your local repository.
3. Make sure to double check the latest version of Spark and modify the `spark_version` at the beginning of the notebook if needed.
4. Run each cell sequentially to load the data and perform SQL queries for data analysis.

## Methodology Breakdown
* Data Loading
  * Read the `home_sales_revised.csv` file into a PySpark DataFrame and create a temporary view.
* Perform SQL Queries and Analysis
  *  Perform queries to calculate average home prices based on the sizes and number of the bedrooms and bathrooms. 
* Caching in Spark for Optimization
  * 
* Partitioning Data
  * 
