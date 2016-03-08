k-means clustering

**1. Introduction to Algorithm**

Say you are given a data set where each observed example has a set of features, but has no labels. Labels are an essential ingredient to a supervised algorithm like Support Vector Machines, which learns a hypothesis function to predict labels given features. So we can't run supervised learning. What can we do?

One of the most straightforward tasks we can perform on a data set without labels is to find groups of data in our dataset which are similar to one another -- what we call clusters.

K-Means is one of the most popular "clustering" algorithms. K-means stores kk centroids that it uses to define clusters. A point is considered to be in a particular cluster if it is closer to that cluster's centroid than any other centroid.

K-Means finds the best centroids by alternating between (1) assigning data points to clusters based on the current centroids (2) chosing centroids (points which are the center of a cluster) based on the current assignment of data points to clusters.

![alt tag](http://stanford.edu/~cpiech/cs221/img/kmeansViz.png)

_Figure 1: K-means algorithm. Training examples are shown as dots, and cluster centroids are shown as crosses. (a) Original dataset. (b) Random initial cluster centroids. (c-f) Illustration of running two iterations of k-means. In each iteration, we assign each training example to the closest cluster centroid (shown by "painting" the training examples the same color as the cluster centroid to which is assigned); then we move each cluster centroid to the mean of the points assigned to it. Images courtesy of Michael Jordan._

**2. Steps of implementation**

In the clustering problem, we are given a training set x(1),...,x(m)x(1),...,x(m), and want to group the data into a few cohesive "clusters." Here, we are given feature vectors for each data point x(i)∈ℝnx(i)∈Rn as usual; but no labels y(i)y(i) (making this an unsupervised learning problem). Our goal is to predict kk centroids and a label c(i)c(i) for each datapoint. The k-means clustering algorithm is as follows:

![alt tag](http://stanford.edu/~cpiech/cs221/img/kmeansMath.png)

**3.Objectives of the analysis**

This data will consist of one data point for each country consisting of two features: birth rate and death rate, measured in annual number of births/deaths per 1,000 people in the population. Since the population is constantly changing, it is measured at some time in the middle of the year to act as a reasonable estimate to the median of all population values throughout the year.

The raw data comes directly from the CIA’s World Factbook data estimate for 2012. Formally, we’re collecting the “crude birth rate” and “crude death rate” of each country with known values for both (some minor self-governing principalities had unknown rates). The “crude rate” simply means that the data does not account for anything except pure numbers; there is no compensation for the age distribution and fertility rates. Of course, there are many many issues affecting the birth rate and death rate, but we don’t have the background nor the stamina to investigate their implications here. Indeed, part of the point of studying learning methods is that we want to extract useful information from the data without too much human intervention (in the form of ambient knowledge).

**4. Results and Discussions**

_For 3 clusters_

Plot of child birth rates per 1000 vs death rate per 1000 across all countries in 2012. Whats interesting is that in developed countries like USA the death rate < birth rate while in developing countries like Afghanistan both the birth rate and death rates are quite high.

![alt tag](https://raw.githubusercontent.com/Akshay-Thakare/kMeans/master/figure_1.png)

![alt tag](http://jeremykun.files.wordpress.com/2013/02/countries-birth-deat-labeled.png?w=1800)



_Ref : http://jeremykun.com/2013/02/04/k-means-clustering-and-birth-rates/_
