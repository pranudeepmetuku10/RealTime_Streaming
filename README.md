# Real-Time Data Streaming Pipeline

## Table of Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

A production-ready real-time data streaming pipeline that processes and analyzes data using modern distributed systems. This project demonstrates the integration of TCP/IP sockets, Apache Spark, Apache Kafka, and Elasticsearch to build a scalable end-to-end data engineering solution with real-time sentiment analysis capabilities.

## Architecture

![System Architecture](assets/System_architecture.png)

### Pipeline Components

- **Data Ingestion**: TCP/IP Socket streaming for network data transmission
- **Stream Processing**: Apache Spark cluster (master-worker architecture)
- **Message Broker**:  Confluent Kafka for distributed event streaming
- **Monitoring**:  Kafka Control Center and Schema Registry
- **Data Integration**: Kafka Connect for sink/source connectors
- **Search & Analytics**: Elasticsearch for real-time indexing and querying
- **AI Integration**: OpenAI API for sentiment analysis

## Features

- ✅ Real-time data ingestion via TCP/IP sockets
- ✅ Distributed stream processing with Apache Spark
- ✅ Event-driven architecture using Kafka
- ✅ Sentiment analysis powered by OpenAI LLM
- ✅ Scalable data storage and search with Elasticsearch
- ✅ Dockerized deployment for easy setup
- ✅ Schema management and monitoring

## Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| TCP/IP | Network data streaming |
| Apache Kafka | Distributed event streaming |
| Apache Spark | Distributed data processing |
| Elasticsearch | Search and analytics engine |
| Docker | Containerization |
| OpenAI API | Sentiment analysis |

## Prerequisites

- Docker and Docker Compose installed
- Python 3.8+
- Git
- Confluent Cloud account (or local Kafka setup)
- OpenAI API key (for sentiment analysis)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/pranudeepmetuku10/RealTime_Streaming.git
   cd RealTime_Streaming
   ```

2. **Set up environment variables**
   ```bash
   cp .env.example . env
   # Edit .env with your configurations
   ```

3. **Start the services**
   ```bash
   docker-compose up -d
   ```

4. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Start the data producer**
   ```bash
   python src/data_producer.py
   ```

2. **Run the Spark streaming job**
   ```bash
   spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.x.x \
                src/spark_streaming. py
   ```

3. **Access the monitoring dashboards**
   - Spark UI: http://localhost:8080
   - Kafka Control Center: http://localhost:9021
   - Elasticsearch: http://localhost:9200

## Project Structure

```
RealTime_Streaming/
├── assets/              # Images and diagrams
├── config/              # Configuration files
├── data/                # Sample datasets
├── src/
│   ├── data_producer.py    # TCP socket producer
│   ├── spark_streaming.py  # Spark processing logic
│   ├── kafka_producer.py   # Kafka producer
│   └── sentiment_analysis.py  # OpenAI integration
├── docker-compose.yml   # Docker services
├── requirements.txt     # Python dependencies
└── README. md
```

⭐ Star this repository if you found it helpful!
```
