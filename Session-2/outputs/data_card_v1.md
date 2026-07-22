
# Data Card: Bank Marketing AI-Ready Dataset v1

## Purpose
Training dataset for BITS Pilani Digital Module 2 AWS lab. Used to teach AI data engineering, labeling, bias, explainability, and MLOps.

## Source
Public UCI Bank Marketing dataset. The raw source copy is preserved in S3.

## Target
`label` = 1 if `y` equals `yes`, otherwise 0.

## Known leakage exclusion
`duration` is excluded from the curated dataset because it is usually known only after a call and can leak outcome information.

## Sensitive or comparison attribute for teaching
`age_group_50plus` is used as a demonstration comparison group for bias analysis. It is not a policy recommendation.

## AWS evidence
- Manifest: s3://bits-ai-de-1464-20260721161520-us-east-1/module2/session2/audit/manifest_v1.json
- Schema: s3://bits-ai-de-1464-20260721161520-us-east-1/module2/session2/audit/schema_v1.json
- Profile: s3://bits-ai-de-1464-20260721161520-us-east-1/module2/session2/audit/data_profile_v1.json
- Athena profile: s3://bits-ai-de-1464-20260721161520-us-east-1/module2/session2/audit/athena_profile_results_v1.json
- Label audit: s3://bits-ai-de-1464-20260721161520-us-east-1/module2/session2/labels/labels_v1/label_audit_v1.json
- Curated table: bits_ai_de_bits_ai_de_1464_20260721161520.curated_bank_marketing_v1

## Limitations
This is a public teaching dataset. It does not represent a live production customer system, and the comparison group is included for responsible AI teaching only.
