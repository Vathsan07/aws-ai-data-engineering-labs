                    UCI Bank Marketing Dataset
                               │
                               ▼
                        Download Dataset
                               │
                               ▼
                    Amazon S3 (Raw CSV)
                               │
                               ▼
                      Data Versioning
                Manifest + Schema + Audit
                               │
                               ▼
                    AWS Glue Crawler
                               │
                               ▼
                 AWS Glue Data Catalog
                               │
                               ▼
                  AWS Glue ETL Job
        (Cleaning + Feature Engineering)
                               │
                               ▼
                  Curated Parquet Dataset
                               │
                 ┌─────────────┴──────────────┐
                 ▼                            ▼
           Amazon Athena              Labels Dataset
         (Profiling & Analysis)             │
                 │                           │
                 └─────────────┬─────────────┘
                               ▼
                     AI Ready Dataset
                               │
                               ▼
                      Session 4 ML Pipeline
