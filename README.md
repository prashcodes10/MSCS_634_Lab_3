# MSCS_634_Lab_3 – Clustering Analysis using K-Means and K-Medoids

## Introduction

In this lab, clustering techniques were applied to the Wine dataset available in scikit-learn. The main goal was to implement and compare K-Means and K-Medoids algorithms in order to analyze how each method groups similar data points.

To evaluate clustering performance, two metrics were used:
- Silhouette Score to measure cluster compactness and separation
- Adjusted Rand Index (ARI) to compare predicted clusters with actual class labels

---

## Dataset Description

The Wine dataset consists of 178 samples with 13 numerical features representing chemical characteristics of different wine cultivars. The dataset contains three distinct classes.

Before performing clustering, the data was standardized using Z-score normalization. This ensured that all features contributed equally to the clustering process and prevented scale dominance.

---

## Methodology

### K-Means Clustering
- Number of clusters set to 3
- Applied to standardized data
- Cluster centers calculated as the mean of assigned points
- Performance evaluated using Silhouette Score and ARI

### K-Medoids Clustering
- Number of clusters set to 3
- Implemented manually due to compatibility limitations with Python 3.13
- Medoids selected as actual data points minimizing intra-cluster distances
- Evaluated using the same performance metrics for fair comparison
## Results and Observations

- K-Means generated slightly more compact clusters based on Silhouette Score.
- ARI results indicated strong agreement between clustering output and actual class labels.
- K-Means performed efficiently on this structured dataset.
- K-Medoids showed greater robustness since cluster centers were real observations.

### Comparative Insights

- K-Means minimizes squared Euclidean distance and generally works well for spherical and well-separated clusters.
- K-Medoids minimizes overall pairwise distance, making it more resistant to outliers.
- For datasets with clear separation like Wine, K-Means tends to perform slightly better.
- For datasets with noise or extreme values, K-Medoids may be more reliable.

---

## Challenges

- The scikit-learn-extra library was incompatible with Python 3.13, requiring a manual implementation of K-Medoids.
- Visualizing high-dimensional data required reducing it to two features for plotting.
- Proper feature scaling was essential to obtain meaningful clustering results.

---

## Summary

This lab provided practical experience in unsupervised learning and cluster evaluation. By comparing K-Means and K-Medoids, we observed how different optimization strategies influence cluster formation and performance.

Overall, both algorithms successfully captured the underlying structure of the Wine dataset, with K-Means showing slightly stronger compactness and K-Medoids offering improved robustness.
