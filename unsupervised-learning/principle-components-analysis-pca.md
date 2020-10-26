---
description: >-
  Decrease the dimension of datasets but keep the features which contribute to
  the variance most
---

# Principle Components Analysis\(PCA\)

> * variance: it measures how far a set of \(random\) numbers are spread out from their average value

> * covariance: Measure certain dimension whether can affect another dimension. It can describe relationship between two factors

## Steps of PCA

1. Average of each dimension
2. Minus the average
3. Set covariance matrice
4. Matrice decomposition
5. Rank eigenvector from high to low \(The first principle componet, the second...\)

## Coding 

### Get principle components

```python
from sklearn.decomposition import PCA
n_components = 10 # choose first 10 principle components
pca = PCA(n_components)
pca.fit(data) # Fitting
```

### Visulization of principle components

```python
def plot_pca_scatter(X_pca):
    """
        Visulization of principle components
    """
    colors = ['black', 'blue', 'purple', 'yellow', 'white', 'red', 'lime', 'cyan', 'orange', 'gray']
    for i in range(len(colors)):
        # Only show first two principle components
        px = X_pca[:, 0][y_digits == i]
        py = X_pca[:, 1][y_digits == i]
        plt.scatter(px, py, c=colors[i])
        
    plt.legend(digits.target_names)
    plt.xlabel('First Principal Component')
    plt.ylabel('Second Principal Component')

plot_pca_scatter(X_pca)
```

## Variance

```python
from sklearn.decomposition import PCA
n_components = 10 # choose first 10 principle components
pca = PCA(n_components)
var_ratio = pca.explained_variance_ratio_ # After pca, variance of each principle components
```

