# Week 03 Log — Data Exploration Sprint

**Week:** 3  
**Date Range:** 24-07-2026 to 30-07-2026  
**Team:** [10]  
**Project:** P10 – ShipTrack: Supply Chain Visibility Hub

---

## 1. Sprint Goal

The goal of this sprint was to explore the ShipTrack datasets, understand their structure, inspect schemas, verify data quality, and prepare the datasets for the Bronze Layer ingestion process using Databricks.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Created Databricks Catalog, Schema and Volume | Shivani | Done | Databricks Workspace |
| Uploaded all ShipTrack datasets to Databricks Volume | Shivani | Done | Volume Screenshot |
| Created Week 3 Data Exploration Notebook | Shivani | Done | `notebooks/01_data_exploration` |
| Loaded hubs, carriers, routes, scan_events and exceptions datasets | Shivani | Done | Notebook Output |
| Explored schemas, row counts and column information | Shivani | Done | Notebook Output |
| Verified source dataset availability in Databricks Volume | Shivani | Done | Volume Screenshot |
| Investigated shipments.parquet loading issue | Shivani | In Progress | Error Screenshot |

---

## 3. Key Decisions

- Used Databricks Free Edition as recommended by the project guidelines.
- Stored all datasets inside the Databricks Volume before beginning data exploration.
- Verified the schema and structure of each dataset before implementing further processing.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| Unable to read `shipments.parquet` due to Parquet compatibility (`TIMESTAMP(NANOS)`) | Shipment dataset exploration is pending | Need a compatible dataset or guidance from the project provider |

---

## 5. Evidence Added to GitHub

- Week 3 Data Exploration Notebook
- Databricks Volume Screenshot
- Dataset Schema Outputs
- Data Exploration Results
- Error Screenshot for `shipments.parquet`

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI assisted in preparing the PySpark notebook, explaining the code, and troubleshooting the dataset loading issue. |
| What we changed after AI suggestion | Updated the notebook structure, verified dataset paths, and performed additional debugging steps. |
| What we verified manually | Verified dataset upload, volume path, schema outputs, notebook execution, and dataset accessibility in Databricks. |
| What we can explain without AI | Project setup, data exploration workflow, dataset structure, notebook execution process, and schema analysis. |

---

## 7. Next Week Preparation

- Resolve the `shipments.parquet` compatibility issue.
- Begin Bronze Layer data ingestion.
- Implement data quality validations and transformation pipeline.
- Prepare datasets for Silver Layer processing.
