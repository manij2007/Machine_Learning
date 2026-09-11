Mani-Jafari

The Mean Shift Clustering algorithm was applied to a synthetically generated dataset to identify natural groups based on two numerical features.

The dataset was created using `make_blobs` and contained **1,000 observations** distributed across four predefined regions with different centers and cluster standard deviations. The data consisted of **2 numerical features**, and an initial scatter plot was used to visualize the overall structure.

As an exploratory step, the **Elbow Method** was also applied using K-Means to examine the within-cluster sum of squares (WCSS) for different numbers of clusters. However, the final clustering model was based on Mean Shift rather than K-Means.

For the Mean Shift model, the bandwidth was estimated automatically using `estimate_bandwidth` with a `quantile` value of **0.25**. The resulting bandwidth was then used to train the final Mean Shift model.

### Key Performance Metrics

* **Total Samples:** 1,000
* **Number of Features:** 2
* **Detected Clusters:** 4
* **Bandwidth Estimation:** `estimate_bandwidth`
* **Quantile:** 0.25
* **Clustering Method:** Mean Shift
* **Missing Values:** Not applicable
* **Duplicate Records:** Not applicable
* **Silhouette Score:** Not calculated in the notebook

The final Mean Shift model successfully identified **four distinct clusters**, as confirmed by the unique cluster labels `[0, 1, 2, 3]`. The resulting groups were then visualized using a scatter plot, providing a clear representation of the identified cluster structure.

Overall, the Mean Shift algorithm successfully detected the underlying grouping structure without requiring the number of clusters to be explicitly specified. The automatic bandwidth estimation provided a practical way to control the clustering behavior and allowed Mean Shift to identify the four groups present in the generated dataset.

Since no quantitative clustering evaluation metric was calculated in the notebook, the quality of the clusters was assessed primarily through the resulting cluster structure and visualization.
