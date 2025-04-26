---
title: Realtime Water Quality Prediction End-to-End Pipeline 
type: page
---

{{< resize src="/images/realtime_water_quality_prediction.gif" width="480" height="480" alt="GIF_Page" >}}

# Problem

Monitoring water quality in real time is crucial for public health, industrial operations, and environmental safety. Traditional systems often rely on delayed batch data, which makes it hard to respond quickly to dangerous conditions such as pH spikes and contamination that will affect in example the business pond fish.

The challenge: **build a scalable, real-time water quality prediction pipeline** that processes sensor data as it’s collected, predicts quality metrics instantly, and stores validated results for downstream analytics.

# Solution

Built using **Google Cloud Platform + Docker**, the pipeline connects end-to-end, from raw sensor data to BigQuery-ready predictions.

## Tools & Flow:
- **MongoDB**: Source of raw water quality sensor data  
- **Kafka**: Streams sensor data in real time  
- **PySpark (Dockerized)**: Predicts water quality using trained ML models  
- **Google Cloud Storage (GCS)**: Stores prediction results  
- **Cloud Functions**: Triggered by GCS events  
- **BigQuery**: Final destination for structured insights  


{{< resize src="/images/realtime_water_quality_prediction_1.png" width="720" height="360" alt="IMG_1" >}}

**NOTE: Due to a limitation in GCP's free trial (which does not support streaming from Spark to BigQuery), i implemented a workaround using Google Cloud Functions to push streaming data into BigQuery.**

## Example Workflow:
1. Water sensor writes raw data → stored in **MongoDB**  
2. Kafka Connector streams updates → **Kafka Broker**  
3. **PySpark model** consumes stream → predicts quality (e.g., “Safe”, “Unsafe”)  
4. Predictions stored as files in **GCS**  
5. **Cloud Function** triggers on new files → loads structured results into **BigQuery**

## Business Impact

- **Near real-time visibility** into water quality metrics  
- **Scalable & automated** pipeline using cloud-native tools  
- **Actionable insights** for alerts, dashboards, and compliance reporting

## Repository
- [**Github Code**](https://github.com/azharizz/Realtime-Water-Quality-Prediction-Data-Pipeline)
- [**Youtube**](https://youtu.be/bKVpUs-Ewoc)
