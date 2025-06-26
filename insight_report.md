# Clustering Insights Report: Facebook Live Sellers Dataset

## 🎯 Purpose

To understand if Facebook post engagement patterns naturally group into meaningful clusters — and if these clusters relate to the post type (`status_type`).

---

## 🔍 Key Observations

### 1. **Optimal Clusters**
- Based on Elbow and Silhouette methods, **4 clusters** provided the best balance of cohesion and separation.

### 2. **Cluster Behavior Patterns**
| Cluster | Engagement Pattern |
|--------|---------------------|
| 0      | High likes, medium comments, very low emoji reactions |
| 1      | High shares and comments, moderate likes |
| 2      | Low engagement across all metrics (possibly link/status posts) |
| 3      | High loves and haha reactions — indicative of viral/entertaining content |

---

## 🔄 Status Type Alignment

While `status_type` was not used for clustering, we evaluated alignment after clustering:
- **Cluster 0**: Dominated by photo posts
- **Cluster 1**: Contained mix of video and photo
- **Cluster 2**: Mostly status or link types (low engagement)
- **Cluster 3**: Mostly video posts with emotional reactions

This shows that the clustering could **infer content types based on engagement** without using the label.

---

## 📈 Visual Analysis

- **PCA (2D)** showed clear separation of clusters.
- Outliers were minimal and did not heavily skew centroids.

---

## ✅ Conclusions

- K-Means successfully revealed natural groupings based on post engagement.
- Cluster analysis provides actionable insights for Facebook marketers:
  - Which type of post gets shared the most?
  - What drives emotional engagement?
  - Which posts receive low traction?

This analysis can help tailor content strategy to target specific engagement goals.

---

## 🧩 Next Steps

- Perform time-series clustering by extracting hour/day from `status_published`.
- Try DBSCAN or Hierarchical Clustering to validate structure.
- Use clustering results to recommend post types to new sellers.
