# Streaming Data Architecture 🚀

## Description
This repository contains a complete streaming architecture for managing real-time data flows. It is designed for data professionals who need to process continuous streams of information, ensuring robust and scalable ingestion, processing, and visualization. 🔄

### Main Components:
- **Streaming Infrastructure (Kafka) ⚙️:** 
  - Setup and configuration of a Kafka cluster for receiving and distributing messages.
  - Definition of topic schemas and reliable ingestion via a Kafka producer in Python.
- **Real-Time Processing (PySpark) 🔥:** 
  - Consumes event streams using PySpark Structured Streaming.
  - Applies transformations and computes aggregates (e.g., average age, geographical distribution).
- **Data Storage 💾:**
  - Stores raw data in **MongoDB** for maximum flexibility.
  - Inserts aggregates into **Cassandra** to ensure fast and scalable queries.
- **Visualization and Monitoring (Streamlit) 📊:**
  - Interactive dashboard displaying the latest users and their real-time statistics.
  - Dynamic refresh for effective monitoring of the data pipeline.
- **Validation and Scalability ✅:**
  - Resilience tests to handle load spikes.
  - Optimization of Kafka and PySpark parameters for optimal performance.
  - Implementation of data governance mechanisms for quality and compliance (GDPR).

## Architecture

The architecture is divided into several layers:

1. **Ingestion 📥:** 
   - Kafka captures and distributes messages through a dedicated topic (`user_events`).

2. **Processing ⚙️:**
   - PySpark Structured Streaming connects to Kafka topics to consume, transform, and aggregate data in real-time.

3. **Storage 💾:**
   - **MongoDB** stores raw data.
   - **Cassandra** hosts aggregates for fast queries and high availability.

4. **Visualization 📊:**
   - An interactive dashboard built with Streamlit monitors the data pipeline in real-time.

5. **Orchestration 🎛️:**
   - Docker Compose orchestrates and deploys all services (Kafka, Zookeeper, MongoDB, Cassandra).

![Architecture Diagram](./docs/architecture.png)  
*(Add an architecture image here if needed)*

## Installation

### Prerequisites 📋
- Docker and Docker Compose
- Python 3.8+
- Spark (to run the PySpark application)

### Deployment

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/streaming-data-architecture.git
   cd streaming-data-architecture
   ```
## Installation Steps

### 1. Install Python Dependencies 🐍
```bash
pip install -r requirements.txt
```

### 2. Start the Services with Docker Compose 🐳
```bash
docker-compose up -d
```

### 3. Launch the Applications 🚀
#### Kafka Producer:
```bash
python producer/kafka_producer.py
```
#### Pyspark Application
```bash
spark-submit pyspark/streaming_app.py
```
#### Streamlit Dashboard:
```bash
streamlit run dashboard/streamlit_dashboard.py
```

### Contribute 🤝
Contributions are welcome! Please submit a pull request or open an issue to discuss your improvements.

