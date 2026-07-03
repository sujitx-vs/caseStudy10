# Social Media Sentiment Analysis using Apache Spark

## Overview

This project implements a complete **Social Media Sentiment Analysis** pipeline using **Apache Spark (PySpark)**. It demonstrates distributed data processing, exploratory data analysis, Spark SQL, ETL pipeline development, sentiment classification using Spark MLlib, and DevOps practices including Docker containerization, Kubernetes deployment, and CI/CD automation with GitHub Actions.

The project was developed as part of a Big Data Analytics case study to showcase the end-to-end lifecycle of a modern data engineering application.

---

## Features

- Distributed data processing using Apache Spark
- DataFrame transformations and analytics
- RDD transformations and actions
- Spark SQL queries for data analysis
- Exploratory Data Analysis (EDA)
- ETL pipeline implementation
- Sentiment classification using Spark MLlib
- Docker containerization
- Kubernetes deployment
- GitHub Actions CI/CD pipeline

---

## Technology Stack

| Category | Technology |
|----------|------------|
| Programming Language | Python 3.13 |
| Big Data Framework | Apache Spark 4.x |
| Library | PySpark |
| Machine Learning | Spark MLlib |
| Runtime | Java 21 |
| Development | VS Code & Jupyter Notebook |
| Containerization | Docker |
| Container Orchestration | Kubernetes (Docker Desktop) |
| CI/CD | GitHub Actions |
| Version Control | Git & GitHub |

---

## Project Workflow

```text
CSV Dataset
      │
      ▼
Spark Session
      │
      ▼
Data Loading
      │
      ▼
Data Cleaning
      │
      ▼
RDD Operations
      │
      ▼
DataFrame Operations
      │
      ▼
Spark SQL Analytics
      │
      ▼
Exploratory Data Analysis
      │
      ▼
ETL Pipeline
      │
      ▼
Spark MLlib Sentiment Classification
      │
      ▼
Docker Container
      │
      ▼
Kubernetes Deployment
      │
      ▼
GitHub Actions CI/CD
```

---

## Dataset

The dataset consists of social media posts with engagement metrics and sentiment labels.

### Dataset Columns

- Post ID
- Post Content
- Sentiment Label
- Number of Likes
- Number of Shares
- Number of Comments
- User Follower Count
- Post Date and Time
- Post Type
- Language

---

## Project Structure

```text
CaseStudy10/
│
├── sentiment_analysis.ipynb
├── dataset.csv
├── requirements.txt
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── README.md
└── TECHNICAL_DOCUMENTATION.md
```

---

## Key Functionalities

- Distributed processing using Spark DataFrames
- Basic RDD transformations and actions
- Spark SQL analytics
- Sentiment distribution analysis
- Engagement analysis
- Influential user identification
- ETL pipeline development
- Logistic Regression sentiment classification
- Docker image creation
- Kubernetes deployment
- Automated CI/CD pipeline

---

## Getting Started

### Clone the Repository

```bash
git clone <repository-url>
cd CaseStudy10
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Notebook

```bash
jupyter notebook
```

### Build Docker Image

```bash
docker build -t social-media-sentiment .
```

### Run Docker Container

```bash
docker run -p 8888:8888 social-media-sentiment
```

### Deploy to Kubernetes

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

---

## Future Enhancements

- TF-IDF and Word2Vec feature extraction
- BERT-based sentiment analysis
- Real-time Spark Streaming
- Apache Kafka integration
- Interactive dashboards
- Cloud deployment (AWS, Azure, GCP)
- Automated Kubernetes deployment from GitHub Actions

---

## License

This project was developed for educational and academic purposes.