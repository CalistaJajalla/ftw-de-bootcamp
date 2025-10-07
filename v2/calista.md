# 📓 Data Cleaning Journal – Insta Dataset

**Date:** `2025-10-07`  
**Author:** `Calista Jajalla`  
**Dataset:** [Insta Aisles Checks](https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data?select=aisles.csv) (`aisles`, `departments`, `products`, `orders`, `order_products_prior`, `order_products_train`)  
**Purpose:** Consolidate **data quality checks**, validate **table integrity**, and create **metrics for dashboards**.

---

## 🔗 Table of Contents

- [1️⃣ Overview](#1️⃣-overview)  
- [2️⃣ Setup – DQ Log Table](#2️⃣-setup--dq-log-table)  
- [3️⃣ Global Checks](#3️⃣-global-checks)  
  - [3.1 Row Counts](#31-row-counts)  
  - [3.2 Primary Key Uniqueness](#32-primary-key-uniqueness)  
- [4️⃣ Table-Level Checks & Story](#4️⃣-table-level-checks--story)  
  - [4.1 Aisles](#41-aisles)  
  - [4.2 Departments](#42-departments)  
  - [4.3 Products](#43-products)  
  - [4.4 Orders & Order Products](#44-orders--order-products)  
  - [4.5 Reorder & Foreign Key Checks](#45-reorder--foreign-key-checks)  
- [5️⃣ Checklist for Data Cleaning Story](#5️⃣-checklist-for-data-cleaning-story)  
- [6️⃣ Next Steps & Links](#6️⃣-next-steps--links)

---

## 1️⃣ Overview

**Goal:** Ensure raw data integrity and prepare it for downstream analytics. We focus on six core **data quality categories**:

- **Volume Checks:** row counts and totals.  
- **Uniqueness Checks:** primary key uniqueness.  
- **Completeness Checks:** critical fields not null or empty.  
- **Referential Integrity:** foreign keys match related tables.  
- **Domain/Range Checks:** values within expected ranges.  
- **Duplicates & Anomalies:** detect full-row duplicates and logical inconsistencies.

**Workflow:**

1. 
2. Inspect raw tables.  
2. Apply DQ checks (SQL queries).  
3. Store results in a central DQ log table: `raw._cali_insta__dq_checks`.  
4. Analyze outcomes (status: PASS/WARN/FAIL).  
5. Feed metrics into dashboards (optional).  
