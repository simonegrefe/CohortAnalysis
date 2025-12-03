# 🔗 ETL & Cohort Analysis 

## 🧾 Project Overview

This project delivers an end-to-end data pipeline and analytical framework designed to evaluate new-customer behaviour, retention, and repeat-purchase dynamics using cohort analysis. It focuses on customers acquired in 2024, leveraging automated data ingestion, cloud-based storage, scalable transformations, and visual analytics to uncover meaningful business insights.

To ... analysis, the project integrates multiple data platforms:

- Fivetran automates extraction from operational systems and continuously syncs transactional data.
- Google Cloud SQL / BigQuery serves as the central storage platform for raw and structured data.
- Databricks handles data preparation, transformation, and cohort construction at scale, including the generation of cohort tables, retention curves, and tree-based behavioural maps.

The primary goal is to understand how different groups of newly acquired customers behave over time and how their purchasing patterns evolve across subsequent months. By breaking customers into cohorts based on acquisition month, the analysis reveals differences in engagement, purchasing frequency, and long-term customer value.
