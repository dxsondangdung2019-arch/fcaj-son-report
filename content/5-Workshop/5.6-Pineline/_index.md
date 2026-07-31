---
title: "Pipeline Data Engineering"
date: 2026-07-28
weight: 6
chapter: false
pre: " <b> 5.6 </b> "
---

In this section, you will explore the **Data Engineering Pipeline** used to clean and validate interaction data before it is delivered to the Machine Learning workflow.

The pipeline focuses on **data validation**, **data normalization**, **ID preservation**, and **quality reporting**. It does **not** train machine learning models, deploy the frontend, or manage the application's database.

---

## Processing Workflow

The pipeline consists of the following stages:

![Overall architecture](/images/5-Workshop/architecture.png)

| Stage                              | Description                                                                                                                                                                                                                 |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Database Export**             | The application exports interaction data as a ZIP archive containing `interactions.csv`, `Products.json`, and `items.csv` (ignored by the pipeline).                                                                        |
| **2. Amazon S3**                   | The ZIP archive is uploaded to an Amazon S3 bucket. An `ObjectCreated` event automatically triggers the processing Lambda function.                                                                                         |
| **3. Processing Lambda**           | AWS Lambda reads the archive, validates the dataset schema, verifies event types and timestamps, checks `ITEM_ID` against `Products.json`, removes duplicate records, and preserves all original user and item identifiers. |
| **4. CloudWatch Logs**             | During execution, Lambda writes execution logs and error logs to Amazon CloudWatch for monitoring and troubleshooting.                                                                                                      |
| **5. Processed Dataset**           | All valid interaction records are written to the `processed/` directory as `interactions_clean.csv`, providing a clean dataset ready for machine learning.                                                                  |
| **6. Rejected Dataset**            | Invalid or duplicate records are stored in the `rejected/` directory together with the corresponding rejection reasons for auditing purposes.                                                                               |
| **7. Data Quality Reports**        | The pipeline generates `data_quality_report.json` and `data_quality_report.md`, summarizing data quality metrics, validation results, and ID preservation checks.                                                           |
| **8. Downstream Machine Learning** | The cleaned dataset and quality reports are delivered to the Machine Learning workflow, where they can be imported into Amazon Personalize or other recommendation systems for model training and evaluation.               |

{{% notice info %}}
The entire pipeline infrastructure is provisioned using **AWS SAM (AWS Serverless Application Model)** and **AWS CloudFormation**, including Amazon S3, AWS Lambda, IAM permissions, S3 event notifications, and CloudWatch log retention. This Infrastructure as Code (IaC) approach ensures consistent and repeatable deployments.
{{% /notice %}}

---

## Input Validation

The pipeline reads two required files:

- `interactions.csv`
- `Products.json`

The `interactions.csv` file must contain the following columns:

```text
USER_ID
ITEM_ID
EVENT_TYPE
TIMESTAMP
```

Where:

- `USER_ID` identifies the user.
- `ITEM_ID` identifies the product.
- `EVENT_TYPE` represents the interaction type.
- `TIMESTAMP` stores the interaction time as a Unix timestamp.

`Products.json` is used to verify that every `ITEM_ID` exists in the product catalog.

---

## Data Validation and Normalization

Before producing the final dataset, the pipeline performs several validation steps:

- Check for missing `USER_ID`, `ITEM_ID`, or `TIMESTAMP`.
- Verify that each `ITEM_ID` exists in `Products.json`.
- Validate supported event types (`view`, `add_to_cart`, `remove_from_cart`, `purchase`).
- Verify that `TIMESTAMP` is a valid Unix timestamp.
- Detect and remove duplicate records.

During normalization:

- `EVENT_TYPE` is converted to lowercase.
- `USER_ID` and `ITEM_ID` are trimmed without modifying their original values.
- All original identifiers are preserved.

---

## ID Preservation

One of the key design goals is to preserve source identifiers.

After processing:

- No new `USER_ID` values are generated.
- No new `ITEM_ID` values are generated.
- Every identifier in the output dataset already exists in the input dataset.

This ensures that the cleaned data can be used directly by downstream recommendation services.

---

## Output Artifacts

After processing, the pipeline generates four artifacts.

| Artifact                    | Purpose                                  |
| --------------------------- | ---------------------------------------- |
| `interactions_clean.csv`    | Clean dataset for Machine Learning       |
| `interactions_rejected.csv` | Invalid or rejected records with reasons |
| `data_quality_report.json`  | Machine-readable quality report          |
| `data_quality_report.md`    | Human-readable quality report            |

These artifacts provide traceability and simplify downstream data validation.

---

## AWS Deployment

The pipeline follows an **event-driven** architecture using Amazon S3 and AWS Lambda.

When a ZIP archive is uploaded to the S3 bucket:

1. Amazon S3 generates an `ObjectCreated` event.
2. AWS Lambda is triggered automatically.
3. The pipeline validates and cleans the interaction data.
4. Output artifacts are written back to Amazon S3.

This design enables fully automated data processing without manual intervention.

---

## Validation Results

The sample dataset produced the following results:

| Metric          |  Value |
| --------------- | -----: |
| Input Rows      | 23,377 |
| Clean Rows      | 23,377 |
| Rejected Rows   |      0 |
| Duplicate Rows  |      0 |
| Unique Users    |    200 |
| Unique Items    |    100 |
| Product IDs     |    100 |
| ID Preservation |   PASS |

These results indicate that the dataset passed all validation checks and is ready for machine learning.

---

## Automated Testing

The repository includes **48 automated tests** covering:

- ZIP archive validation
- Schema validation
- Product lookup
- Duplicate detection
- Output schema
- ID preservation
- Lambda event handling
- Output generation

These tests help ensure that the pipeline behaves consistently before deployment.

---

## Handover to Machine Learning

After the pipeline completes, the following artifacts are delivered to the Machine Learning team:

- `interactions_clean.csv`
- `data_quality_report.json`
- `data_quality_report.md`

These files are then used to import data into Amazon Personalize, train recommendation models, evaluate performance, and deploy recommendation campaigns.
