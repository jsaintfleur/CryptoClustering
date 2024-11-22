# CryptoClustering

## Overview

This project uses the **K-Means clustering algorithm** and **Principal Component Analysis (PCA)** to classify cryptocurrencies based on their price fluctuations across various timeframes. By leveraging machine learning and dimensionality reduction techniques, we aim to uncover patterns in cryptocurrency behavior and group assets with similar performance characteristics.

---

## Key Features

- **Clustering with K-Means**: Group cryptocurrencies into clusters based on their price changes.
- **Dimensionality Reduction with PCA**: Reduce the complexity of the dataset while preserving essential information.
- **Optimal Clustering**: Use the Elbow Method to determine the best number of clusters for both raw and PCA-transformed data.
- **Visualizations**: Provide clear plots to display clustering results, feature influences, and optimal clustering.

---

## Workflow

### 1. Data Preparation
- Collect cryptocurrency data, focusing on price percentage changes over various timeframes (e.g., 24 hours, 7 days, 30 days).
- Normalize the data using `StandardScaler` to ensure consistent scaling.

### 2. Optimal Cluster Selection
- Apply the **Elbow Method** on both original and PCA-transformed data to identify the optimal number of clusters (`k`).
- Analyze inertia values to determine the "elbow" point, where additional clusters offer diminishing returns.

### 3. Dimensionality Reduction with PCA
- Perform PCA to reduce the dataset's dimensionality to three principal components, retaining the most critical information.
- Analyze the influence of each feature on the principal components using a heatmap.

### 4. Clustering and Visualization
- Apply the K-Means algorithm to both raw and PCA-reduced data.
- Visualize the clusters in a 2D scatter plot to highlight relationships and groupings.
- Compare clustering results between raw and PCA-transformed data.

---

## Results

### Optimal Number of Clusters
- **Original Data**: The Elbow Method suggests an optimal `k = 2`.
- **PCA-Transformed Data**: PCA refinement indicates an optimal `k = 3`.

### Clustering Insights
- Cryptocurrencies were successfully grouped into distinct clusters based on their price percentage changes.
- PCA clusters revealed more nuanced groupings, emphasizing the importance of mid- and short-term metrics.

### Feature Analysis
- **PC1**: Positively influenced by long-term metrics (e.g., `price_change_percentage_1y`) and negatively by short-term changes (`price_change_percentage_24h`).
- **PC2**: Driven by mid-term metrics (e.g., `price_change_percentage_30d`, `price_change_percentage_14d`).
- **PC3**: Dominated by weekly changes (`price_change_percentage_7d`).

---

## Visualizations

1. **Optimal Clustering (Original Data)**
   ![Optimal K Inertia](optimal_k_inertia.png)

2. **Optimal Clustering (PCA Data)**
   ![Elbow Curve for PCA Data](elbow_curve_pca_data.png)

3. **Cluster Visualization**
   ![Cryptocurrency Clusters](cryptocurrency_clusters_price_change_pct.png)

4. **PCA Feature Influence**
   ![PCA Weights Heatmap](pca_weights_heatmap.png)

---

## Future Enhancements

- **Dynamic Data**: Integrate real-time cryptocurrency data for dynamic cluster updates.
- **Additional Features**: Include trading volume, market capitalization, and sentiment analysis to refine clustering.
- **Predictive Modeling**: Combine clustering with forecasting models to predict future price movements and cluster shifts.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

