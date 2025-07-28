# WWI Sales Data Engineering Project

This repository contains a complete Microsoft Fabric Data Engineering solution for **WWI (Wide World Importers)**, designed to demonstrate scalable modern data architecture with a focus on analytics, governance, and reproducibility.

---

## 🧭 Project Overview

The WWI Sales project integrates multiple data sources—including on-premises databases, SharePoint, and file systems—into a unified data platform using Microsoft Fabric. This platform supports enterprise-grade data processing, lakehouse modeling, and Power BI analytics, delivering end-to-end visibility into sales performance and customer behavior.

---

## 🎯 Objectives

- Establish a **Lakehouse architecture** to consolidate structured and semi-structured data.
- Build **data ingestion pipelines** from hybrid sources (SharePoint, SQL Server).
- Enable **semantic modeling** for governed, reusable datasets.
- Deliver **Power BI reporting** for business consumption and decision-making.
- Apply best practices for project organization, documentation, and Git integration.

---

## 📐 Solution Architecture

┌─────────────────────────────┐
│ Source Systems │
│ ────────────────────────── │
│ - On-prem SQL │
│ - SharePoint DW Files │
│ - Manual File Uploads │
└────────────┬────────────────┘
│
▼
┌─────────────────────────────┐
│ Ingestion & Transformation│
│ ────────────────────────── │
│ - Fabric Dataflows │
│ - Data Pipelines (ETL) │
└────────────┬────────────────┘
│
▼
┌─────────────────────────────┐
│ Fabric Lakehouse │
│ ────────────────────────── │
│ - Bronze/Silver/Gold Layers│
│ - Star Schema Model │
└────────────┬────────────────┘
│
▼
┌─────────────────────────────┐
│ Semantic Modeling │
│ ────────────────────────── │
│ - Power BI Data Model │
│ - Reusable Datasets │
└────────────┬────────────────┘
│
▼
┌─────────────────────────────┐
│ Reporting & Insights │
│ ────────────────────────── │
│ - Power BI Dashboard │
└─────────────────────────────┘
