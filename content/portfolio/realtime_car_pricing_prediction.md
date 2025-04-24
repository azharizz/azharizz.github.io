---
title: Realtime Car Pricing Prediction
type: page
---

{{< resize src="/images/realtime_car_pricing_prediction.gif" width="480" height="480" alt="GIF_Page" >}}

# Problem

This project tackles the challenge of real-time car price prediction in used car marketplaces, where pricing is often **inconsistent and subjective**. The goal is to provide an AI-powered tool that predicts fair market prices instantly, helping both sellers and buyers make better decisions

# Result

Tools Used:
- MySQL
- Debezium
- Kafka
- Spark
- FastAPI
- GCP
- Cloud Storage
- Cloud Functions
- BigQuery
- ML Model
- Docker

Using the tools above, we built the data infrastructure and pipeline from **scratch**, enabling seamless real-time price prediction. The system streams data from MySQL using Debezium, processes it with Spark, and serves predictions through a **FastAPI endpoint**.

**NOTE: Due to a limitation in GCP's free trial (which does not support streaming from Spark to BigQuery), we implemented a workaround using Google Cloud Functions to push streaming data into BigQuery.**

A full demo of the project is available on **YouTube**, showcasing the end-to-end flow from data ingestion to real-time prediction.

## Repository
- [**Github Code**](https://github.com/azharizz/realtime_car_pricing_prediction)
- [**Youtube**](https://youtu.be/mvJR-IZ9x04)

