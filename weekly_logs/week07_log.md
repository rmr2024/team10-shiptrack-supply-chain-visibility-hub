# Week 07 Log — Gold Metrics

**Project:** ShipTrack – Supply Chain Visibility Hub

**Week:** 7

**Date range:** September 1–7, 2026

---

## 1. Sprint Goal

The goal for Week 7 was to create dashboard-ready Gold tables and document the KPI formulas and metric grain.

---

## 2. Work Completed

| Task | Status |
|---|---|
| Created Gold aggregation notebook | Done |
| Created daily shipment metrics | Done |
| Created carrier metrics | Done |
| Created route metrics | Done |
| Created hub metrics | Done |
| Documented KPI formulas | Done |
| Defined metric grain | Done |
| Added Gold validation checks | Done |

---

## 3. Gold Tables

The following Gold tables were created in Databricks:

- `gold_shipment_daily_metrics`
- `gold_carrier_metrics`
- `gold_route_metrics`
- `gold_hub_metrics`

These tables provide aggregated outputs for dashboard and Power BI reporting.

---

## 4. Validation

The Gold tables were validated in Databricks after creation.

Validation checks include:

- Gold table row counts
- Null checks on key fields
- Delivery rate range validation
- On-time delivery rate range validation
- Negative metric validation

---

## 5. Evidence

The following evidence will be added to GitHub:

- `week07_gold_metrics.png`
- `week07_validation.png`

---

## 6. Blockers / Risks

No major blockers were identified during the Gold aggregation stage.

---

## 7. AI Transparency Note

AI was used to help structure the Gold aggregation notebook and organize KPI definitions.

The suggested logic was adapted to match the actual ShipTrack Silver tables and columns available in Databricks.

The team verified the table names, column names, aggregation logic, joins, and validation queries in Databricks.

The team can explain the purpose of each Gold table, KPI formula, metric grain, and validation check.

---

## 8. Next Steps

- Review Gold table outputs.
- Capture Gold metrics evidence.
- Capture Gold validation evidence.
- Prepare the Gold outputs for dashboard development.
