# 🚀 Data Engineering Portfolio

Selamat datang di repository portofolio Data Engineering saya. Repository ini merangkum arsitektur, pipeline data, dan solusi analitik yang telah saya rancang dan implementasikan, mencakup pemrosesan **Batch (ELT)** hingga **Real-time Streaming**. 

Informasi mengenai diri saya dapat dilihat di [Ilham Zamzami](https://www.linkedin.com/in/ilham-zamzami-971631296/)

---

## 👨‍💻 Profil Singkat
- **Role Target:** Data Engineer / Analytics Engineer
- **Core Focus:** End-to-End Data Pipeline Architecture, Data Warehousing, Data Lakehouse, & Real-time Analytics.
- **Tech Stack Utama:** 
  - **Languages:** Python, SQL, Bash
  - **Processing & Streaming:** Apache Kafka, Apache Spark Streaming, DuckDB
  - **Orchestration & Transformation:** Apache Airflow, dbt
  - **Storage & Databases:** PostgreSQL, SeaweedFS / MinIO (S3-compatible)
  - **Containerization & Environment:** Docker, Docker Compose, Linux (WSL2)

---

## 📌 Highlight Projects

| Project Name | Architecture Type | Key Technologies | Main Impact / Focus |
| :--- | :--- | :--- | :--- |
| [**1. AdventureWorks HR & Workforce Analytics**](#1-adventureworks-hr-attrition--workforce-analytics-elt-pipeline) | Batch ELT / Lakehouse | PostgreSQL, SeaweedFS, DuckDB, Airflow | Lakehouse architecture for HR attrition metrics & automated ELT pipeline. |
| [**2. Real-Time Data Streaming Pipeline**](#2-building-real-time-data-pipelines-with-kafka-and-spark-streaming) | Real-Time Streaming | Apache Kafka, Apache Spark Streaming, Docker | Low-latency streaming pipeline for event-driven data ingestion. |

---

## 🛠️ Detailed Project Summaries

### 1. AdventureWorks HR Attrition & Workforce Analytics ELT Pipeline
*Local ELT Data Lakehouse Architecture*

- **Repository Link:** [ZamzamiIlham/AdventureWorks-HR-Attrition-Workforce-Analytics-ELT-Pipeline](https://github.com/ZamzamiIlham/AdventureWorks-HR-Attrition-Workforce-Analytics-ELT-Pipeline)
- **Problem Statement:** Membangun infrastruktur pipeline data otomatis untuk menganalisis turnover dan performa tenaga kerja dari OLTP HR database secara efisien tanpa membebani database operasional.
- **Architecture Highlights:**
  - **Extraction & Ingestion:** Data diekstrak dari **PostgreSQL** (Source OLTP) secara periodik.
  - **Object Storage (Data Lake):** Disimpan di **SeaweedFS** (S3-compatible object storage) sebagai raw zone (Parquet/CSV format).
  - **Data Warehouse / OLAP:** Ingestion dan query analitis menggunakan **DuckDB** untuk kalkulasi metrik HR secara cepat.
  - **Orchestration:** Diorkestrasi secara penuh menggunakan **Apache Airflow** yang berjalan di atas Docker Compose.
- **Key Learnings & Deliverables:**
  - Merancang skema data marts khusus untuk metrik *HR Attrition Rate* dan *Workforce Distribution*.
  - Mengimplementasikan pola Data Lakehouse lokal yang efisien dalam penggunaan resource memori/CPU.

---

### 2. Building Real-Time Data Pipelines with Kafka and Spark Streaming
*Event-Driven Streaming Architecture*

- **Repository Link:** [ZamzamiIlham/Building-Real-Time-Data-Pipelines-with-Kafka-and-Spark-Streaming](https://github.com/ZamzamiIlham/Building-Real-Time-Data-Pipelines-with-Kafka-and-Spark-Streaming)
- **Problem Statement:** Mengolah aliran data berkecepatan tinggi (high-velocity stream) secara real-time dengan latensi rendah untuk kebutuhan pemantauan dan pemrosesan berlanjut.
- **Architecture Highlights:**
  - **Message Broker:** **Apache Kafka** sebagai platform pub/sub untuk menangani *ingestion rate* yang tinggi.
  - **Stream Processing:** **Apache Spark Streaming** untuk mentransformasi, memfilter, dan melakukan pemrosesan data terdistribusi secara *real-time*.
  - **Infrastructure:** Seluruh layanan (*Broker, Zookeeper/KRaft, Spark Master & Worker*) di-deploy menggunakan **Docker Compose** terisolasi.
- **Key Learnings & Deliverables:**
  - Menangani *windowing aggregations* dan penanganan *out-of-order data* pada Spark Streaming.
  - Optimasi *producer-consumer configurations* di Kafka untuk throughput optimal.

---

## 🌐 Hubungi Saya
- **LinkedIn:** [Ilham Zamzami](https://www.linkedin.com/in/ilham-zamzami-971631296/)
- **Email:** zamzamilham17@gmail.com
