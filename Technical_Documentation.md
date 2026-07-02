# Technical Documentation

## Project Overview

This project implements a Social Media Sentiment Analysis pipeline using
Apache Spark (PySpark). It demonstrates distributed data processing, RDD
operations, DataFrame transformations, Spark SQL analytics, an ETL
pipeline, and a Spark MLlib sentiment classification model.

## Objectives

-   Distributed data processing
-   RDD and DataFrame APIs
-   Spark SQL analytics
-   ETL pipeline
-   Baseline sentiment classification

## Technology Stack

-   Python 3.x
-   Apache Spark 4.1.2
-   PySpark
-   Java 21
-   VS Code + Jupyter Notebook

## Dataset Schema

-   Post ID
-   Post Content
-   Sentiment Label
-   Number of Likes
-   Number of Shares
-   Number of Comments
-   User Follower Count
-   Post Date and Time
-   Post Type
-   Language

## Architecture

CSV -\> SparkSession -\> DataFrame -\> Cleaning -\> RDD -\> Spark SQL
-\> ETL -\> Spark MLlib

## Components

### Spark Initialization

SparkSession, local\[\*\], schema inference, multiline CSV.

### RDD

DataFrame to RDD, map, filter, reduceByKey, groupByKey, cache/persist.

### DataFrame

select, filter, groupBy, agg, orderBy, withColumn.

### Spark SQL

Temporary view and SQL analytics for sentiment, engagement, influential
users and trends.

### ETL

Extract CSV, transform (drop nulls, trim, normalize), load to Parquet
(requires Hadoop configuration on Windows for writing).

### Machine Learning

Tokenizer -\> HashingTF -\> StringIndexer -\> LogisticRegression.

## Limitations

-   Synthetic-looking dataset.
-   No topic/hashtag column.
-   Windows Parquet output may require HADOOP_HOME.

## Future Work

TF-IDF, Word2Vec, streaming, dashboards, hyperparameter tuning.
