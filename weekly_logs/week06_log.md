# Week 06 Log — Data Quality Checks

**Week:** 6  
**Date range:** September 1–7, 2026
**Team:** Team 10  
**Project:** ShipTrack – Supply Chain Visibility Hub

---

## 1. Sprint Goal

The goal for Week 6 was to run meaningful data quality checks on the Silver data.

The checks cover required fields, duplicate records, valid numeric ranges, reference integrity, and timestamp ordering.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Added required field checks | Team 10 | Done | `notebooks/04_data_quality_checks.ipynb` |
| Added duplicate record checks | Team 10 | Done | `notebooks/04_data_quality_checks.ipynb` |
| Added range checks | Team 10 | Done | `notebooks/04_data_quality_checks.ipynb` |
| Added reference checks | Team 10 | Done | `notebooks/04_data_quality_checks.ipynb` |
| Added timestamp validation | Team 10 | Done | `notebooks/04_data_quality_checks.ipynb` |
| Captured failed record examples | Team 10 | Done | DQ notebook outputs |
| Documented business impact | Team 10 | Done | `docs/data_quality_summary.md` |

---

## 3. Key Decisions

- DQ checks were designed using the actual Silver tables available in Databricks.
- The checks focus on data issues that can affect shipment tracking and business metrics.
- Failed records are captured for review instead of being silently removed.
- High-impact data quality issues will be reviewed before Gold metrics are generated.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| None currently identified | No major impact | None |

---

## 5. Evidence Added to GitHub

- `notebooks/04_data_quality_checks.ipynb`
- `src/data_quality_rules.py`
- `docs/data_quality_summary.md`
- `weekly_logs/week06_log.md`
- `screenshots/week06_dq_results.png`
- `screenshots/week06_failed_records_sample.png`

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI was used to help structure the data quality checks and explain suitable DQ rules for the ShipTrack Silver tables. |
| What we changed after AI suggestion | The suggested checks were adapted to match the actual ShipTrack table and column names in Databricks. |
| What we verified manually | The Silver table names, column names, joins, and SQL logic were verified in Databricks. |
| What we can explain without AI | We can explain why each DQ rule is required, what type of failure it detects, and how the failure can affect shipment reporting. |

---

## 7. Next Week Preparation

- Review the Week 6 DQ results and failed records.
- Prepare the validated Silver data for Gold-level aggregations.
