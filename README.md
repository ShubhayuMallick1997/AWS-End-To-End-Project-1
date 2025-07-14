
---

# 🔴 **AWS End-to-End Project Execution | Retail Domain | S3 + Glue + Athena | CSV, Parquet, JSON**

Welcome to this hands-on **AWS Big Data Project Execution** where we build a **complete data pipeline in the Retail domain** using **Amazon S3, AWS Glue Visual Editor, and Amazon Athena** — all **without writing a single line of code!**

🚀 **Project Overview:**

In this mini end-to-end project, we demonstrate how to process **Retail domain data** from raw ingestion to structured querying using AWS analytics services.

🔹 **Source Files:**

* `customer_data.csv`
* `sales_data.csv`
  Both files are uploaded into the **raw folder of an S3 bucket**.

🔹 **Step-by-Step Execution:**

1. **Upload Raw Data** to S3 in `.csv` format.
2. **Create an AWS Glue ETL Job** using **Glue Visual Editor**.
3. **Read Source Data from S3** (Customer + Sales).
4. **Apply Transformations**:

   * Join on customer ID
   * Remove **nulls** and **duplicate records**
5. **Write Cleaned Output** to **S3 Destination Folder** in:

   * `CSV`
   * `Parquet`
   * `JSON`
6. **Partitioning** the data on **2 levels**:

   * `country`
   * `sales_date`
7. **Create Glue Database** and connect to **Athena**.
8. **Create External Table in Athena** on the **Parquet folder** with partition projection.
9. **Run SQL Queries in Athena** for validation and analytics.

📂 **Output Structure:**

```
s3://your-bucket-name/cleaned-data/
    ├── parquet/   (partitioned by country/sales_date)
    ├── json/
    └── csv/
```

🎯 **What You'll Learn:**

* AWS Glue Visual Editor for no-code ETL
* Handling multiple data formats: CSV, Parquet, JSON
* Partitioning strategies in Glue + Athena
* Creating External Tables in Athena
* Real-world transformation logic with join, deduplication, null removal
* Retail domain use case data flow



