# Databricks Demo Project with NYC Taxi Data


**Project description:**

Developed data transformation workflows in **Unity Catalog** using managed Delta tables, following the **medallion architecture** (bronze, silver, and gold layers) with **PySpark** in **Databricks**.

Notebooks are incorporated into pipelines and jobs to support incremental updates by employing **Slowly Changing Dimension Type 2** and append mode.

During the initial one-time setup, data for the first seven months of 2026 is dynamically downloaded via variables. Subsequent transformation steps append only the latest month's data using append mode.


**Data Source:**

https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

The dataset is published monthly on the official website, typically with a two-month delay to accommodate complete submissions from vendors.

