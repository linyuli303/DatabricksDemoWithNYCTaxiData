# Databricks Demo Project With NYCTaxi Data

Data Source: 
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Developed data transformation workflows in Unity Catalog using managed Delta tables following the medallion architecture (bronze, silver, and gold layers). 

Notebooks are incorporated into pipelines and jobs to support incremental updates employing Slowly Changing Dimension Type 2 and append mode.

During the initial one-time setup, data for the first seven months of 2026 is dynamically downloaded via variables. Subsequent transformation steps append only the latest month’s data using append mode.

The dataset is published monthly on the official website, usually with a two-month delay to accommodate complete submissions from vendors.
