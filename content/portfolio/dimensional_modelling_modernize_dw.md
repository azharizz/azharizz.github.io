---
title: Dimensional Modelling & Modernize Data Warehouse
type: page
tags: ["data engineer", "portfolio", "platform", "architecture", "ai", "machine learning"]
---

{{< resize src="/images/dimensional_modelling_modernize_dw.gif" width="480" height="480" alt="GIF_Page" >}}

# Problem

Modernize and build a scalable Data Warehouse for Multiple Teams using a cloud-native. Key challenges include:

- **Inconsistent data sources**: Sales data spread across transactional systems, Firestore, and external feeds.  
- **Lack of actionable insights**: Difficulty measuring promotion ROI, territory performance, and customer segments in real time.  
- **Complex ETL maintenance**: Existing pipelines are brittle and hard to orchestrate.

## User Requirements

1. **Business Development Manager:**
   - Analyze effectiveness of special offers and promotions on sales to inform future marketing decisions.
2. **Sales Manager:**
   - Compare sales across territories and convert USD↔EUR to pinpoint top regions and assess currency impact.
3. **Customer Relationship Manager:**
   - Perform real-time clustering of customers by purchase frequency and average order value (since 2013) to tailor loyalty programs.

# Result

We designed a dimensional model in BigQuery and automated ELT/ETL with **dbt**, **Airflow**, and streaming components for real-time analytics.

## Implementation

1. **Promotion Performance** (Req. 1)
   - Created a **daily promotion fact table** capturing promotion IDs, types, and sales metrics.
   - Orchestrated with Airflow DAGs and transformed with dbt models.

{{< resize src="/images/dimensional_modelling_modernize_dw_1.png" width="720" height="480" alt="IMG_1" >}}

2. **Territory & Currency Analysis** (Req. 2)
   - Built a **territory dimension** and **sales fact** table recording USD/EUR values.
   - Historic data from 2013–2014 loaded via Dataflow into BigQuery; currency conversion rates applied in dbt.

{{< resize src="/images/dimensional_modelling_modernize_dw_2.png" width="720" height="480" alt="IMG_2" >}}

3. **Real-Time Customer Clustering** (Req. 3)
   - Streamed Firestore purchase events through **Pub/Sub** into **Dataflow**, then into **Dataproc** Spark KMeans job.
   - Cluster assignments landed in BigQuery; Cloud Functions trigger retraining and reload customer segments.

{{< resize src="/images/dimensional_modelling_modernize_dw_3.png" width="720" height="480" alt="IMG_3" >}}


## Tools & Technologies

- **Data Warehouse**: BigQuery  
- **Modeling & ELT**: dbt, Airflow  
- **Streaming & ETL**: Pub/Sub, Dataflow, Dataproc (Spark)  
- **Batch Processing**: Cloud Functions, Docker containers  
- **Storage & DB**: Firestore, BigQuery  
- **Orchestration**: Airflow (GKE)  
- **Development**: Agile SDLC

{{< resize src="/images/dimensional_modelling_modernize_dw_4.png" width="720" height="360" alt="IMG_4" >}}

**NOTE: Due to a limitation in GCP's free trial (which does not support streaming from Spark to BigQuery), i implemented a workaround using Google Cloud Functions to push streaming data into BigQuery.**

## Business Impact

- **Promotion ROI Visibility**: Daily insights into offer effectiveness.  
- **Territory Optimization**: Identified top-performing regions and quantified currency effects.  
- **Customer Retention**: Dynamic segments enable targeted loyalty programs and higher repeat purchases.

## Repository
- [**Github Code**](https://github.com/azharizz/Modernize-Data-Warehouse-GCP)
- [**Youtube**](https://youtu.be/Urmqulp2EZk)
