# End-to-End Realtime Data Streaming Pipeline

## Overview

This project builds a comprehensive real-time data streaming pipeline for a Smart City application, covering each phase from data ingestion to processing and finally storage. The system uses various cutting-edge tools and technologies to collect, process, and visualize data from IoT devices in real-time. The data includes vehicle information, GPS data, camera feeds, weather conditions, and emergency incidents. This solution is ideal for urban monitoring and management, providing timely and actionable insights.

## Features

- **Real-time Data Ingestion**: Continuous data collection from IoT devices, including vehicle telemetry, GPS coordinates, camera images, weather data, and emergency reports.
- **Apache Kafka Integration**: High-throughput, low-latency platform for handling real-time data streams.
- **Apache Spark Streaming**: Real-time data processing and analytics with Spark.
- **AWS Integration**: Data storage and management using AWS S3, Glue, Athena, IAM, and Redshift.
- **Visualization**: Data insights visualization using PowerBI, Tableau, and Looker Studio.

## Technologies Used

- **IoT Devices**: Sensors and devices for collecting vehicle, GPS, camera, weather, and emergency data.
- **Apache Zookeeper**: Coordination service for managing Kafka clusters.
- **Apache Kafka**: Distributed streaming platform for real-time data pipelines.
- **Apache Spark**: Unified analytics engine for large-scale data processing.
- **Docker**: Containerization platform for packaging and deploying applications.
- **Python**: Programming language for developing the data processing pipeline.
- **AWS Cloud**: Cloud services for data storage, cataloging, querying, and visualization (S3, Glue, Athena, IAM, Redshift).
- **PowerBI, Tableau, Looker Studio**: Data visualization tools for generating actionable insights.

## Architecture

![System Architecture](path/to/architecture-diagram.png)

## Prerequisites

- Docker and Docker Compose
- AWS Account with S3 and IAM setup
- Python 3.9 or later
- Apache Kafka

## Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/smart-city-pipeline.git
cd smart-city-pipeline
```

### Step 2: Configure AWS Credentials

Create a `config.py` file in the `jobs` directory with your AWS credentials.

```python
# jobs/config.py
configuration = {
    "AWS_ACCESS_KEY": "your-access-key",
    "AWS_SECRET_KEY": "your-secret-key"
}
```

### Step 3: Set Up Docker

Ensure Docker and Docker Compose are installed on your machine. Then, start the Docker services.

```bash
docker-compose up -d
```

### Step 4: Install Python Dependencies

Create a virtual environment and install the required Python packages.

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Step 5: Run the Project

Run the main script to start collecting and processing data.

```bash
python jobs/main.py
```

## Usage

### Viewing the Data

The processed data is stored in an AWS S3 bucket. You can use AWS Athena or any other querying tool to access the data.

### Visualization

You can visualize the data using PowerBI, Tableau, or Looker Studio. Connect these tools to your AWS S3 bucket or Redshift for real-time insights.
