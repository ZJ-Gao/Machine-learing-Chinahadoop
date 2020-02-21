# K-Means Clustering

## Basic

* Clustering belongs to unsupervised learning
* Samples don't have labels
* Parameter: K \(number of clusters\)

## Description of algorithm

* Set up K value
* Choose K clustering centers
* For each sample, calculate the distance between centers and this sample
* **Belong** to the closet center
* **Update center** according the average value of one cluster
* Until achieve the **max iteration** or **no change** of updated center \(Distance = 0 between new and old center \)

![Process of K-means Clustering](.gitbook/assets/image%20%281%29.png)

## Practice

```python
k = 10
kmeans = KMeans(n_clusteres=k, random_state = 0)
cluster_codes = kmeans.fit_predict(X) # results of clustering
```

