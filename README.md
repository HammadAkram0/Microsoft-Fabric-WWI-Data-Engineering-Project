# **Microsoft Fabric Data Engineering End to End Project**

This repository contains a complete end-to-end implementation of a **Sales Data Engineering** solution for **Wide World Importers (WWI)** using **Microsoft Fabric**. The project demonstrates real-world enterprise data engineering concepts, from ingestion to reporting, leveraging modern, scalable architecture.

---

## ⭐ **1. Project Overview**

This solution showcases how multiple data sources (**on-prem SQL**, **SharePoint**, **file uploads**) can be unified into a **Lakehouse** architecture for downstream analytics using **Power BI**.

**Key Highlights:**

* Scalable ingestion using **Dataflows** and **Pipelines**
* Centralized data modeling in a **Lakehouse & Data warehouse**
* Reporting via a **Power BI dashboard** with a star-schema-based semantic model
* Best practices in structuring, versioning, and documenting a **Microsoft Fabric** project

---

## 🧭 **2. Architecture Overview**

![Architecture Diagram](Architecture%20Diagram%20MS%20Fabric%20WWI.png)

> *Arrows indicate the data flow across stages.*

### 🧩 **Architecture Components:**

* **Dataflows & Pipelines:** Ingest from SharePoint and SQL Server
* **Lakehouse:** OneLake-based scalable storage for structured/semi-structured data
* **Semantic Model:** Star schema model with facts and dimensions for performance
* **Power BI Reports:** Dynamic visualizations for business stakeholders

---

## 🔄 **3. Step-by-Step Project Workflow**

Each stage is mapped to a corresponding folder in the repository and will include a screenshot.

### 3.1 **Ingestion**

**Objective:** Bring raw data from SharePoint and SQL Server into the Fabric workspace

* **Tools:** Fabric Dataflows Gen2 and Pipelines
* **Output:** Data stored as tables in Lakehouse Bronze layer

**Steps:**

1. Create pipelines to connect on-prem SQL and SharePoint
2. Define transformations in Dataflows (if needed)
3. Export pipeline/dataflow JSON to `/ingestion/`

![Ingestion Pipeline](Data%20Ingestion/Fabric%20Data%20Pipeline.png)

---

### 3.2 **Lakehouse**

**Objective:** Store curated data for analytics

* **Tool:** Microsoft Fabric Lakehouse
* **Output:** Star schema tables in Silver/Gold zones

**Steps:**

1. Create a new Lakehouse (e.g., `WWILakehouse`)
2. Load ingested data into tables
3. Create derived tables and relationships (Fact + Dimension)

**Key Tables:**

* `Fact_Order_Line`
* `wwi_Sales_Orders`
* `Dim_Customer`
* `Dim_Countries`
* `Dim_Cities`
* `Dim_Date`

![Lakehouse Structure](lakehouse/Lakehouse%20tables.png)

---

### 3.3 **Semantic Model**

**Objective:** Build a reusable, performance-optimized model for reporting

* **Tool:** Power BI PBIP model (Fabric-native semantic model)

**Steps:**

1. Create relationships between facts and dimensions
2. Add DAX measures (e.g., `Total Sales`, `Order Count`, `Avg Tax Rate`)
3. Export PBIP model to `/semantic-model/`

![Semantic Model Architecture](Power%20BI%20Dashboard/Semantic%20Model%20Architecture.png)

---

### 3.4 **Power BI Dashboard**

**Objective:** Deliver a business-friendly interactive reporting experience

* **Tool:** Power BI
* **Output:** Deployed report file (`.pbip`) in `/pbi/`

**Dashboard Highlights:**

* Sales trend by time
* Revenue by geography
* Orders by product size
* Top 10 customers by revenue

![Power BI Dashboard](Power%20BI%20Dashboard/WWI%20Sales%20Analysis%20Dashboard.png)

---

## 📁 **4. Repository Structure**

```bash
/
├── ingestion/               # Pipelines and Dataflows JSON
├── lakehouse/               # Lakehouse tables & structure exports
├── semantic-model/          # Semantic model (PBIP)
├── pbi/                     # Power BI dashboard files
├── docs/images/             # Screenshots & architecture diagram
└── README.md                # Root documentation (this file)
```

---

## ✅ **5. Best Practices Followed**

* Structured folders per Fabric domain
* Documentation-first approach
* Screenshots embedded for clarity
* Star schema modeling with natural keys


---

*Last updated: **July 28, 2025***
