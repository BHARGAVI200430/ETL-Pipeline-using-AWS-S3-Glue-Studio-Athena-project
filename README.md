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

![S3 Buckets] <img width="2209" height="1099" alt="image" src="https://github.com/user-attachments/assets/b331de65-5205-4bc6-8401-88609919b430" />


---

## 📊 Step 2: Raw Data Table (AWS Glue)

- Schema automatically detected

![Glue Table] <img width="2184" height="1102" alt="image" src="https://github.com/user-attachments/assets/74f88710-72d0-4e2a-aa47-cb6b6de8164e" />
<img width="1167" height="733" alt="image" src="https://github.com/user-attachments/assets/0f76d85a-8444-4c30-9f5f-6a1971c5e192" />



---

## 🔄 Step 3: Glue ETL Job (Visual Flow)

- Source → Glue Data Catalog
- Target → S3

![Glue ETL] <img width="1692" height="776" alt="image" src="https://github.com/user-attachments/assets/170f14fd-7e0f-4cb8-a4a5-0465f2c4fd0d" />
<img width="1167" height="726" alt="image" src="https://github.com/user-attachments/assets/8ff69c73-cdcc-40c4-9480-77dc3026d5f7" />




---

## ✅ Step 4: Job Execution

- Status: **SUCCEEDED**

![Job Success] <img width="1714" height="1024" alt="image" src="https://github.com/user-attachments/assets/cb374764-20ac-44ee-aa67-980ac55540ce" />


---

## 📦 Step 5: Processed Data in S3

- Parquet format output
- `_SUCCESS` file present

![Processed Data] <img width="1781" height="1096" alt="image" src="https://github.com/user-attachments/assets/c9d3ec2e-8b6b-4fbd-b58b-f0cf8e0ca94f" />


---

## 🔍 Step 6: Glue Crawler

- Updated schema for processed data

![Crawler] <img width="1666" height="1013" alt="image" src="https://github.com/user-attachments/assets/ef53f253-a140-46a5-9675-e9d3e9e283fc" />


---

## 🧠 Step 7: Athena Query
<img width="1964" height="1093" alt="image" src="https://github.com/user-attachments/assets/b2710192-43f0-46d1-a18a-58977bf51722" />
<img width="1172" height="736" alt="image" src="https://github.com/user-attachments/assets/72c793a0-3ec9-4c17-beab-4b1bd5054b28" />



