Mani-Jafari

The K-Means Clustering algorithm was applied to the dataset to identify natural groups based on two numerical features, `x` and `y`. The dataset contained **150 observations and 2 features**, with no missing values or duplicate records.

During the exploratory analysis, the data distribution was visualized, and the **Elbow Method** was used to determine an appropriate number of clusters. Based on the WCSS analysis, **3 clusters** were selected for the final K-Means model.

The final model was configured with **3 clusters**, `k-means++` initialization, **10 initializations**, and a maximum of **300 iterations**. The resulting clusters were evenly distributed, with **50 observations in each cluster**.

### Key Performance Metrics

* **Silhouette Score:** 0.6708
* **Number of Clusters:** 3
* **Cluster 0:** 50 samples
* **Cluster 1:** 50 samples
* **Cluster 2:** 50 samples
* **Total Samples:** 150
* **Missing Values:** 0
* **Duplicate Records:** 0

The model achieved a **Silhouette Score of 0.6708**, indicating a relatively strong clustering structure with good separation between the identified groups and reasonable cohesion within each cluster.

Overall, the K-Means model successfully identified **three well-defined and balanced clusters** in the dataset. The combination of the Elbow Method and Silhouette Score provides good evidence that the selected clustering structure is meaningful for this dataset.

