# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries such as pandas, matplotlib, and KMeans from sklearn.
2.Read the customer dataset using pd.read_csv().
3.Choose Annual Income and Spending Score columns for clustering
4.Create the KMeans model with 5 clusters and fit it to the data.
5.Assign each customer to a cluster using fit_predict().
6.Plot the customer groups and centroids using a scatter plot.



## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: MOHAMMED GHUFRAN P
RegisterNumber:  212225230178
*/
# Simple K-Means Clustering Program for Customer Segmentation

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customer.csv")

x = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(x)

plt.scatter(x[:, 0], x[:, 1], c=y_kmeans, s=40)

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=180,
            marker='X',color='red')

# Labels
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()

```

## Output:
<img width="858" height="570" alt="593017890-c4e6274b-c866-4429-be81-25333a97f275" src="https://github.com/user-attachments/assets/ccccb198-6077-4d97-9d00-93bf11a9e899" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
