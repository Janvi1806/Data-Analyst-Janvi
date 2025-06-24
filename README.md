# Data-Analyst-Janvi

# Project title – Descriptive Analysis of Operating Permits for water systems in the City of Vancouver!

# Objective

The primary goal of this project is to analyze the issued operating permits for water systems across Vancouver using AWS services. The project seeks to understand the permit distribution, assess data quality, and develop a scalable analytics pipeline that ensures security, governance, and visibility.

# Dataset Selection

For my part, I chose the ‘Issued Operating Permits – water systems’ dataset from –
https://opendata.vancouver.ca/explore/dataset/issued-operating-permits-water-systems-/analyze/?dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJ5QXhpcyI6InR1cmJpZGl0eSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6InJhbmdlLWN1c3RvbSJ9XSwieEF4aXMiOiJjdXJyZW50X3N5c3RlbV9zdGF0dXMiLCJtYXhwb2ludHMiOm51bGwsInRpbWVzY2FsZSI6IiIsInNvcnQiOiIiLCJjb25maWciOnsiZGF0YXNldCI6Imlzc3VlZC1vcGVyYXRpbmctcGVybWl0cy13YXRlci1zeXN0ZW1zLSIsIm9wdGlvbnMiOnt9fSwic2VyaWVzQnJlYWtkb3duIjoibWVjaGFuaWNhbF9zeXN0ZW1fdHlwZSJ9XSwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZSwidGltZXNjYWxlIjoiIn0%3D

# Descriptive Analysis

The primary goal of this project is to analyze the issued operating permits for water systems across Vancouver using AWS services. The project seeks to understand the permit distribution, assess data quality, and develop a scalable analytics pipeline that ensures security, governance, and visibility.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/9fee48cf-fed2-4e22-bdd3-d3c682b36f25" />

# Dataset

The dataset was sourced from the City of Vancouver Open Data Portal. It includes 1,243 records with attributes such as:

•	Operating Permit Number

•	Address & Geolocation

•	Mechanical System Type

•	Current System Status

•	Contaminant Indicators (e.g., Benzene, E. coli)

•	Permit Renewal Date

# Business Question

“What percentage of total permits are issued for cooling towers?”
-	Out of 1,243 total permits, 373 are for cooling towers, 29.99% of all permits.

#Draw io representation

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/e8e7c108-4c75-4758-8851-8141d23ad388" />

This diagram represents the AWS Data Analytics Pipeline designed for the project. It includes Amazon S3 for storage, AWS Glue for ETL, DataBrew for profiling and cleaning, and Athena for querying, with outputs visualized through QuickSight or stored in curated buckets.

# Methodology

# 1. Data Ingestion

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/d11c0501-2d37-4649-a39b-c0a0752822a4" />

This image shows the raw dataset stored in S3, confirming the initial ingestion step of the pipeline. S3 ensures scalable and durable data storage.

# 2. Data Profiling 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/36061089-113e-4cd4-baa3-3136a169b8e0" />

The screenshot demonstrates the DataBrew profiling results, highlighting null percentages and column statistics. This helped identify data quality gaps before processing.

# 3. Data Cleaning

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/48ac7b20-6959-4e0b-9591-b645d347ed10" />

This image captures the cleaned dataset pipeline in Glue DataBrew. It reflects the column transformations and the transition to the clean storage tier.

# 4. Data Cataloging 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/2c12651d-b839-4baa-9ce1-8b7704ee807f" />

This shows the Glue visual pipeline with a step-by-step ETL flow for summarization. It aggregates data and routes the cleaned output to the curated layer.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/69f3a09d-dae9-4eee-a5d7-4c164bc1c35b" />

# 5. Data Security 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/888def5e-a30b-4a97-b4e5-a661590aaa07" />

The screenshots show the KMS key creation and its application to the S3 buckets. Encryption and versioning settings are crucial for ensuring data confidentiality and availability.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/ddcf1159-be9d-4610-9c9f-5b42f00c9fa2" />

Replication rules were configured in Amazon S3 to automatically duplicate all objects from the raw, clean, and curated buckets to designated backup buckets. This setup ensures high availability and disaster recovery by maintaining a copy of the data in a separate location.

# 6. Data Governance 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/4067a19a-be60-4a4e-a31d-8795081f12bd" />

The image displays the quality check pipeline with row-level outcomes and conditional routing. This ensures only valid data proceeds to downstream analysis.

# 7. Data Monitoring 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/4f1a7777-e210-44e4-9a1b-5001e3c16022" />

This shows a CloudWatch dashboard tracking Glue job usage and S3 growth. CloudTrail logs complement this by recording detailed access activity for auditing.

# Conclusion 

This project successfully demonstrated how to leverage AWS cloud services to ingest, process, secure, and analyze operational permit data for water systems in the City of Vancouver. Through the use of tools like AWS Glue, S3, KMS, and CloudWatch, we created a scalable and reliable data analytics pipeline. The results offer valuable insights—such as cooling towers accounting for nearly 30% of issued permits—enabling better regulatory planning and resource allocation by the city.













