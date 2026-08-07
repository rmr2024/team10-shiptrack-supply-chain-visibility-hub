# Problem Charter

**Week:** 1

**Project:** ShipTrack – Supply Chain Visibility Hub

**Owners:** G. Shivani, B. Likhitha, R. Meenakshi Reddy

---

# 1. Problem Context

Supply chain organizations generate large amounts of data from orders, shipments, warehouses, suppliers, and inventory systems. This data is often stored in different formats, making it difficult to monitor operations, identify delays, and make timely business decisions.

ShipTrack addresses this challenge by building an end-to-end data engineering pipeline that ingests, cleans, validates, and transforms raw supply chain data into reliable datasets for reporting and analytics.

---

# 2. Engineering Problem

Design and implement a scalable Medallion Architecture using Databricks that converts raw supply chain datasets into trusted Bronze, Silver, and Gold layers. Apply data quality validation and generate business-ready datasets that can be visualized in Power BI dashboards while supporting streaming simulation for shipment events.

---

# 3. Users / Stakeholders

| Stakeholder | Data Requirement |
|-------------|------------------|
| Supply Chain Manager | Monitor shipment progress and inventory |
| Warehouse Manager | Track stock levels and warehouse operations |
| Logistics Team | Detect shipment delays and optimize delivery |
| Business Analyst | Generate reports and business insights |

---

# 4. Scope (Included)

The project will include:

- Source datasets
- Bronze data ingestion
- Silver transformations
- Data Quality validation
- Gold business metrics
- Power BI dashboards
- Streaming simulation
- GitHub documentation
- Weekly sprint evidence

---

# 5. Scope (Excluded)

The project will not include:

- Production deployment
- Live customer data
- ERP integration
- Payment systems
- Mobile application
- Third-party logistics APIs
- Copied external projects

---

## 6. Success Criteria

By the end of 12 weeks, the project is successful if:

- The pipeline can be explained end to end.
- The team can show Bronze, Silver, DQ, Gold, dashboard, and streaming evidence.
- All three students can explain the full project at a high level.
- GitHub contains weekly evidence and final submission files.
