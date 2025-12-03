# 🔗 ETL & Cohort Analysis 

## 🧾 Project Overview

This project provides an end-to-end data pipeline and analytical framework designed to evaluate new-customer behaviour, retention, and repeat-purchase dynamics through cohort analysis. Focusing on customers acquired in 2024, the solution combines ++automated data ingestion**, **cloud-based storage**, **scalable transformations**, and **curated analytics** to generate meaningful insights into customer engagement and long-term value.

A **structured Databricks medallion architecture (bronze–silver–gold)** ensures data quality and analytical reliability throughout the process. **Raw data from BigQuery** is ingested into the bronze layer, refined into a clean and structured cohort dataset in silver, and curated into gold-layer analytical tables that enable detailed retention and repeat-purchase evaluations. These curated results are **visualized in a Databricks dashboard**, illustrating how customer behaviour evolves across monthly acquisition cohorts and providing clear visibility into customer lifecycle performance.


## 🎯 Objectives

The primary objectives of the project are:

- Understand how newly acquired customers behave over time.
- Measure retention and repeat-purchase patterns across monthly cohorts.
- Identify differences in purchasing behaviour between customer groups.
- Detect acquisition trends throughout 2024.
- Provide actionable insights to support customer-retention and marketing strategies.


## 🗂️ Data Sources

The analysis is based on customer and transaction data covering the year 2024, including:

- 200 new customers
- 1,000 total orders
- sales by customer


## 🔧 Transformation Process

To deliver a robust and scalable foundation for cohort analysis, the project integrates multiple data platforms and applies a structured transformation workflow within Databricks.

### 1. Platform Integration

- **Google Cloud SQL / BigQuery** serves as the central storage platform for raw and structured data prior to transformation.
- **Fivetran** automates the extraction of transactional and customer data from operational systems and continuously syncs updates to the data warehouse.
- **Databricks** performs the full transformation workflow, including data preparation, SQL-based modeling, and cohort construction at scale.

### 2. Medallion Architecture (Bronze–Silver–Gold)

The Databricks transformation logic follows the standard medallion architecture:

- **Bronze Layer – Raw Data**
Clean raw data is imported from BigQuery into Databricks exactly as ingested by Fivetran, preserving source fidelity.

- **Silver Layer – Refined Data**
Data is standardized, and modeled using SQL to produce the `cohort_analysis` table with **total_orders**, **first_order_date** and **second_order_date** which forms the analytical foundation for subsequent calculations.

- **Gold Layer – Curated Analytics Tables**
Final analytical datasets are generated for direct analysis and visualization, including:
  - `retention_rate` – retention performance within 1, 2 and 3 month across cohorts
  - `repeat_purchase_rates` – repeated orders across cohorts
  - `cohort_size` – number of customers for each cohort
 
### **3. Curated Analytics & Dashboard Visualization**

The final curated analytical tables are presented in a **Databricks dashboard**, enabling interactive exploration of how customer behaviour evolves across time and across cohorts.


## 📊 Visualization

![Dashboard preview](


