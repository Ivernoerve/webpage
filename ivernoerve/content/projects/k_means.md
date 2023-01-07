---
title: "K-means clustering"
date: 2022-11-14T10:55:17+01:00
draft: true
imgpath: wordle.jpeg
math: true
---

K-means is an iterative clustering algorithm that classifies unlabeled into K different classes by finding K mean values best representing the given dataset.
Let $K$ be the number of clusters $i ∈ {1, 2, 3, . . . K}, i$ represent each individual cluster and the mean value assigned to it, and $D$ represent the dataset to perform the K-means clustering on:

1. Initiate the algorithm by selecting $K$ random values from the dataset, this will be the initial values $k_i$ for each cluster $i$.
2. Assign each value $v ∈ D$ from the dataset to cluster $i$ where the distance $|v − k_i|$ is minimized.
3. Calculate the cluster mean $k_i$ as the mean value of the data assigned to each cluster.
4. repeat step 2, 3 until a condition is met, commonly this can be that no value $v ∈ D$ changes it‘s associated cluster, a certain number of iterations, or that a cost function has been minimized.
5. Post convergence replace the value of each point to the value of it‘s associated cluster