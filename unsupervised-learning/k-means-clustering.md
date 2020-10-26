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

![Process of K-means Clustering](../.gitbook/assets/image%20%281%29.png)

## Practice

```python
from sklearn.metrics import silhouette_score
k = 10
kmeans = KMeans(n_clusters=k, random_state = 0)
cluster_codes = KMeans.fit_predict(X) # results of clustering
test_score = silhouette_score(X, cluster_codes) #cluser_codes is labels
```

{% hint style="info" %}
The value of random\_state could affect the result of clustering centers.
{% endhint %}

### Visulization of clustering center

```python
import visuals as vs
k = 10
kmeans = KMeans(n_clusters=k, random_state = 0)
centers = kmeans.cluster_centers_
```

