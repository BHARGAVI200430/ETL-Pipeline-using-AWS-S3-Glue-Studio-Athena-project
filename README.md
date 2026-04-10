# 🚀 ETL Pipeline using AWS S3, Glue Studio & Athena

## 📌 Project Overview
This project demonstrates a complete ETL (Extract, Transform, Load) pipeline using AWS services:

- Amazon S3 (Storage)
- AWS Glue (ETL Processing)
- AWS Athena (Querying)

The pipeline takes raw CSV data, processes it using Glue, and stores it as Parquet for efficient querying.

---

## 🏗️ Architecture
S3 (Raw Data) → Glue ETL → S3 (Processed Data) → Athena Query

---

## 📂 Step 1: S3 Buckets (Input & Output)

- Raw data stored in CSV format
- Processed data stored in Parquet format

![S3 Buckets](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/s3-buckets.png)

---

## 📊 Step 2: Raw Data Table (Glue Data Catalog)

- Glue detects schema automatically
- Table created from raw S3 data

![Glue Table](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/glue-table.png)

---

## 🔄 Step 3: Glue ETL Job (Visual Flow)

- Source: Glue Data Catalog
- Target: S3 Bucket
- Transformation handled in Glue Studio

![Glue ETL Job](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/glue-etl.png)

---

## ✅ Step 4: Job Run Success

- ETL job executed successfully
- Status: SUCCEEDED

![Job Success](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/job-success.png)

---

## 📦 Step 5: Processed Data in S3

- Output stored in Parquet format
- `_SUCCESS` file confirms pipeline completion

![Processed Data](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/processed-data.png)

---

## 🔍 Step 6: Glue Crawler

- Crawler updates schema for processed data
- Status: READY / SUCCEEDED

![Crawler](https://github.com/YOUR_USERNAME/YOUR_REPO/assets/crawler.png)

---

## 🧠 Step 7: Athena Query (Final Output)

```sql
SELECT * 
FROM etl_project_processed_data2 
LIMIT 10;
