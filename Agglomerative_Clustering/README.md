Mani-Jafari

The Agglomerative Clustering approach was applied to segment 2,000 customers based on demographic and socioeconomic characteristics, including age, education, income, occupation, marital status, sex, and settlement size. The `ID` feature was removed because it does not provide meaningful information for customer segmentation.

The dataset contained no missing values or duplicate records, and the numerical features were standardized using `StandardScaler` before clustering. A hierarchical clustering approach was explored using a dendrogram, and the final model was configured with **2 clusters**, **Ward linkage**, and **Euclidean distance**.

The resulting **Silhouette Score of 0.2363** indicates that the identified clusters have some degree of structure, but the separation between them is relatively weak. Therefore, the dataset does not exhibit strongly separated customer groups under this clustering configuration.

Overall, Agglomerative Clustering provides a useful initial segmentation of the customers, but the relatively low Silhouette Score suggests that alternative clustering methods, distance metrics, or feature representations could potentially produce more distinct and meaningful segments.
