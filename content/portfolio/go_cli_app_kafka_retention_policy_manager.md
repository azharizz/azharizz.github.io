---
title: Go CLI App Kafka Retention Policy Manager 
type: page
---

{{< resize src="/images/go_cli_app_kafka_retention.gif" width="480" height="480" alt="GIF_Page" >}}

# Problem

Managing Kafka topic retention policies at scale is manual, error-prone, and carries two main risks:

- **Data Loss**: Misconfigured retention can delete critical streaming data.  
- **Cost Overruns**: Unvalidated data retention leads to inflated storage bills.

# Solution

To solve the problem, one approach is to create app like CLI to automate easily with the features:

- **Automated Retention Updates**  
  Applies bulk topic settings via Kafka’s Admin API in one command.  
- **Integrity Validation**  
  - Stores expected message counts in Redis  
  - Compares Redis counts with files or stored counts in GCS  
  - Halts on discrepancies to prevent data loss  
- **Cost-Efficient Archiving**  
  - Moves validated data from Cloud Storage to Coldline/Archive tiers  
  - Optionally deletes stale data post-archive  
- **Easy Integration**  
  Docker-packaged CLI, fits into CI/CD pipelines or scheduled jobs.


Stack Used:
- Redis
- GCS
- Kafka
- Postgres


{{< resize src="/images/go_cli_app_kafka_retention_1.png" width="720" height="360" alt="IMG_1" >}}



## Example Workflow

1. Ingested record count → saved to Redis key  
2. Compare Redis count with GCS file count  
3. **If counts match** → archive to Coldline/Archive or delete  
4. **If mismatch** → operation stops and raises alert  

## Business Impact

- **Zero-loss retention policy changes**  
- **Reduced storage costs** through automated tiering  
- **Faster, consistent policy management**  


## Repository
- [**Github Code**](https://github.com/azharizz/kafka-retention-manager-cli)
- [**Youtube**](https://www.youtube.com/watch?v=aGrZOSbiRoo)
