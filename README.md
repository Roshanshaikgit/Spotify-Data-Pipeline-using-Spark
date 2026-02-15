# Spotify-Data-Pipeline-using-Spark
The Spotify Data Pipeline is a scalable ETL workflow that ingests Spotify streaming data into Snowflake for analytics. It leverages AWS services for storage and automation, Python for extraction, and Apache Spark for distributed transformations.
🔹 Key Components
- Data Extraction
- Python scripts (running in AWS Lambda or other compute) connect to the Spotify API.
- Raw JSON data is ingested into Amazon S3 staging buckets.
- Data Transformation (Spark)
- Apache Spark processes raw JSON files from S3.
- Transformations include flattening nested structures, handling nulls, type casting, and enrichment.
- Spark jobs output clean, structured parquet/CSV files back into S3.
- Data Loading
- Snowpipe automatically ingests transformed files from S3 into Snowflake.
- Data is organized into stage, core, and mart layers for analytics.
- Data Modeling
- Fact tables (e.g., track plays) and dimension tables (songs, albums, artists) designed in Snowflake.
- Optimized schema supports efficient queries and BI dashboards
🔹 Features
- Distributed transformations with Spark → handles large datasets efficiently.
- Serverless ingestion → automated flow from API to warehouse.
- Scalable design → grows seamlessly with Spotify data volume.
- Analytics‑ready schema → supports dashboards, reporting, and recommendation systems.
