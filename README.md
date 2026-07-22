# AWS AI Data Engineering Pipeline using Amazon S3, AWS Glue & SageMaker

## Project Overview

This project demonstrates an end-to-end AI-ready data engineering pipeline built on AWS using the UCI Bank Marketing dataset.

The objective is to ingest a public dataset, prepare it for machine learning, generate metadata and audit artifacts, catalog it using AWS Glue, perform exploratory data profiling, create AI-ready labels, and produce a reusable dataset for downstream ML workflows.

This project was implemented as part of the BITS Pilani AI Engineering Program using real AWS services.

---

# Architecture Diagram

                 UCI Bank Marketing Dataset
                           │
                           ▼
                    Download Dataset
                           │
                           ▼
                     Amazon S3 (Raw)
                           │
          ┌────────────────┴───────────────┐
          │                                │
          ▼                                ▼
     Manifest JSON                 Data Profile
          │                                │
          └──────────────┬─────────────────┘
                         ▼
                  AWS Glue Crawler
                         │
                         ▼
                 Glue Data Catalog
                         │
                         ▼
                  AWS Athena Queries
                         │
                         ▼
              Label Engineering (Python)
                         │
                         ▼
                 Curated AI Dataset
                         │
                         ▼
                  Label Audit & Data Card

---

# Project Workflow

```
                UCI Bank Marketing Dataset
                           │
                           ▼
                  Data Collection (Python)
                           │
                           ▼
                  Amazon S3 (Raw Layer)
                           │
                           ▼
               Metadata & Version Manifest
                           │
                           ▼
                 AWS Glue Crawler
                           │
                           ▼
                 AWS Glue Data Catalog
                           │
                           ▼
                 Data Profiling & Validation
                           │
                           ▼
              Feature Engineering & Labeling
                           │
                           ▼
              Curated AI-ready Dataset (Parquet)
                           │
                           ▼
             Audit Reports & Data Card Generation
```

---

# AWS Services Used

- Amazon S3
- AWS Glue Crawlers
- AWS Glue Data Catalog
- AWS Glue ETL
- AWS IAM
- Amazon Athena
- Amazon SageMaker Studio
- AWS CloudWatch (Glue execution logs)

---

# Technologies

- Python
- Pandas
- PyArrow
- Boto3
- JSON
- Parquet
- Jupyter Notebook

---

# Dataset

**Dataset Name**

UCI Bank Marketing Dataset

Dataset Source

https://archive.ics.uci.edu/ml/datasets/bank+marketing

Dataset contains customer marketing campaign information used to predict whether a customer subscribes to a term deposit.

---

# Project Features

✔ Automated dataset ingestion

✔ Data versioning

✔ Schema generation

✔ Metadata manifest creation

✔ S3 data lake organization

✔ Data profiling

✔ Feature engineering

✔ Label engineering

✔ Glue Data Catalog

✔ Glue Crawlers

✔ Athena-ready metadata

✔ AI-ready Parquet dataset

✔ Data Card generation

---

# Folder Structure

```
Session-2
│
├── README.md
├── aws_ai_data_engineering_pipeline.ipynb
│
├── architecture
│     └── session2_architecture.png
│
├── screenshots
│     ├── 01_s3_bucket_structure.png
│     ├── 02_glue_database.png
│     ├── 03_glue_crawlers.png
│     ├── 04_glue_tables.png
│     ├── 05_glue_job.png
│     ├── 06_manifest_output.png
│     ├── 07_data_profiling_results.png
│     ├── 08_data_card.png
│     └── 09_artifact_inventory.png
│
├── outputs
│
└── assets
```

---

# Screenshots

## Amazon S3 Data Lake

![](screenshots/01_s3_bucket_structure.png)

---

## AWS Glue Database

![](screenshots/02_glue_database.png)

---

## AWS Glue Crawlers

![](screenshots/03_glue_crawlers.png)

---

## AWS Glue Tables

![](screenshots/04_glue_tables.png)

---

## AWS Glue Job

![](screenshots/05_glue_job.png)

---

## Dataset Manifest

![](screenshots/06_manifest_output.png)

---

## Data Profiling Results

![](screenshots/07_data_profiling_results.png)

---

## Data Card

![](screenshots/08_data_card.png)

---

## Generated Artifacts

![](screenshots/09_artifact_inventory.png)

---

# Outputs Generated

The pipeline generates the following artifacts:

- Version Manifest
- Dataset Profile
- Schema Definition
- AI-ready Parquet Dataset
- Label Dataset
- Label Audit Report
- Data Card
- Athena Profiling Results
- Artifact Inventory

---

# Key Learning Outcomes

Through this project I gained practical experience with:

- Designing an AI-ready data engineering pipeline
- Organizing datasets inside an S3 data lake
- Working with AWS Glue Crawlers and Data Catalog
- Building metadata-driven pipelines
- Dataset versioning and auditability
- Feature engineering for Machine Learning
- Label engineering
- Generating reusable AI datasets
- Working with Parquet datasets
- Producing data cards for responsible AI workflows

---

# Future Improvements

- Automate pipeline using AWS Step Functions
- Integrate AWS Glue Workflows
- Add AWS Lambda event triggers
- Create CI/CD deployment using GitHub Actions
- Integrate Amazon Bedrock for metadata enrichment
- Deploy downstream ML training pipeline using SageMaker

---

# Author

**Shrivathsan K M**

GitHub

https://github.com/Vathsan07

---

# License

This repository is created for educational purposes as part of the BITS Pilani AI Engineering Program.

The original dataset belongs to the UCI Machine Learning Repository.
