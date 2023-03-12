## README
This code contains the implementation of two algorithms, Agglomerative Clustering and K-Nearest Neighbors (KNN) for classification tasks.

### Requirements
This code requires numpy, pandas and tabulate libraries to be installed.

### Agglomerative Clustering
`Agglomerative Clustering` is a hierarchical clustering algorithm that works by iteratively merging the two closest clusters in the data. The implementation in this code uses three linkage criteria:

*Single Linkage*
*Complete Linkage*
*Average Linkage*

Class
The AgglomerativeClustering class in this code takes two input arguments:

n_clusters: the number of clusters to be formed
linkage: the type of linkage criteria to be used, which can be one of "single", "complete" or "average" (default="single")
The fit_predict method of this class fits the input data to the model and returns the predicted labels.

Distance Matrix for Agglomerative Clustering
The distance function in this code calculates the Euclidean distance between two points.

KNN
K-Nearest Neighbors is a classification algorithm that works by identifying the K nearest points in the training data to a new data point, and predicting the label based on the most common label among these neighbors.

Main KNN functions
The knn_main function in this code takes four input arguments:

sample: the data point to be classified
k: the number of neighbors to be considered
X: the training data
y: the training data labels
The function returns the predicted label for the input sample data point.

Creating new features for the train and test data
The datasets_for_KNN function in this code takes three input arguments:

df: the input data
n: the number of clusters to be formed
linkage: the type of linkage criteria to be used for the Agglomerative Clustering algorithm
The function splits the input data into training and testing sets, assigns cluster IDs as new species(labels), and returns the updated training and testing sets.



