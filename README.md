# Real-Time Data Processing with Kafka and Spark Streaming

This project implements a real-time data processing pipeline using **Apache Kafka**, **Apache Spark Streaming**, and **FastAPI**. It processes clickstream events, validates them, enriches them with metadata, and publishes the enriched data back to Kafka.

## 🚀 Features

- Ingests events in real-time through a **FastAPI** endpoint.
- Validates events using **Schema Registry** to ensure data conformity.
- Processes events in real-time using **Apache Spark Streaming**.
- Enriches events with metadata such as `correlation_id`, `schema_id`, and `ingestion_timestamp`.
- Publishes enriched events back to Kafka in the `acme.clickstream.latest.events` topic.
- Monitors system health using **Prometheus** and **Grafana**.

## 🛠️ Technologies Used

- **FastAPI**: Used for building the API to receive events.
- **Apache Kafka**: Middleware for message queuing and event streaming.
- **Apache Spark Streaming**: For processing data in real-time.
- **Minio**: Local S3-compatible storage for persisting data (optional).
- **Docker**: Used for orchestrating the environment.
- **Prometheus + Grafana**: For system monitoring and visualization.

## 🗂️ Project Structure

```plaintext
project_root/
├── api/                     # FastAPI code to receive events
├── pyspark/apps/            # Spark Streaming code to process events
├── config/                  # Configuration files (Kafka, Logging, etc.)
├── tests/                   # Automated tests for the project
├── docker-compose.yml       # Docker Compose to orchestrate containers
├── Dockerfile               # Docker image for the FastAPI app
└── README.md                # Documentation for the project
  
