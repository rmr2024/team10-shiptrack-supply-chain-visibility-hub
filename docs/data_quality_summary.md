# Data Quality Summary

**Project:** ShipTrack – Supply Chain Visibility Hub

**Week:** 6

**Purpose:** Run meaningful data quality checks on Silver tables, capture failures, and explain their business impact.

---

## 1. Quality Rule Results

| Rule ID | Rule Name | Severity | Failed Count | Business Impact |
|---|---|---|---:|---|
| DQ-01 | Required scan_id not null | High | [Enter result] | Records without a scan ID cannot be reliably tracked. |
| DQ-02 | Duplicate scan_id check | High | [Enter result] | Duplicate scan events can distort shipment tracking and metrics. |
| DQ-03 | Shipment numeric values not negative | Medium | [Enter result] | Invalid weight, package count, freight, or attempt values can affect operational and financial metrics. |
| DQ-04 | Valid reference IDs | High | [Enter result] | Invalid hub, carrier, or route references can cause incorrect joins and reporting. |
| DQ-05 | Valid shipment timestamp order | Medium | [Enter result] | Incorrect timestamps can affect delivery time and performance calculations. |

---

## 2. Failed Record Examples

Failed records were reviewed using the Data Quality Checks notebook.

The notebook captures sample failed records for:

- Missing scan IDs
- Duplicate scan IDs
- Invalid shipment numeric values
- Invalid hub, carrier, or route references
- Invalid shipment timestamp order

The failed examples will be reviewed before Gold-level metrics are generated.

---

## 3. Business Impact

Data quality issues can directly affect shipment visibility and dashboard accuracy.

Missing or duplicate scan IDs can make shipment events difficult to track correctly.

Invalid hub, carrier, or route references can lead to incorrect joins between Silver tables.

Negative or invalid shipment values can affect operational and financial calculations.

Incorrect timestamp ordering can affect delivery duration and on-time delivery metrics.

Therefore, high-severity data quality failures should be investigated before the affected records are used for important Gold metrics.

---

## 4. Handling of Failed Records

Failed records are identified during the Data Quality Checks stage.

The team will review the failed records and decide whether they should be corrected, excluded, or flagged depending on the type of failure.

No records are silently removed during the DQ checking stage.

---

## 5. Rules That Should Block or Flag Gold Metrics

The following rules should be treated as important before generating Gold metrics:

- DQ-01 should be reviewed because missing scan IDs affect shipment tracking.
- DQ-02 should be reviewed because duplicate events can inflate metrics.
- DQ-04 should be reviewed because invalid references can affect joins.
- DQ-05 should be reviewed because incorrect timestamps can affect delivery metrics.

DQ-03 should also be reviewed before using shipment financial and operational measures.

---

## 6. Overall Quality Summary

The Silver data was checked using multiple data quality rules covering required fields, duplicates, numeric ranges, reference integrity, and timestamp ordering.

The checks are designed around the actual ShipTrack business data rather than only checking for null values.

Failed records are captured as examples so that the team can understand the cause and business impact of each issue.

The results from the Databricks notebook will be used to complete the final failed counts in this document.

The most important failures for downstream reporting are duplicate records, invalid references, and incorrect timestamps because they can directly affect shipment visibility and business metrics.

The DQ results will be reviewed before proceeding to Gold-level aggregations.
