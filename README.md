# Facebook Live Sellers in Thailand - K-Means Clustering

This project applies **unsupervised machine learning (K-Means Clustering)** to the [Facebook Live Sellers in Thailand dataset](https://archive.ics.uci.edu/ml/datasets/Facebook+Live+Sellers+in+Thailand). The dataset contains information on various types of Facebook posts and their engagement metrics, such as likes, comments, and emoji reactions.

## 📌 Objective

To use **K-Means Clustering** to discover hidden patterns in user engagement across different post types (`status_type`) without using the target label during training.

## 📁 Dataset Description

- **Rows**: 7050
- **Columns**: 12 (Engagement metrics + post metadata)

| Column Name       | Description                                      |
|-------------------|--------------------------------------------------|
| status_id         | ID of the status                                 |
| status_type       | Type of post (video, photo, status, link)       |
| status_published  | Date and time the status was published           |
| num_reactions     | Total reactions to the post                      |
| num_comments      | Number of comments                               |
| num_shares        | Number of shares                                 |
| num_likes         | Count of likes                                   |
| num_loves         | Count of loves                                   |
| num_wows          | Count of wows                                    |
| num_hahas         | Count of hahas                                   |
| num_sads          | Count of sads                                    |
| num_angrys        | Count of angry reactions                         |

## 🔧 Tools Used

- Python
- Pandas, NumPy
- Scikit-learn (KMeans, StandardScaler, PCA)
- Seaborn & Matplotlib for visualization

## 🧪 Steps Followed

1. **Data Cleaning & Preprocessing**
   - Dropped irrelevant and empty columns
   - Encoded categorical data (`status_type`)
   - Standardized numerical features

2. **Clustering**
   - Used Elbow Method and Silhouette Score to find optimal `k`
   - Fit final K-Means model

3. **Evaluation**
   - Compared cluster distribution with actual `status_type`
   - Visualized clusters using PCA

## 📊 Results Summary

- Final model used `k = 4` clusters.
- Clusters showed distinguishable engagement behaviors across post types.
- PCA visualization helped confirm separation of clusters.

## 📎 Files

- `Status_type behavior.ipynb` — Jupyter Notebook with full code
- `insight_report.md` — Insights and observations from clustering
