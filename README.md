WWI Sales Data Engineering Project Documentation

This repository contains a complete end-to-end implementation of a Sales Data Engineering solution for Wide World Importers (WWI) using Microsoft Fabric. The project demonstrates real-world enterprise data engineering concepts, from ingestion to reporting, leveraging modern, scalable architecture.

1. ✨ Project Overview

This solution showcases how multiple data sources (on-prem SQL, SharePoint, file uploads) can be unified into a Lakehouse architecture for downstream analytics using Power BI.

It follows:

Scalable ingestion using Dataflows and Pipelines

Centralized data modeling in a Lakehouse

Reporting via a Power BI dashboard with a star-schema-based semantic model

Best practices in structuring, versioning, and documenting a Microsoft Fabric-based project

2. 📏 Architecture Overview



Arrows indicate the data flow across stages. All assets are created, managed, and versioned in GitHub.

Components:

Dataflows & Pipelines: Ingest from SharePoint, SQL Server

Lakehouse: OneLake-based scalable storage for structured/semi-structured data

Semantic Model: Star schema model with facts and dimensions for performance

Power BI Reports: Dynamic visualizations for business stakeholders

3. 🔄 Step-by-Step Project Workflow

Each stage below is mapped to a corresponding folder in the repository and is illustrated via screenshots.

3.1 Ingestion

Objective: Bring raw data from SharePoint and SQL Server into the Fabric workspace

Tool: Fabric Dataflows Gen2 and Pipelines

Output: Data stored as tables in Lakehouse Bronze layer

Steps:

Create pipelines to connect on-prem SQL and SharePoint

Define transformations in Dataflows (if needed)

Export pipeline/dataflow JSON to /ingestion/

Screenshot Placeholder: docs/images/ingestion-pipeline.png

3.2 Lakehouse

Objective: Store curated data for analytics

Tool: Microsoft Fabric Lakehouse

Output: Star schema tables in Silver/Gold zones

Steps:

Create a new Lakehouse (e.g., WWILakehouse)

Load ingested data into tables

Create derived tables and relationships (Fact + Dimension)

Key Tables:

Fact_Order_Line

wwi_Sales_Orders

Dim_Customer, Dim_Countries, Dim_Cities, Dim_Date

Screenshot Placeholder: docs/images/lakehouse-structure.png

3.3 Semantic Model

Objective: Build a reusable, performance-optimized model for reporting

Tool: Power BI PBIP model (fabric-native semantic model)

Steps:

Create relationships between facts and dimensions

Add DAX measures (e.g., Total Sales, Order Count, Avg Tax Rate)

Export PBIP model to /semantic-model/

Screenshot Placeholder: docs/images/semantic-model.png

3.4 Power BI Dashboard

Objective: Deliver a business-friendly interactive reporting experience

Tool: Power BI

Output: Deployed report file (.pbip) in /pbi/

Report Highlights:

Sales trend by time

Revenue by geography

Orders by product size

Top 10 customers by revenue

Screenshot Placeholder: docs/images/pbi-dashboard.png
