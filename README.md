# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import libraries and load data.

2.Select features for clustering.

3.Fit KMeans model with chosen clusters (e.g., k=5).

4.Predict clusters and plot results.

5.Print cluster centers and finish.

## Program:
```
Program to implement the K Means Clustering for Customer Segmentation.
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# Load and prepare data
data = pd.read_csv("/content/Mall_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]

# Apply K-Means
kmeans = KMeans(n_clusters=5)
kmeans.fit(X)
labels = kmeans.labels_
centers = kmeans.cluster_centers_

# Plot clusters
colors = ['r', 'g', 'b', 'c', 'm']
for i in range(5):
    plt.scatter(X[labels==i]['Annual Income (k$)'], X[labels==i]['Spending Score (1-100)'], color=colors[i], label=f'Cluster {i+1}')
plt.scatter(centers[:,0], centers[:,1], color='black', s=200, label='Centroids')
plt.xlabel('Annual Income (k$)')
plt.ylabel('Spending Score (1-100)')
plt.title('K-Means Clustering')
plt.legend()
plt.grid(True)
plt.show()

```

## Output:
## VISUALIZE RAW DATA
![Screenshot 2025-04-21 225451](https://github.com/user-attachments/assets/5838612b-ffcf-4797-aacb-7a9faa7f0618)
## PRINT CLUSTER CENTERS
![Screenshot 2025-04-21 225512](https://github.com/user-attachments/assets/f2343d2c-b1f9-45f4-b9c7-39e9c235e039)

## Developed by : SANJEEV RAJ.S
## Reg no: 212223220096

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
