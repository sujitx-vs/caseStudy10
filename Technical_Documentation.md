# Technical Documentation

# Social Media Sentiment Analysis using Apache Spark

---

# 1. Project Overview

This project implements a distributed Social Media Sentiment Analysis system using Apache Spark (PySpark). It demonstrates the complete Big Data processing lifecycle, including distributed data processing, RDD and DataFrame operations, Spark SQL analytics, ETL pipeline development, Machine Learning-based sentiment classification, and modern DevOps practices using Docker, Kubernetes, and GitHub Actions.

The project is designed to showcase both Big Data Analytics and DevOps deployment concepts.

---

# 2. Project Objectives

The primary objectives of this project are:

- Process social media datasets using Apache Spark.
- Demonstrate distributed computing using Spark DataFrames.
- Implement basic RDD transformations and actions.
- Perform exploratory data analysis using Spark SQL.
- Develop a complete ETL pipeline.
- Build a sentiment classification model using Spark MLlib.
- Containerize the application using Docker.
- Deploy the application using Kubernetes.
- Automate build and deployment using GitHub Actions.

---

# 3. Technology Stack

| Component | Technology |
|------------|------------|
| Programming Language | Python 3.13 |
| Big Data Framework | Apache Spark 4.x |
| Library | PySpark |
| Machine Learning | Spark MLlib |
| Development Environment | VS Code |
| Notebook | Jupyter Notebook |
| Containerization | Docker |
| Container Orchestration | Kubernetes (Docker Desktop) |
| CI/CD | GitHub Actions |
| Runtime | Java 21 |
| Version Control | Git & GitHub |

---

# 4. Dataset Description

The dataset contains social media posts along with user engagement statistics.

## Dataset Schema

| Column | Data Type |
|----------|----------|
| Post ID | String |
| Post Content | String |
| Sentiment Label | String |
| Number of Likes | Integer |
| Number of Shares | Integer |
| Number of Comments | Integer |
| User Follower Count | Integer |
| Post Date and Time | Timestamp |
| Post Type | String |
| Language | String |

---

# 5. System Architecture

```

CSV Dataset
│
▼
SparkSession
│
▼
Spark DataFrame
│
├── Data Cleaning
│
├── RDD Operations
│
├── DataFrame Operations
│
├── Spark SQL Analytics
│
├── ETL Pipeline
│
├── Machine Learning
│
▼
Processed Dataset (Parquet)
│
▼
Docker Container
│
▼
Kubernetes Deployment
│
▼
GitHub Actions CI/CD Pipeline

```

---

# 6. Project Components

## 6.1 Spark Session Initialization

The project begins by creating a SparkSession that acts as the entry point for all Spark operations.

Features:

- Local execution
- Automatic schema inference
- CSV file loading
- Timestamp parsing

---

## 6.2 DataFrame Operations

The dataset is processed primarily using Spark DataFrames.

Operations implemented:

- select()
- filter()
- withColumn()
- groupBy()
- orderBy()
- agg()
- dropDuplicates()
- dropna()

These operations are executed using Spark's distributed execution engine.

---

## 6.3 RDD Operations

Although DataFrames are the preferred API, RDD operations were implemented to demonstrate Spark's low-level programming model.

Operations performed:

- DataFrame → RDD conversion
- map()
- filter()
- reduceByKey()
- groupByKey()
- collect()
- count()

Example use case:

- Extract positive sentiment records
- Count posts by sentiment
- Perform key-value operations

---

## 6.4 Key-Value Operations

Key-value transformations were implemented using RDDs.

Implemented operations include:

- map()
- reduceByKey()
- groupByKey()
- sortByKey()

These operations demonstrate distributed aggregation across partitions.

---

## 6.5 Persistence

RDD persistence was implemented using:

```

cache()

```

and

```

persist()

```

Purpose:

- Avoid recomputation
- Improve iterative processing performance
- Reuse intermediate datasets efficiently

---

## 6.6 Exploratory Data Analysis

EDA was performed using DataFrame APIs.

Analysis includes:

- Sentiment distribution
- Engagement statistics
- Most active post types
- Language distribution
- Average likes, shares and comments

---

## 6.7 Spark SQL

A temporary SQL view was created from the DataFrame.

SQL queries were executed to analyze:

- Sentiment distribution
- Trending content
- Highly influential users
- Engagement metrics
- Daily sentiment trends

Spark SQL provides SQL-like querying capabilities over distributed datasets.

---

## 6.8 ETL Pipeline

A complete ETL pipeline was implemented.

### Extract

- Read CSV dataset

### Transform

- Remove null values
- Trim whitespace
- Normalize text
- Convert timestamp
- Remove duplicates

### Load

- Store processed data in Parquet format

The ETL workflow prepares clean data for downstream analytics.

---

## 6.9 Machine Learning

Spark MLlib was used to implement a baseline sentiment classification model.

Pipeline Components:

- Tokenizer
- HashingTF
- StringIndexer
- Logistic Regression

Evaluation Metric:

- Accuracy

This demonstrates the integration of machine learning within Spark.

---

# 7. Docker Containerization

The project was containerized using Docker.

Docker implementation includes:

- Python runtime
- Java installation
- Apache Spark dependencies
- Project source code
- Jupyter Notebook execution

Benefits:

- Portability
- Environment consistency
- Easy deployment

---

# 8. Kubernetes Deployment

The Docker container was deployed on a Kubernetes cluster.

Files created:

- deployment.yaml
- service.yaml

Deployment includes:

- Replica management
- Pod scheduling
- Service exposure
- Container orchestration

The application was successfully deployed using Docker Desktop Kubernetes.

---

# 9. CI/CD Pipeline

A GitHub Actions workflow was implemented.

Pipeline stages:

1. Checkout repository
2. Install Python
3. Install dependencies
4. Run basic validation
5. Build Docker image
6. Deployment stage

This demonstrates a basic Continuous Integration and Continuous Deployment workflow.

---

# 10. Performance Characteristics

Apache Spark improves processing efficiency through:

- Distributed execution
- Data partitioning
- Parallel processing
- Lazy evaluation
- DAG optimization
- In-memory computation
- Fault tolerance
- Persistence

---

# 11. Project Limitations

- Dataset contains limited sentiment classes.
- Trending topic detection is based on post engagement rather than NLP topic modeling.
- ML model serves as a baseline classifier.
- Local Kubernetes deployment only.
- Windows Parquet output requires Hadoop configuration.

---

# 12. Future Enhancements

Possible future improvements include:

- TF-IDF feature extraction
- Word2Vec embeddings
- BERT-based sentiment classification
- Real-time Spark Streaming
- Kafka integration
- Interactive dashboards
- Model hyperparameter tuning
- Cloud deployment (AWS, Azure, GCP)
- Automated Kubernetes deployment through GitHub Actions

---

# 13. Conclusion

This project successfully demonstrates the complete workflow of a modern Big Data analytics application. It combines Apache Spark for distributed processing, Spark SQL for analytics, Spark MLlib for sentiment classification, Docker for containerization, Kubernetes for orchestration, and GitHub Actions for CI/CD automation.

The implementation provides a practical understanding of scalable data processing and modern DevOps practices while satisfying all the requirements of the case study.