# Support Tickets ETL Pipeline

Cloud-based ETL pipeline for CarePlus BPO that processes support ticket data using AWS services.

## Architecture

![Data Architecture](Pipeline_architecture.jpeg)

## Tech Stack

- **Storage**: AWS S3 Data Lake
- **Processing**: AWS Lambda (logs) | AWS Glue (CSV files)
- **Warehouse**: Amazon Redshift
- **Analytics**: AWS Athena | Power BI

## Data Flow

```
OLTP → S3 Raw → Lambda/Glue → S3 Processed → Redshift → Power BI
                                            ↓
                                         Athena
```

## Key Features

- Event-driven automation with S3 triggers
- Serverless scalable architecture
- Incremental data loading
- Interactive Power BI dashboards

## Quick Setup

1. Configure AWS credentials: `aws configure`
2. Create S3 buckets (raw, processed, scripts)
3. Deploy Lambda function with S3 trigger
4. Set up Glue crawler and ETL job
5. Configure Redshift cluster and load data
6. Connect Power BI via ODBC driver

## Project Structure

```
├── data/           # Raw and processed data
├── lambda/         # Log processing function
├── glue/           # CSV ETL job scripts
└── sql/            # Athena queries
```

## Contact

[Your Name] - [sreeragcr547@gmail.com]

GitHub: [github.com/sreeragcr13/aws-etl-pipeline](https://github.com/sreeragcr13/Support-Tickets-ETL-Pipeline-Using-AWS)
