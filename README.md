# Customer Segmentation and Classification using Clustering and Decision Tree

## 📌 Project Overview

This project aims to segment customers based on their behavior using **Unsupervised Learning (Clustering)** and build a **Classification Model (Decision Tree)** to classify new customers into the discovered clusters. The use case simulates a retail scenario where businesses can tailor marketing strategies, promotions, and loyalty programs more effectively.

## 📂 Dataset Description

- The dataset contains customer information including **numerical features** and **textual reviews/comments**.
- Preprocessing includes:
  - Removing identifier and IP address columns.
  - Text cleaning (lowercase, URL removal, punctuation cleaning).
  - Label encoding for categorical columns.
  - Feature scaling with MinMaxScaler for numerical attributes.

## 🔍 Clustering Stage

- **Algorithm**: K-Means
- **Optimal Cluster Count**: Determined using Elbow Method & Silhouette Score
- **Visualization**: PCA for 2D projection of clusters
- **Model Saved**: `model_clustering.h5`
- **Clustered Data Exported**: `data_clustering.csv`

### ✅ Cluster Interpretation

Each cluster is analyzed based on the mean, min, and max values of each numerical feature (after and before inverse scaling).

## 🤖 Classification Stage

- **Algorithm**: Decision Tree
- **Vectorization**: TF-IDF on cleaned text
- **Train/Test Split**: 80/20
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score

### 📊 Performance Report

Each cluster (from the unsupervised step) is evaluated to see how well the classifier identifies it. Performance is interpreted using classification metrics and comments per class.

## 💡 Insights & Next Steps

- High F1-Score clusters indicate strong separability in the feature space.
- Low-performing clusters may require further feature engineering or data balancing.
- The classifier allows automated classification of new customer reviews into strategic segments.

## 🛠️ Requirements

```bash
scikit-learn
pandas
numpy
matplotlib
seaborn
yellowbrick
joblib
```
install via pip:
```bash
pip install -r requirements.txt
```
Project Structure

- data.csv                    # Original dataset
- data_clustering.csv         # Dataset with added cluster labels
- model_clustering.h5         # Saved KMeans clustering model
- project.ipynb / .py         # Main project notebook or script
- README.md                   # Project description and documentation


📣 Author
Created by Satria Nugraha Saputra
This project is part of a customer insight analysis using machine learning.
