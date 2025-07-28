# 📘 WWI Sales – Fabric Lakehouse

This folder contains the core data lakehouse assets for the **WWI Sales Data Engineering Project**, built using Microsoft Fabric. The lakehouse serves as the foundational storage layer for all structured and semi-structured data used across analytics, reporting, and semantic modeling workloads.

---

## 🏷️ Lakehouse: `WWILakehouse`

---

## 🎯 Objective

The goal of this lakehouse is to enable centralized, scalable, and performant data access for key business domains including:

- Sales operations
- Customer analytics
- Geographic insights
- Inventory tracking

It integrates multiple upstream systems such as on-premises SQL, SharePoint lists, and flat file uploads, and standardizes the data using robust ETL pipelines and dataflows.

---

## 🧩 Table Overview

| Table Name                | Type       | Description                                 |
|---------------------------|------------|---------------------------------------------|
| `Dim_Cities`              | Dimension  | City-level lookup with location attributes  |
| `Dim_Countries`           | Dimension  | Country metadata and geography hierarchy    |
| `Dim_Customer`            | Dimension  | Master customer reference data              |
| `Dim_CustomerCategories`  | Dimension  | Customer segmentation mapping               |
| `Dim_Date`                | Dimension  | Standard date dimension for time analysis   |
| `Dim_StateProvinces`      | Dimension  | Regional subdivision information            |
| `Fact_Order_Line`         | Fact       | Granular sales line items                   |
| `wwi_Sales_Orders`        | Fact       | Sales order headers                         |
| `WWI_Warehouse_Inventory` | Fact       | Warehouse-level inventory snapshots         |

---

## 🔁 Ingestion Sources

Data is ingested using the following patterns:

- 🧩 **Dataflows** – SharePoint source for curated sales fact tables  
- 🔗 **Pipelines** – Ingest and land on-prem SQL tables to the lakehouse

---

## 📈 Consumption Layers

Data in this lakehouse powers:

- 📊 **Power BI Reports** – `WWI Sales PBI`
- 📐 **Semantic Models** – `WWI Sales Semantic Model`  
- 🧠 **Business KPIs** – Embedded into dashboards and decision workflows

---

## 🧱 Design Notes

- Modeled using a **star schema** with clean dimensional modeling
- Primary relationships use **natural keys** for consistency
- Partitioning and indexing designed for **performance at scale**
- Supports downstream **versioning, schema evolution**, and **delta updates**

---

## 📅 Last Updated

**July 28, 2025**

---
