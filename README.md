# Hierarchical Clustering Analysis

This directory contains an implementation of **Hierarchical Clustering**, an unsupervised learning method used to discover natural groupings in data by building a hierarchy of clusters.

## Dataset Overview

The model uses the `Mall_Customers.csv` dataset, which includes:

- **Features Used**:
  - `Annual Income (k$)`: Annual income of the customer.
  - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature.
- **Goal**: Segment customers into distinct groups to better understand their profiles.

## Implementation Steps

The implementation follows these key steps:

1.  **Data Preprocessing**:
    - Importing libraries (`numpy`, `matplotlib`, `pandas`).
    - Extracting features (Annual Income and Spending Score).
2.  **Finding Optimal Clusters**:
    - Used a **Dendrogram** via `scipy.cluster.hierarchy`.
    - Applied the **Ward method** (minimizing variance within clusters).
    - Identified **5 clusters** as the optimal number.
3.  **Model Training**:
    - Used `sklearn.cluster.AgglomerativeClustering`.
    - Parameters: `n_clusters = 5`, `affinity = 'euclidean'`, and `linkage = 'ward'`.
4.  **Visualization**:
    - Plotted the 5 clusters with colored markers to showcase clear customer segmentation.

## Results

The Hierarchical Clustering algorithm successfully categorized the customers into 5 groups:

- **Cluster 1**: Average Income, Average Spending.
- **Cluster 2**: High Income, Low Spending.
- **Cluster 3**: Low Income, Low Spending.
- **Cluster 4**: Low Income, High Spending.
- **Cluster 5**: High Income, High Spending.

This segmentation allows for targeted marketing strategies based on customer behavior.
