Mani-Jafari

The DBSCAN clustering algorithm was applied to the `Spiral.csv` dataset to identify natural groups within the data based on two numerical features. The dataset contained **311 observations and 3 columns**, with no missing values or duplicate records.

During the exploratory analysis, the first two numerical features were selected for clustering and visualized to understand the structure of the dataset. The **K-Means Elbow Method** was also used as an exploratory technique to examine the appropriate number of clusters before applying the final clustering algorithm.

DBSCAN was then trained using **eps = 3** and **min_samples = 5**. The model identified **three distinct clusters** without assigning any observations as noise.

### Key Performance Metrics

* **Number of Clusters:** 3
* **Cluster 0:** 105 samples
* **Cluster 1:** 101 samples
* **Cluster 2:** 105 samples
* **Total Samples:** 311
* **Noise Points:** 0
* **Duplicate Records:** 0
* **Missing Values:** 0

The resulting clusters were visualized to show the separation between the three groups. The nearly balanced cluster sizes indicate that DBSCAN successfully identified three major structures within the spiral-shaped dataset.

Overall, the DBSCAN model provided a clear clustering structure for this dataset and successfully separated the observations into **three clusters with no detected noise points**. The visualization also provides an intuitive representation of the resulting groups, making DBSCAN a suitable approach for discovering the underlying structure of this type of spatial dataset.
