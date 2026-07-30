# 🎌 Anime Recommendation System

> End-to-end anime recommendation system on 148M+ ratings using Apache Spark, Databricks, and 6 ML models.

---

## 📌 Project Overview

An end-to-end Machine Learning pipeline built on **Apache Spark (Databricks)** 
processing **148M+ user-anime interaction records** across **20,237 anime titles** and **325K+ users**.

---

## 🔧 What This Project Does

| Step | Description |
|------|-------------|
| **Ingestion** | Extracts compressed datasets from Unity Catalog Volumes into Bronze layer Delta tables |
| **Cleaning** | Fault-tolerant cleaning using Spark SQL `try_cast`, IQR outlier capping, deduplication |
| **EDA** | Rating distributions, genre frequency, user activity, anime popularity power-law |
| **Task 1** | User segmentation — K-Means vs DBSCAN with PCA visualization |
| **Task 2** | Content-based filtering — TF-IDF + Cosine Similarity vs KNN |
| **Task 3** | Collaborative filtering — ALS (RMSE: 1.3488) vs SVD |
| **Insights** | Hidden gems discovery — high quality anime with low exposure |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)

- **Platform:** Databricks Serverless · Unity Catalog · Delta Lake
- **Big Data:** Apache Spark · PySpark · Spark MLlib
- **ML Models:** ALS · SVD · K-Means · DBSCAN · PCA · TF-IDF · KNN
- **Libraries:** Scikit-Learn · Scikit-Surprise · Pandas · NumPy · Matplotlib

---

## 📊 Dataset

- **Source:** [User Animelist Dataset — Kaggle](https://www.kaggle.com/datasets/ramazanturann/user-animelist-dataset)
- **Size:** 148M+ ratings · 20,237 anime · 325K+ users
- **Files used:** `ratings.csv` · `animes.csv`

---

## 📈 Model Results

| Model | Type | Data | RMSE | MAE |
|-------|------|------|------|-----|
| ALS Default | Collaborative Filtering | 100M rows | ~1.40 | ~1.05 |
| **ALS Tuned** | Collaborative Filtering | 100M rows | **1.3488** | **0.9941** |
| SVD | Collaborative Filtering | 1M sample | ~1.55 | ~1.10 |

**Best params:** rank=10 · regParam=0.1 · nonnegative=True

---

## 🗂️ Project Structure
