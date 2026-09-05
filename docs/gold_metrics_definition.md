# Gold Metrics Definition

**Project:** ShipTrack – Supply Chain Visibility Hub

**Week:** 7

**Date:** September 1–7, 2026

## 1. Purpose

The Gold layer contains aggregated, dashboard-ready datasets created from the validated Silver layer.

These tables are designed to support shipment monitoring, carrier performance, route analysis, and hub-level reporting.

---

## 2. Gold Tables

| Gold Table | Metric Grain | Purpose |
|---|---|---|
| `gold_shipment_daily_metrics` | One row per booking date | Daily shipment KPIs |
| `gold_carrier_metrics` | One row per carrier | Carrier performance |
| `gold_route_metrics` | One row per route | Route performance |
| `gold_hub_metrics` | One row per hub | Hub shipment flow |

---

## 3. KPI Definitions

### Total Shipments

**Formula:**

`COUNT(*)`

**Meaning:**

Total number of shipment records for the selected metric grain.

---

### Delivered Shipments

**Formula:**

`COUNT of shipments where delivery_outcome = 'DELIVERED'`

**Meaning:**

Number of shipments successfully delivered.

---

### Delivery Rate

**Formula:**

`Delivered Shipments / Total Shipments × 100`

**Meaning:**

Percentage of shipments that were delivered.

---

### On-Time Shipments

**Formula:**

A shipment is considered on time when:

`actual_delivery_ts <= promised_delivery_ts`

and the shipment has been delivered.

---

### On-Time Delivery Rate

**Formula:**

`On-Time Shipments / Delivered Shipments × 100`

**Meaning:**

Percentage of delivered shipments that reached the customer on or before the promised delivery time.

---

### Delayed Deliveries

**Formula:**

A shipment is considered delayed when:

`actual_delivery_ts > promised_delivery_ts`

and the shipment has been delivered.

---

### Average Delivery Hours

**Formula:**

`Average(actual_delivery_ts - pickup_ts)`

The difference is measured in hours.

**Meaning:**

Average time taken from pickup to actual delivery.

---

### Total Freight Amount

**Formula:**

`SUM(freight_amount_inr)`

**Meaning:**

Total freight amount associated with the shipments.

---

### Average Package Weight

**Formula:**

`AVG(package_weight_kg)`

**Meaning:**

Average package weight for the selected metric grain.

---

## 4. Gold Table Details

### gold_shipment_daily_metrics

**Grain:** One row per booking date.

Main metrics:

- Total shipments
- Delivered shipments
- On-time shipments
- Delayed deliveries
- Delivery rate
- On-time delivery rate
- Average delivery hours
- Total freight amount

**Dashboard use:**

Used for daily shipment trends and overall shipment KPIs.

---

### gold_carrier_metrics

**Grain:** One row per carrier.

Main metrics:

- Total shipments
- Delivered shipments
- On-time shipments
- Delayed deliveries
- Delivery rate
- On-time delivery rate
- Average delivery hours
- Total freight amount

**Dashboard use:**

Used to compare carrier performance.

---

### gold_route_metrics

**Grain:** One row per route.

Main metrics:

- Total shipments
- Delivered shipments
- On-time shipments
- Delayed deliveries
- Delivery rate
- On-time delivery rate
- Average package weight
- Total freight amount

**Dashboard use:**

Used to identify high-volume and underperforming routes.

---

### gold_hub_metrics

**Grain:** One row per hub.

Main metrics:

- Origin shipments
- Destination shipments
- Delivered shipments
- Total hub shipments

**Dashboard use:**

Used to understand shipment flow and hub activity.

---

## 5. Dashboard Usage

The Gold tables are intended to be used as the primary datasets for dashboard and Power BI reporting.

Recommended dashboard sections:

1. Overall shipment KPIs
2. Daily shipment trends
3. Carrier performance
4. Route performance
5. Hub shipment flow

The dashboard should use the Gold layer rather than directly querying raw data.

---

## 6. Data Quality Dependency

The Gold layer is created from the validated Silver layer.

Data quality checks performed during Week 6 cover:

- Required fields
- Duplicate records
- Numeric range validation
- Reference integrity
- Timestamp ordering

DQ failures should be reviewed before using affected data for important business metrics.

---

## 7. Metric Design Principles

The Gold tables use a clearly defined metric grain so that dashboard aggregations do not unintentionally double-count records.

Aggregations are performed before the data is consumed by the dashboard layer.

The Gold layer contains business-ready metrics rather than raw event-level records.
