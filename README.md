# 🚀 ETL Pipeline using AWS S3, Glue Studio & Athena

## 📌 Project Overview
This project demonstrates a complete ETL (Extract, Transform, Load) pipeline using AWS services.

The pipeline extracts raw CSV data from Amazon S3, transforms it using AWS Glue, and loads the processed data (Parquet format) back into S3 for efficient querying using Amazon Athena.

---

## 🏗️ Architecture
S3 (Raw Data) → Glue ETL → S3 (Processed Data) → Athena

---

## 📂 Step 1: S3 Buckets (Input & Output)

- Raw Data Bucket (CSV files)
- Processed Data Bucket (Parquet files)

![S3 Buckets](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/s3-buckets.png)

---

## 📊 Step 2: Raw Data Table (AWS Glue)

- Schema automatically detected

![Glue Table](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/glue-table.png)

---

## 🔄 Step 3: Glue ETL Job (Visual Flow)

- Source → Glue Data Catalog
- Target → S3

![Glue ETL](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/glue-etl.png)

---

## ✅ Step 4: Job Execution

- Status: **SUCCEEDED**

![Job Success](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/job-success.png)

---

## 📦 Step 5: Processed Data in S3

- Parquet format output
- `_SUCCESS` file present

![Processed Data](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/processed-data.png)

---

## 🔍 Step 6: Glue Crawler

- Updated schema for processed data

![Crawler](https://raw.githubusercontent.com/BHARGAVI200430/ETL-Pipeline-using-AWS-S3-Glue-Studio-Athena-project/main/assets/crawler.png)

---

## 🧠 Step 7: Athena Query

```sql
SELECT * 
FROM etl_project_processed_data2 
LIMIT 10;
