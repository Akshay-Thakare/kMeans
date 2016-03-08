k-means clustering

1. Introduction to Algorithm

Say you are given a data set where each observed example has a set of features, but has no labels. Labels are an essential ingredient to a supervised algorithm like Support Vector Machines, which learns a hypothesis function to predict labels given features. So we can't run supervised learning. What can we do?

One of the most straightforward tasks we can perform on a data set without labels is to find groups of data in our dataset which are similar to one another -- what we call clusters.

K-Means is one of the most popular "clustering" algorithms. K-means stores kk centroids that it uses to define clusters. A point is considered to be in a particular cluster if it is closer to that cluster's centroid than any other centroid.

K-Means finds the best centroids by alternating between (1) assigning data points to clusters based on the current centroids (2) chosing centroids (points which are the center of a cluster) based on the current assignment of data points to clusters.

![alt tag](http://stanford.edu/~cpiech/cs221/img/kmeansViz.png)

Figure 1: K-means algorithm. Training examples are shown as dots, and cluster centroids are shown as crosses. (a) Original dataset. (b) Random initial cluster centroids. (c-f) Illustration of running two iterations of k-means. In each iteration, we assign each training example to the closest cluster centroid (shown by "painting" the training examples the same color as the cluster centroid to which is assigned); then we move each cluster centroid to the mean of the points assigned to it. Images courtesy of Michael Jordan.

2. Steps of implementation

In the clustering problem, we are given a training set x(1),...,x(m)x(1),...,x(m), and want to group the data into a few cohesive "clusters." Here, we are given feature vectors for each data point x(i)∈ℝnx(i)∈Rn as usual; but no labels y(i)y(i) (making this an unsupervised learning problem). Our goal is to predict kk centroids and a label c(i)c(i) for each datapoint. The k-means clustering algorithm is as follows:

![alt tag](http://stanford.edu/~cpiech/cs221/img/kmeansMath.png)

3.Objectives of the analysis

4.Data sets used snapshot

5.Step by Step calculation on that dataset.

6. Results and Discussions

6. Conclusion for your problem