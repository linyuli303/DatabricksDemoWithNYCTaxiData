# Databricks Demo Project with NYC Taxi Data


**Project description:**

Developed data transformation workflows in **Unity Catalog** using managed Delta tables, following the **medallion architecture** (bronze, silver, and gold layers) with **PySpark** in **Databricks**.

Notebooks are incorporated into pipelines and jobs to support incremental updates by employing **Slowly Changing Dimension Type 2** and append mode.

During the initial one-time setup, data for the first seven months of 2026 is dynamically downloaded via variables. Subsequent transformation steps append only the latest month's data using append mode.



**How to run the notebooks:**

If you are interested in the codes. Make sure you run them in the right order:

**[one_off]**

creating_catalog_schemas_volume.ipynb

**[one_off/initial_load/notebooks/]**

**00_landing**

  - backfill_historical_yellow_taxi_trips.ipynb
  
  - load_taxi_zone_lookup.ipynb
  
**01_bronze**

  - yellow_trips_raw.ipynb
  
**02_silver**

  - taxi_zone_lookup.ipynb
  
  - yellow_trips_cleansed.ipynb
  
  - yellow_trips_enriched.ipynb
  
**03_gold**

  - daily_trip_summary.ipynb

**[transformations/notebooks/]** 

00_landing

  - ingest_lookup.ipynb
  
  - ingest_yellow_trips.ipynb
  
01_bronze

  - yellow_trips_raw.ipynb
  
02_silver

  - taxi_zone_lookup.ipynb **(SCD Type 2)**
  
  - yellow_trips_cleansed.ipynb
  
  - yellow_trips_enriched.ipynb
  
03_gold

  - daily_trip_summary.ipynb
    

**Data Source:**

https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

The dataset is published monthly on the official website, typically with a two-month delay to accommodate complete submissions from vendors.

